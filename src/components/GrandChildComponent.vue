<template>
  <div>
    <h3>GrandChild Component</h3>
    <button @click="sendMessageToChild">Send Message to Child</button>
  </div>
</template>

<script>
export default {
  name: 'GrandChildComponent',
  methods: {
    sendMessageToChild() {
      this.$emit('grandchild-message', 'Hello from GrandChild Component');
    }
  }
};
</script>
