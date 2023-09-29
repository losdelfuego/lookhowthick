<script setup>
import { ref } from 'vue'

defineProps({
  msg: String,
})

const count = ref(0)
</script>

<template>
  <h1 v-if="count < 500">{{ msg }}</h1>
  <h1 v-else>That's Too Thick!!!</h1>

  <div class="card">
    <button type="button" @click="count++">count is {{ count }}</button>
    <p>
      (Clicking on this does nothing.)
    </p>
  </div>

  <div v-if="count > 20">
    <p>
      (It really doesn't.)
    </p>
  </div>

  <div v-if="count > 100">
    <p>
      (Stop clicking. I won't warn you again.)
    </p>
  </div>

  <div v-if="count > 250">
    <p>(Seriously.)

    </p>
  </div>
</template>

<style scoped>
.read-the-docs {
  color: #888;
}
</style>
