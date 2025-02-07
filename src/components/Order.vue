<script setup>
import { ref } from 'vue'

defineProps({
  item1: String,
  item2: String,
  item3: String,
})

const count1 = ref(0)
const count2 = ref(0)
const count3 = ref(0)

</script>

<template>
  <h1>Order</h1>

  <div class="cards">
    <div class="card">
      <h2>{{item1}}</h2>
      <div class="counter">
        <button type="button" @click="count1--">-</button>
        <p>{{count1}}</p>
        <button type="button" @click="count1++">+</button>
      </div>
    </div>
    <div class="card">
      <h2>{{item2}}</h2>
      <div class="counter">
        <button type="button" @click="count2--">-</button>
        <p>{{count2}}</p>
        <button type="button" @click="count2++">+</button>
      </div>
    </div>
    <div class="card">
      <h2>{{item3}}</h2>
      <div class="counter">
        <button type="button" @click="count3--">-</button>
        <p>{{count3}}</p>
        <button type="button" @click="count3++">+</button>
      </div>
    </div>
  </div>

</template>

<style scoped>
.cards {
  display: flex;
  gap: 20px;
  justify-content: center;
  align-items: center;
}
.card {
  display: flex;
  flex-direction: column;
  align-items: center;
  border: 1px solid #ccc;
  padding: 10px;
  border-radius: 5px;
}
.counter {
  display: flex;
  align-items: center;
}
</style>
