<template>
  <header class="header__header">
    <div class="header__container">
      <TheNavigation />
      <div class="backround-shadowing"></div>
      <div class="header__container--main">
        <div class="social__container">
          <span class="social__line"></span>
          <a href="#" class="social__link"
            ><img
              src="@/assets/images/instagram_icon.svg"
              alt="Instagram logo"
              class="social__icon"
          /></a>
          <a href="#" class="social__link"
            ><img
              src="@/assets/images/unsplash_icon.svg"
              alt="Unsplash logo"
              class="social__icon"
          /></a>
          <span class="social__line"></span>
        </div>
        <div class="header__container--text">
          <h1 class="header__h1">Leon Schwarzmueller</h1>
          <h2 class="header__h2">
            I have been engaged in photography for over 8 years. I conduct
            commercial photo shoots and video filming.
          </h2>
        </div>
      </div>
    </div>
  </header>
</template>

<script>
import TheNavigation from '@/components/heading/navigation/Navigation'

export default {
  components: {
    TheNavigation,
  },
}
</script>

<style lang="sass" scoped>
$orange: #FC7411

.header__header
  height: 100vh
  background: url('@/assets/images/header-background.jpg') left top/cover no-repeat

.header__container--main
  display: flex
  color: #fff
  position: relative
  // align-items: center

.header__container--text
  display: flex
  flex-direction: column
  align-self: flex-end
  margin: 0 0 0 4.5em
  max-width: 33em
  .header__h1
    font-size: 2.7em
    color: $orange
    font-family: 'Verdana Bold', sans-serif
  .header__h2
    font-size: 1em
    font-weight: 400

.backround-shadowing
  position: absolute
  width: 75vw
  height: calc(100vh - 3.6em)
  left: 0
  top: 3.6em
  background: linear-gradient(-90deg, rgba(0, 0, 0, 0) 0%, rgba(0, 0, 0, 0.85) 50%)

.social__container
  display: flex
  position: relative
  flex-direction: column
  align-items: center
  justify-content: center
  width: fit-content

.social__line
  background-color: $orange
  width: 3px
  height: 18vh
  margin-bottom: 40px
  &:last-child
    margin-bottom: 0

.social__icon
  width: 32px
  height: 32px

.social__link
  margin-bottom: 40px
</style>
