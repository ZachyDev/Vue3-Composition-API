<template>
  <div>
      <h2>{{ capacity }}</h2>
      <button @click="increaseCapacity()">Increase Capacity</button>
  </div>
</template>

<script>
import { ref } from 'vue';
export default {
    setup() {
        const capacity = ref(0);
        function increaseCapacity() {
            capacity.value++;
        }
        return { capacity, increaseCapacity };
    }
}
</script>

<style>

</style>