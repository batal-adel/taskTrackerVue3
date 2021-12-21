<template>
  <button @click="onClick()" class="btn" :style="{ background: color }">
    {{ text }}
  </button>
</template>

<script>
export default {
  name: 'Button',
  props: {
    text: {
      type: String,
      default: 'broken button',
    },
    color: {
      type: String,
      default: 'grey',
    },
    showAddTask: {
      type: Boolean,
      default: false,
    },
  },
  methods: {
    onClick() {
      this.$emit('btn-click');
    },
  },
};
</script>
