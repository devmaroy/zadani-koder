<template>
  <button v-if="type !== 'link'" :class="buttonClass">
    <slot></slot>
  </button>
  <a v-else :class="buttonClass" :href="href">
    <slot></slot>
  </a>
</template>

<script>
export default {
  name: "Button",
  props: {
    type: {
      type: String,
      default: "button",
    },
    variant: {
      type: String,
      default: "blue",
    },
    size: {
      type: String,
      default: "md",
    },
    className: {
      type: String,
      default: "",
    },
    href: {
      type: String,
      default: "#",
    },
  },
  computed: {
    buttonClass() {
      return this.className
        ? `${this.className} button--${this.variant} button--${this.size}`
        : `button button--${this.variant} button--${this.size}`;
    },
  },
};
</script>

<style scoped>
/* Add your button styles here */
</style>
