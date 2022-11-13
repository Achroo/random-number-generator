<template>
  <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->
  <div class="align-middle mx-auto px-4 bg-slate-300 h-3/4 w-2/4 text-black rounded-lg">
        <h1 class="text-5xl font-sans pt-8 pb-8">Dice App</h1>
        <h2 class="text-2xl font-sans pb-6">Choose the type of dice</h2>
        <div class="flex justify-around buttons-container">
            <DiceButton text="D3"></DiceButton>
            <DiceButton text="D4"></DiceButton>
            <DiceButton text="D6"></DiceButton>
            <DiceButton text="D10"></DiceButton>
            <DiceButton text="D12"></DiceButton>
            <DiceButton text="D20"></DiceButton>
        </div>

        <h2 class="text-2xl font-sans pt-8 pb-6">Choose the number of dices</h2>
        <div class="flex justify-around buttons-container pb-8">
            <DiceButton text="1"></DiceButton>
            <DiceButton text="2"></DiceButton>
            <DiceButton text="3"></DiceButton>
            <DiceButton text="4"></DiceButton>
            <DiceButton text="5"></DiceButton>
            <DiceButton text="6"></DiceButton>
        </div>

        <div class="buttons-container pb-8">
          <button class="mx-auto w-28 h-16 rounded-lg bg-red-700 hover:bg-red-800">
              <h1 class=" text-xl font-sans">Roll</h1>
          </button>
        </div>
    </div>
</template>

<script>
import DiceButton from './components/DiceButton.vue'

export default {
  name: 'App',
  components: {
    DiceButton
  }
}
</script>

<style>
@tailwind base;
@tailwind components;
@tailwind utilities;

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
