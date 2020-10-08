<template>
  <div> 
      <h2> Geeky Sesion by {{ name }}.</h2>
      <button @click="increaseCapacity()">Increase Capacity</button> <span>{{ capacity }}</span>
      <button @click="getData()">Fetch Data</button>
      <h2>{{companies}}</h2>
  </div>
</template>

<script>
import { ref } from 'vue';
import axios from 'axios';
export default {
    setup() {
        const capacity = ref(0);
        const companies = ref('hello');
        const name = ref('ZachyDev');
        // const companies = ref('https://my-json-server.typicode.com/ZachyDev/ZachyAPI/companies');
        function increaseCapacity() {
            capacity.value++;
        }
        function getData() {
            axios.get('https://my-json-server.typicode.com/ZachyDev/ZachyAPI/companies')
                .then(res => {
                    companies.value = res.data;
                })
        } 
        return { name, capacity, increaseCapacity,getData, companies };
    }
}
</script>

<style>

</style>