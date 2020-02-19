<template>
  <Layout>
    <section class="bg-black text-white pt-64 pb-32 relative">
      <div class="pt-64 container mx-auto">
        <div class="flex">
          <g-image src="~/dotted-trianlge.svg" class="mr-4 -ml-Hello kuda32" />
          <div class>
            <h1 class="text-5xl font-black">Portfolio</h1>
            <p class="text-lg">See what I have created in the past and enjoy yourself!</p>
          </div>
        </div>

        <div class="mt-32 flex justify-between -mx-16 flex-wrap">
          <div class="px-16 py-2 w-1/2 gallery-image" v-for="i in 4" :key="i">
            <div
              class="bg-white p-4 relative"
              @mouseenter="showDescriptionFor(i)"
              @mouseleave="hideDescription"
            >
              <div
                :class="{hidden: shownDescription !== i }"
                class="absolute flex flex-col justify-between center-absolute bg-transparent-yellow-brand text-black"
              >
                <div class="p-4">
                  <h2 class="text-3xl font-medium mb-4">Prazlion - Procurement System</h2>
                  <p class="text-lg">Internal app capable of doing X,Y and Z.</p>
                </div>

                <button class="bg-black text-white text-lg w-full p-4">Visit Project</button>
              </div>
              <!-- The image of the  -->
              <div class="w-full flex-1 mb-4">
                &nbsp;
                <g-image src="~/highlight-procurement.png" />
              </div>
            </div>
            <!-- Visit the applicatioin -->
          </div>

          <div class="px-16 gallery-image">
            <button
              class="border-2 border-white text-white text-lg p-4"
            >See more of my work &rightarrow;</button>
          </div>
        </div>
      </div>
    </section>

    <section class="bg-black text-white py-64 relative">
      <div class="container mx-auto flex">
        <div>
          <div class="flex pr-24 mb-32">
            <g-image src="~/dotted-trianlge.svg" class="mr-4 -ml-Hello kuda32" />
            <div class>
              <h1 class="text-5xl font-black">This is what I do</h1>
              <p
                class="text-2xl"
              >This is my pitch.What I can do for you. I am selling myself to you, my potential client.</p>
            </div>
          </div>

          <div class="ml-36 pl-4">
            <ul>
              <li v-for="service in services" :key="service" class="flex items-center text-xl py-2">
                <svg
                  class="mr-4"
                  width="24"
                  height="24"
                  viewBox="0 0 24 24"
                  fill="none"
                  xmlns="http://www.w3.org/2000/svg"
                >
                  <path
                    d="M12 22C9.34784 22 6.8043 20.9464 4.92893 19.0711C3.05357 17.1957 2 14.6522 2 12C2 9.34784 3.05357 6.8043 4.92893 4.92893C6.8043 3.05357 9.34784 2 12 2C14.6522 2 17.1957 3.05357 19.0711 4.92893C20.9464 6.8043 22 9.34784 22 12C22 14.6522 20.9464 17.1957 19.0711 19.0711C17.1957 20.9464 14.6522 22 12 22ZM12 20C14.1217 20 16.1566 19.1571 17.6569 17.6569C19.1571 16.1566 20 14.1217 20 12C20 9.87827 19.1571 7.84344 17.6569 6.34315C16.1566 4.84285 14.1217 4 12 4C9.87827 4 7.84344 4.84285 6.34315 6.34315C4.84285 7.84344 4 9.87827 4 12C4 14.1217 4.84285 16.1566 6.34315 17.6569C7.84344 19.1571 9.87827 20 12 20ZM9.7 11.3L11 12.59L14.3 9.29C14.4924 9.12744 14.7392 9.0435 14.9908 9.05496C15.2425 9.06643 15.4805 9.17246 15.6574 9.35185C15.8343 9.53125 15.9369 9.77078 15.9448 10.0226C15.9527 10.2744 15.8653 10.5199 15.7 10.71L11.7 14.71C11.5131 14.8932 11.2618 14.9959 11 14.9959C10.7382 14.9959 10.4869 14.8932 10.3 14.71L8.3 12.71C8.13472 12.5199 8.04729 12.2744 8.05519 12.0226C8.06309 11.7708 8.16573 11.5312 8.34259 11.3519C8.51946 11.1725 8.75752 11.0664 9.00918 11.055C9.26084 11.0435 9.50755 11.1274 9.7 11.29V11.3Z"
                    fill="#FDD231"
                  />
                </svg>
                {{ service }}
              </li>
            </ul>
            <button
              class="border-2 border-white text-white text-lg p-4 mt-8"
            >See more of my skills & capabilities &rightarrow;</button>
          </div>
        </div>

        <div class="-mr-24">
          <div class="relative p-2">
            <div
              class="absolute z-10 h-full w-full -mr-8 -mt-8 right-0 border-4 border-white"
            >&nbsp;</div>
            <div
              class="absolute try-position bottom-0 h-full w-full bg-yellow-brand -ml-8 -mb-8 left-0"
            >&nbsp;</div>
            <g-image src="~/me.jpg" class="relative z-30 max-w-md" />
          </div>
        </div>
      </div>
    </section>

    <section class="bg-black flex items-center justify-center">
      <div class="container rounded bg-yellow-brand p-8 relative">
        <h3 class="text-5xl font-black">Don't wait until its too late</h3>
        <p>A brief by consise description about the value I can provide people</p>

        <button class="bg-black text-white text-lg rounded p-4 mt-8">Call to action &rightarrow;</button>

        <g-image
          src="~/me.jpg"
          class="absolute right-0 mr-8 border-4 border-black z-30 w-24 h-24 rounded-full"
        />
      </div>
    </section>

    <section class="bg-black text-white text-xl py-64">
      <div class="container mx-auto flex flex-col items-center">
        <Accordion title="FAQ?" :items="frequentlyAskedQuestions" />

        <button
          class="border-2 border-white text-white text-lg p-4"
        >You could ask me anything &rightarrow;</button>
      </div>
    </section>

    <section class="bg-black text-white pb-64 relative">
      <div class="container mx-auto">
        <div class="flex pr-24 mb-32">
          <g-image src="~/dotted-trianlge.svg" class="mr-4 -ml-Hello kuda32" />
          <div class>
            <h1 class="text-5xl font-black">What people say about me</h1>
            <p class="text-2xl">Some people really say nice things about me you know.</p>
          </div>
        </div>
      </div>
      <div class="testimonials-block">
        <div class="animation">
          <div class="flex">
            <div
              v-for="i in 10"
              :key="i"
              class="testimonial-card w-full max-w-sm min-w-sm bg-white pt-16 px-8 text-gray-800 text-xl mr-6"
            >
              <p class="mb-2">He is an awesome developer and a fun human in general</p>
              <p class="mb-2">I am continually mind blown by the stuff he puts out.</p>

              <div class="-mb-10 relative z-30">
                <div class="h-20 w-20 rounded-full border-4 border-white bg-black">&nbsp;</div>
              </div>
              <div class="-mx-8 bg-gray-200 p-8 pt-12 relative">
                <div class="flex items-center justify-between">
                  <p>Scooby McDoo</p>
                  <p class="text-sm">Chief Technology Officer</p>
                </div>

                <div class="flex items-center justify-between text-right">
                  <a href="https://twitter.com/scooby" class="text-sm text-indigo-600">@scooby</a>
                  <a href="https://dooscooby.com" class="text-sm text-indigo-600">dooscooby.com</a>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>
  </Layout>
