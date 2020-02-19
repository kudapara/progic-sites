<template>
  <div class="layout bg-black">
    <div id="stars"></div>
    <div id="stars1"></div>
    <div id="stars2"></div>
    <header class="bg-yellow-brand p-4">
      <nav class="container mx-auto flex items-center justify-between">
        <div>
          <a href="#" class="nav__link">Portfolio</a>
          <a href="#" class="nav__link" to="#">Services</a>
          <a href="#" class="nav__link" to="#">Services</a>
        </div>

        <div class='bg-white p-4 rounded-lg shadow w-24 mr-8'>
          <g-image src="~/progic-logo.svg" class="w-full" />
          <span class="text-gray-800 text-center block">Founder</span>
        </div>

        <div>
          <a href="#" class="nav__link">Twitter</a>
          <a href="#" class="nav__link" to="#">Github</a>
          <a href="#" class="nav__link" to="#">Blog</a>
        </div>
      </nav>


      <div class="text-center my-24 ">
        <h1 class="text-5xl font-black">It's Kudakwashe Paradzayi</h1>
        <p class="text-lg">A very brief but concise description about the value I can provide to clients</p>
      </div>

      <div class="text-center mb-48">
        <button class="py-2 px-4 bg-black text-white text-lg rounded shadow uppercase">call to action</button>
      </div>

    </header>

    <!-- Higglight the app of the month -->

    <section class="flex justify-center">
      <div class="w-full max-w-xl absolute z-50 -mt-32">
        <div class="text-right -mb-4 mr-4">
            <span class="inline-block bg-yellow-brand shadow border-2 border-black py-1 px-4 rounded">App Of The Month</span>
        </div>

        <div class="flex flex-col bg-white w-full shadow-lg rounded p-4">
          <!-- the maximize, resize and close buttons-->
          <div class="flex mb-4">
            <div class="h-4 w-4 rounded-full bg-red-400 mr-2">&nbsp;</div>
            <div class="h-4 w-4 rounded-full bg-yellow-400 mr-2">&nbsp;</div>
            <div class="h-4 w-4 rounded-full bg-green-400">&nbsp;</div>
          </div>

          <!-- The image of the  -->
          <div class="w-full flex-1  mb-4">&nbsp;
            <g-image src="~/highlight-procurement.png"/>
          </div>

          <!-- Visit the applicatioin -->

          <button class="border-2 border-black text-lg w-full p-4">
            Visit Project
          </button>
        </div>
      </div>
    </section>  
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
@import url('https://rsms.me/inter/inter.css');
html { font-family: 'Inter', sans-serif; }
@supports (font-variation-settings: normal) {
  html { font-family: 'Inter var', sans-serif; }
}

.nav__link {
  @apply mr-8 font-medium text-xl
}

</style>
