<template>
  <div>
    <h1>Parent Component</h1>
    <p>Message from Child: {{ message }}</p>
    <ChildComponent @message-emitted="handleMessage">
      <template #slotContent>
        <p>This is a slot content from Parent</p>
      </template>
    </ChildComponent>
  </div>
</template>

<script>
import ChildComponent from './ChildComponent.vue';

export default {
  name: 'ParentComponent',
  components: {
    ChildComponent
  },
  data() {
    return {
      message: ''
    };
  },
  methods: {
    handleMessage(msg) {
      this.message = msg;
    }
  }
};
</script>
