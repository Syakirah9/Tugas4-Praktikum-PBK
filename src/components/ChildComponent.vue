<template>
  <div>
    <h2>Child Component</h2>
    <slot name="slotContent"></slot>
    <button @click="sendMessageToParent">Send Message to Parent</button>
    <GrandChildComponent @grandchild-message="sendMessageToParent" />
  </div>
</template>

<script>
import GrandChildComponent from './GrandChildComponent.vue';

export default {
  name: 'ChildComponent',
  components: {
    GrandChildComponent
  },
  methods: {
    sendMessageToParent(msg = 'Hello from Child Component') {
      this.$emit('message-emitted', msg);
    }
  }
};
</script>
