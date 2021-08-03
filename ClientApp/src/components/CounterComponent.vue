<template>
  <div>
    <p class="my-3">
      Current count:
      <strong>{{ currentCount }}</strong>
    </p>
    <button class="mr-2 btn btn-primary" @click.prevent="increment">Increment</button>
    <button class="btn btn-secondary" @click.prevent="reset">Reset</button>
  </div>
</template>

<script setup lang="ts">
    import { ref } from 'vue'

const currentCount = ref(0)

    const increment = (): void => {
        currentCount.value++
}

    const reset = (): void => {
        currentCount.value = 0
}
</script>
