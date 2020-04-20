<template>
  <div class="layout font-sans  text-xl">
    <div class="bg-black">

    <div id="stars"></div>
    <div id="stars1"></div>
    <div id="stars2"></div>
    <header class="container mx-auto mt-12">
      <nav class="flex items-center">
        <g-image src="~/progic-logo-light.svg" alt="" class="mr-8"/>
        <g-image src="~/brought-to-you-by-kudapara.svg" alt=""/>

        <div class="flex-1 flex justify-end  text-white">
          <a href="#" class="mx-4">Why Progic?</a>
          <a href="#" class="mx-4">Services</a>
          <a href="#" class="mx-4">Showcase</a>
          <a href="#" class="mx-4">Get in touch</a>
        </div>
      </nav>
    </header>

    </div>
    <!-- Higglight the app of the month --> 
    <slot/>
  </div>
</template>

<static-query>
query {
  metadata {
    siteName
  }
}
</static-query>

<style>
/* @import url('https://rsms.me/inter/inter.css'); */
@import url('https://fonts.googleapis.com/css2?family=Inter&family=Sansita:wght@400;900&display=swap');
html {font-family: 'Inter', sans-serif; }
@supports (font-variation-settings: normal) {
  html { font-family: 'Inter var', sans-serif; }
}

.nav__link {
  @apply mr-4 font-medium text-indigo-600 underline
}

</style>
