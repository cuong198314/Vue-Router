<template>
  <div class="reverse">
    <h1>This is the Reverse Page</h1>
    <h2> Please enter a string to reverse!</h2>
    <label>String:
      <input type="text" id="string" v-model.lazy="message">
    </label>
    <h2>The reverse message is:</h2>
    <p>{{ reverseMessage }}</p>
  </div>
</template>

<script>
export default {
  name: 'Reverse',
  data() {
    return {
      message: ''
    }
  },
  computed: 
  {
    reverseMessage() {
      return this.message.split('').reverse().join('');
    }
  }
}
</script>