<template>
  <div class="layout font-sans  sm:text-xl">
    <div class="bg-black">

    <div id="stars"></div>
    <div id="stars1"></div>
    <div id="stars2"></div>
    <header class="container mx-auto mt-12">
      <nav class="flex items-center flex-wrap sm:flex-no-wrap">
        <div class="flex justify-center sm:justify-start w-full">
          <g-image src="~/progic-logo-light.svg" alt="" class="mr-8"/>
          <g-image src="~/brought-to-you-by-kudapara.svg" alt=""/>
        </div>

        <div class="flex-1 flex items-center justify-center sm:justify-end text-white mt-8 sm:mt-0 flex-wrap sm:flex-no-wrap">
          <a href="#why-progic" class="mx-4 whitespace-no-wrap">Why Progic?</a>
          <a href="#showcase" class="mx-4 whitespace-no-wrap">Showcase</a>
          <a href="#services" class="mx-4 whitespace-no-wrap">Services</a>
          <a href="#get-in-touch" class="mx-4 p-4 border-2 border-white text-center whitespace-no-wrap w-full sm:w-auto mt-4 sm:mt-0 hover:bg-white hover:text-black">Get in touch</a>
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
