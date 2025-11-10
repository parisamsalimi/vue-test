<script setup>
import { ref } from 'vue'
const text = ref ('Edit me')
const checked = ref(true)
const checkedNames = ref(['Jack'])
const picked = ref(['one'])
const selected = ref('A')
const multiSelected = ref ('A')

</script>
<template>
  <h1 class="title">Text Input</h1>
  <input class="inp" v-model="text">{{ text }}</input>

  <h2>Checkbox</h2>
  <input type="checkbox" id="checkbox" v-model="checked">
  <label for="checkbox">Checked: {{ checked }}</label>

  <h2>Multi Checkbox</h2>
  <input type="checkbox" id="jack" value="Jack" v-model="checkedNames">
  <label for="jack">Jack</label>
  <input type="checkbox" id="john" value="John" v-model="checkedNames">
  <label for="john">John</label>
  <input type="checkbox" id="mike" value="Mike" v-model="checkedNames">
  <label for="mike">Mike</label>
  <input type="checkbox" id="pari" value="pari" v-model="checkedNames"></input>
  <label for="parisa">parisa</label>
  <p>Checked names: {{ checkedNames }}</p>

  <h2>Radio</h2>
  <input type="radio" id="one" value="One" v-model="picked">
  <label for="one">One</label>
  <br>
  <input type="radio" id="two" value="Two" v-model="picked">
  <label for="two">Two</label>
  <br>
  <input type="radio" id="three" value="three" v-model="picked"></input>
  <label for="three">three</label>
</br>
  <p>Picked: {{ picked }}</p>

  <h2>selecte</h2>
  <select v-model="selected">
    <option>Please select one  </option>

      <option>A</option>
      <option>B</option>
      <option>C</option>
  </select>
  <p> Selected : {{ selected }}</p>

  <h2>Multi Select</h2>
  <select v-model="multiSelected" multiple style="width:100px">
    <option>A</option>
    <option>B</option>
    <option>C</option>
  </select>
  <p>Selected: {{ multiSelected }}</p>
</template>





  

<style scoped>

.title{
  margin: 0 auto;
  
}
.inp{
  margin-top: 10px;
  margin-right: 10px;
}
</style>
