<template>
  <div class="secondary-button-container" v-bind:class="rootClassName">
    <button class="secondary-button-button TextXS button">{{ button }}</button>
  </div>
</template>

<script>
export default {
  name: 'SecondaryButton',
  props: {
    button: {
      type: String,
      default: 'Button',
    },
    rootClassName: String,
  },
}
</script>

<style scoped>
.secondary-button-container {
  display: flex;
  position: relative;
}
.secondary-button-button {
  color: var(--dl-color-gray-white);
  box-shadow: 0 1px 3px 0 rgba(0,0,0,0.1),0 1px 2px 0 rgba(0,0,0,0.06);
  transition: 0.3s;
  line-height: 1;
  padding-top: var(--dl-space-space-halfunit);
  border-width: 0px;
  padding-left: var(--dl-space-space-unit);
  padding-right: var(--dl-space-space-unit);
  padding-bottom: var(--dl-space-space-halfunit);
  text-transform: uppercase;
  background-color: var(--dl-color-secondary-300);
}
.secondary-button-button:hover {
  box-shadow: 0 4px 6px -1px rgba(0,0,0,0.1),0 2px 4px -1px rgba(0,0,0,0.06);
}
.secondary-button-button:active {
  background-color: var(--dl-color-secondary-100);
}

</style>
