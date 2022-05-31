<template>
  <div class="[ app-container ] [ max-width-1100 ]">
    <menu-header class="[ menu ] [ pad-bottom-600 box-flex full-bleed-md ]"/>
    <main class="md:box-flex flex-between">
      <section class="[ hero__image-container ] [ full-bleed ]">
        <picture>
          <source media="(min-width: 48em)" srcset="/images/image-hero-desktop.png">
          <img src="/images/image-hero-mobile.png" alt="Man using laptop">
        </picture>
      </section>
      <section class="[ hero__content ] [ text-center flow text-left-md ]">
        <h1><span class="desktop-active">Make</span> remote work</h1>
        <p class="font-grey md:text-500">Get your team in sync, no matter your location. Streamline processes, create team rituals, and watch productivity soar.</p>
        <button class="[ hero-button ] [ weight-bold bg-black font-white md:text-500 ]">Learn more</button>
        <endorsement-hero class="[ endorsement-container ] [ flex-gap-400 ]" />
      </section>
    </main>
  </div>
</template>

<script>
import EndorsementHero from '~/components/EndorsementHero.vue'
import MenuHeader from '~/components/MenuHeader.vue'
export default {
  components: { MenuHeader, EndorsementHero },
  name: 'IndexPage',
}
</script>
