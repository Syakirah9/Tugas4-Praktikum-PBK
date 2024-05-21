<template>
    <div>
      <slot-component>
        <p>This content is passed from the parent component.</p>
      </slot-component>
    </div>
  </template>
  
  <script>
  import SlotComponent from './SlotComponent.vue';
  
  export default {
    name: 'ParentWithSlotComponent',
    components: {
      SlotComponent
    }
  }
  </script>
  