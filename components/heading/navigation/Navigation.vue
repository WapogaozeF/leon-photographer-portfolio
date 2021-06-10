<template>
  <nav class="navigation__nav">
    <div class="navigation__container">
      <h2 class="navigation__h2">Commercial photographer and cameraman</h2>
      <span class="navigation__container--shielding">
        <a
          href="tel:+4904827954951"
          class="navigation__link navigation__link--phone"
        >
          +49 (048) 2795-4951</a
        >
      </span>
      <div class="header__container--select-lang">
        <NuxtLink to="/de" class="header__link--select-lang">DE</NuxtLink>
        <NuxtLink to="/" class="header__link--select-lang">EN</NuxtLink>
      </div>
      <Hamburger class="navigation__button" />
    </div>
  </nav>
</template>

<script>
import Hamburger from '@/components/heading/navigation/menu/Hamburger'

export default {
  components: {
    Hamburger,
  },
}
</script>

<style lang="sass" scoped>
.navigation__nav
    color: #fff
    height: 3.6em
    width: 100vw
    background-color: rgba(0, 0, 0, 0.85)

.navigation__container
    height: 100%
    max-width: 1320px
    display: flex
    justify-content: space-between
    align-items: center
    margin: 0 auto

.navigation__container--shielding
    flex-grow: 4

.navigation__h2
    text-align: left
    font-size: 0.8em
    font-weight: 400
    flex-grow: 2

.navigation__link, .header__link--select-lang
    font-size: 1em
    color: #fff
    text-decoration: underline

.navigation__link--phone
    text-align: right
    display: none
    width: fit-content
    margin-left: auto

.header__link--select-lang
    text-decoration: none
    margin-right: 2vw
    &:last-child
        margin-right: 0

.header__container--select-lang
    flex-grow: 2
    text-align: center
    display: none

.navigation__button
    flex-grow: 1
    text-align: right

.nuxt-link-active, .nuxt-link-exact-active
    font-size: 1em
    color: #FC7411
    text-decoration: underline

@media only screen and (max-width: 576px)
    .navigation__container
        margin: 0 30px

@media only screen and (min-width: 576px)
    .navigation__container
        max-width: 540px

@media only screen and (min-width: 768px)
    .navigation__container
        max-width: 720px
    .header__container--select-lang
        display: block
    .navigation__h2
        font-size: 1em

@media only screen and (min-width: 992px)
    .navigation__container
        max-width: 960px
    .navigation__link--phone
        display: block

@media only screen and (min-width: 1200px)
    .navigation__container
        max-width: 1140px

@media only screen and (min-width: 1400px)
    .navigation__container
        max-width: 1320px
</style>