</template>

<script>
import Accordion from "@/components/Accordion";
export default {
  metaInfo: {
    title: "Hello, world!"
  },

  components: {
    Accordion
  },

  data() {
    return {
      shownDescription: null,
      services: ["Design", "Programming", "Consulting", "Talks", "Trainings"],

      frequentlyAskedQuestions: [
        {
          title: "How much do your services cost?",
          description: `
            It depends!

            Most projects range from  USD $999  to USD $10,000 depending on the complexity and scope of the project. Usually after each project there is a monthly fee of about USD $199 for maintainance and minor updates.

            Any major features to be introduced after wards will be billed as a seperate project and the amount is subject to negotiation. 
          `
        },
        {
          title: "How much do your services cost?",
          description: `
            It depends!

            Most projects range from  USD $999  to USD $10,000 depending on the complexity and scope of the project. Usually after each project there is a monthly fee of about USD $199 for maintainance and minor updates.

            Any major features to be introduced after wards will be billed as a seperate project and the amount is subject to negotiation. 
          `
        }
      ]
    };
  },

  methods: {
    showDescriptionFor(i) {
      this.shownDescription = i;
    },

    hideDescription() {
      this.shownDescription = null;
    }
  }
};
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
  background-image: linear-gradient(#fdd231, #fdd2310a);
}

.center-absolute {
  width: calc(100% - 2rem);
  height: calc(100% - 2rem);
}

.bg-transparent-black {
  background-color: rgba(255, 255, 255, 0.1);
}

.faq-body {
  height: 0;
  overflow: hidden;
  animation: transition max-height 0.3s;
}
.faq-body--open {
  max-height: 500px;
  transition: max-height 0.25s ease-in;
}

.testimonial-card {
  background-image: url("/callout.svg");
  background-repeat: no-repeat;
  background-position: top left;
}

/* testimonial animation experiments */
@keyframes animatedBackground {
  from {
    left: 0px;
  }
  50% {
    left: -100%;
  }
  100% {
    left: 0px;
  }
}
.testimonials-block {
  width: 100%;
  padding: 1rem;
  overflow-y: hidden;
}

.animation {
  width: 100%;
  position: relative;
  animation: animatedBackground 160s linear infinite;
}
</style>
