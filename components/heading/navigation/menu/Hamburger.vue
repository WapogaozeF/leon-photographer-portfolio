<template>
  <button :class="menuClass" type="button" @click="changeMenuStatus">
    <span class="hamburger-box">
      <span class="hamburger-inner"></span>
    </span>
  </button>
</template>

<script>
export default {
  data() {
    return {
      status: true,
    }
  },
  computed: {
    menuClass() {
      const defaultClass = 'hamburger hamburger--slider'
      return !this.status ? `${defaultClass} is-active` : defaultClass
    },
  },
  methods: {
    changeMenuStatus() {
      this.status = !this.status
    },
  },
}
</script>

<style lang="sass" scoped>
$hamburger-padding-x: 14px !default
$hamburger-padding-y: 14px !default
$hamburger-layer-width: 25px !default
$hamburger-layer-height: 2px !default
$hamburger-layer-spacing: 5px !default
$hamburger-layer-color: #fff !default
$hamburger-layer-border-radius: 0 !default
$hamburger-hover-opacity: 0.6 !default

.hamburger
  margin-top: 7px
  &:focus
    outline: none

.hamburger-box
  vertical-align: middle

@import '@/node_modules/hamburgers/_sass/hamburgers/hamburgers.scss'
</style>
