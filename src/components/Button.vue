<template>
  <!-- v-on:click="onClick()" === @click for adding an event -->
  <button @click="onClick()" v-bind:style="{background: color}" class="btn">{{ text  }}</button>
</template>

<script>
  export default {
    /* eslint-disable */
    name: "Button",
    props: {
      text: String,
      color: String
    }, 
    methods: {
      // adding a method when an event is defined
      onClick() {
        this.$emit('toggle-add-task')
      }
    }
  }

</script>