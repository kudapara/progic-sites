<template>
  <div class="layout bg-black">
    <div id="stars"></div>
    <div id="stars1"></div>
    <div id="stars2"></div>
    <header class="bg-yellow-brand p-4 py-24">
      &nbsp;
    </header>

    <!-- Higglight the app of the month -->

    <section class="flex justify-center">
      <div class="w-full max-w-xl bg-white absolute z-50 -mt-32 border-4 rounded-xl shadow-xl border-black p-8">
        <div class="flex items-center justify-between">
          <div class="flex items-end mb-4">
            <g-image src="~/me.jpg" class="relative z-30 w-16 h-16 rounded-full mr-2 shadow-inner" />
            <div>
              <h3 class="text-md font-medium mb-1">Kudakwashe Paradzayi</h3>
              <a href="https://twitter.com/kudapara" class="text-indigo-600">@kudapara</a>
            </div>
          </div>

          <div>
            <button class="px-4 py-2 border-2 border-black text-black font-medium rounded-full">Follow</button>
          </div>
        </div>

        <div>
          <p class="mb-4">
            Hey, I am a full stack web developer. My mission is to build software that will make the lives of people better whilst making profit for your business.
          </p>


          <div>
            <nav class="container mx-auto flex items-center justify-between mb-4">
              <div>
                <a href="#" class="nav__link">Portfolio</a>
                <a href="#" class="nav__link" to="#">Services</a>
                <a href="#" class="nav__link" to="#">Work</a>
 
                <a href="#" class="nav__link">FAQs</a>
                <a href="#" class="nav__link" to="#">Testimonials</a>
                <a href="#" class="nav__link" to="#">Newsletter</a>
              </div>
            </nav>

          </div>

        <a href="#apply-for-work" class="inline-block p-4 bg-black text-white text-lg rounded shadow">Let's build something amazing, together &rightarrow;</a>

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
  @apply mr-4 font-medium text-indigo-600 underline
}

</style>
