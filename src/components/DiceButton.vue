<script>
export default {
  name: 'DiceButton',
  props: {
    text: String
  }
}
</script>

<template lang="en">
    <button class="flex justify-center items-center w-28 h-16 rounded-lg bg-blue-500 hover:bg-blue-600">
        <h1 class=" text-xl font-sans">{{text}}</h1>
    </button>
</template>

<style lang="">
    
</style>