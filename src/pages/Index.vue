<template>
  <Layout>
    <section class="bg-black text-white pt-64 pb-32 relative">
      <div class="pt-64 container mx-auto">
        <div class="flex">
          <g-image src="~/dotted-trianlge.svg" class="mr-4 -ml-Hello kuda32"/>
          <div class="">
            <h1 class="text-5xl font-black">Portfolio</h1>
            <p class="text-lg">See what I have created in the past and enjoy yourself!</p>
          </div>
        </div>


        <div class="mt-32 flex justify-between -mx-16 flex-wrap" >
          <div class="px-16 py-2 w-1/2 gallery-image" v-for="i in 4" :key="i">
            <div class="bg-white p-4 relative" @mouseenter="showDescriptionFor(i)" @mouseleave="hideDescription" >
              <div :class="{hidden: shownDescription !== i }" class=" absolute flex flex-col justify-between center-absolute bg-transparent-yellow-brand text-black">
                <div class="p-4">
                  <h2 class="text-3xl  font-medium mb-4">Prazlion - Procurement System</h2>
                  <p class="text-lg">Internal app capable of doing X,Y and Z.</p>
                </div>

                <button class="bg-black text-white text-lg w-full p-4">
                  Visit Project
                </button>
              </div>
              <!-- The image of the  -->
              <div class="w-full flex-1  mb-4">&nbsp;
                <g-image src="~/highlight-procurement.png"/>
              </div>
            </div>
            <!-- Visit the applicatioin -->
          </div>
          
          <div class="px-16 gallery-image">
            <button class="border-2 border-white text-white text-lg  p-4">
              See more of my work &rightarrow;
            </button>
          </div>
        </div>
      </div>
    </section>
  </Layout>
</template>

<script>
export default {
  metaInfo: {
    title: 'Hello, world!'
  },

  data () {
    return {
      shownDescription: null
    }
  },

  methods: {
    showDescriptionFor(i) {
      this.shownDescription = i
    },

    hideDescription() {
      this.shownDescription = null
    }
  }
}
</script>

<style>
.home-links a {
  margin-right: 1rem;
}

.gallery-image:nth-child(even) {
  @apply mt-16;
}

.gallery-image:nth-child(odd) {
  @apply -mt-16;
}

.bg-transparent-yellow-brand {
  background-image: linear-gradient(#fdd231, #fdd2310a)
}

.center-absolute {
  width: calc(100% - 2rem);
  height: calc(100% - 2rem);
}
</style>
