<template>
  <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->
  <div class="align-middle mx-auto px-4 bg-slate-300 h-3/4 w-2/4 text-black rounded-lg">
        <h1 class="text-5xl font-sans pt-8 pb-8">Dice App</h1>
        <h2 class="text-2xl font-sans pb-6">Choose the type of dice</h2>
        <div class="flex justify-around buttons-container">
            <DiceButton v-on:click="setDiceType(3)" text="D3"></DiceButton>
            <DiceButton v-on:click="setDiceType(4)" text="D4"></DiceButton>
            <DiceButton v-on:click="setDiceType(6)" text="D6"></DiceButton>
            <DiceButton v-on:click="setDiceType(10)" text="D10"></DiceButton>
            <DiceButton v-on:click="setDiceType(12)" text="D12"></DiceButton>
            <DiceButton v-on:click="setDiceType(20)" text="D20"></DiceButton>
        </div>

        <h2 class="text-2xl font-sans pt-8 pb-6">Choose the number of dices</h2>
        <div class="flex justify-around buttons-container pb-8">
            <DiceButton v-on:click="setDiceNumber(1)" text="1"></DiceButton>
            <DiceButton v-on:click="setDiceNumber(2)" text="2"></DiceButton>
            <DiceButton v-on:click="setDiceNumber(3)" text="3"></DiceButton>
            <DiceButton v-on:click="setDiceNumber(4)" text="4"></DiceButton>
            <DiceButton v-on:click="setDiceNumber(5)" text="5"></DiceButton>
            <DiceButton v-on:click="setDiceNumber(6)" text="6"></DiceButton>
        </div>

        <div class="buttons-container pb-8">
          <button v-on:click="rollDice()" class="mx-auto w-28 h-16 rounded-lg bg-red-700 hover:bg-red-800">
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
  },
  methods : {
    rollDice() {
      console.log('Rolling dice')
      console.log(this.diceType, this.diceNumber)
    },
    setDiceType(type) {
      console.log('Setting dice type ' + type)
      this.diceType = type
    },
    setDiceNumber(number) {
      console.log('Setting dice number ' + number)
      this.diceNumber = number
    }
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
