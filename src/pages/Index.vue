<template>
  <Layout>
    <section class="text-black py-32 relative">
      <div class="pt-64 container mx-auto">
      <div class>
        <h1 class="text-6xl font-black text-white">Portfolio</h1>
        <p class="text-lg">See what I have created in the past and enjoy yourself!</p>
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
            <!--<button
              class="border-2 border-white text-white text-lg p-4"
            >See more of my work &rightarrow;</button>-->
          </div>
        </div>
      </div>
    </section>

    <section class="text-white pt-64 pb-32 relative">
      <div class="container mx-auto flex justify-between">
        <div>
          <div class>
            <h1 class="text-6xl font-black">This is what I do</h1>
            <p
              class="text-2xl max-w-xl mb-8"
            >This is my pitch.What I can do for you. I am selling myself to you, my potential client.</p>
          </div>

          <div class="">
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
            <div class="absolute z-10 h-full w-full -mr-8 mt-8 right-0 border-4 border-white">&nbsp;</div>
            <div
              class="absolute z-20 try-position bottom-0 h-full w-full bg-yellow-brand -ml-8 -mb-16 left-0"
            >&nbsp;</div>
            <g-image src="~/me.jpg" class="relative z-30 max-w-md mt-24" />
          </div>
        </div>
      </div>
    </section>

    <section id="apply-for-work" class="flex items-center justify-center pt-32"> <!-- pt-32 to compensate for the lost padding above-->
      <div class="w-full bg-white text-black p-8 relative">
        <h3 class="text-5xl font-black">We could build something great, together</h3>

        <label for class="block text-xl font-black mb-4">Select the packages that suite your needs</label>
        <p class="py-4">Every company is unique. </p>
        <div class="flex justify-start">
          <div
            v-for="plan in plans"
            :key="plan.code"
            class="flex flex-col justify-between hover:bg-gray-200 hover:cursor-pointer hover:text-black border-4 rounded max-w-sm min-w-sm p-8 mr-4"
            :class="{
              'border-black': selectedPackages.includes(plan.code),
              'bg-black': selectedPackages.includes(plan.code),
              'text-white': selectedPackages.includes(plan.code),
              'shadow-xl': selectedPackages.includes(plan.code)
            }"
            @click="toggleSelectedPackages(plan.code)"
          >

            <div class="flex justify-center -mt-12" v-if="plan.isMostPopular">
              <div class="span px-6 bg-yellow-brand uppercase text-black border-4 rounded "
              :class="{
              'border-white': selectedPackages.includes(plan.code)
              }"
              >most popular</div>
            </div>
            <div>
              <div class="flex items-center justify-between mb-4">
                <span class="text-3xl font-medium">{{ plan.title }}</span>
                <input
                  type="checkbox"
                  v-model="selectedPackages"
                  name
                  :value="plan.code"
                  id
                  class="form-checkbox text-yellow-brand h-8 w-8"
                />
              </div>

              <div class="mb-4">
                {{ plan.description }}
                <div class="py-4">
                  <ul>
                    <li
                      class="flex items-center py-1"
                      v-for="feature in plan.features"
                      :key="feature"
                    >
                      <svg
                        class="mr-4 h-6 w-6 fill-current"
                        viewBox="0 0 24 24"
                        fill="fill-current"
                        xmlns="http://www.w3.org/2000/svg"
                      >
                        <path
                          d="M12 22C9.34784 22 6.8043 20.9464 4.92893 19.0711C3.05357 17.1957 2 14.6522 2 12C2 9.34784 3.05357 6.8043 4.92893 4.92893C6.8043 3.05357 9.34784 2 12 2C14.6522 2 17.1957 3.05357 19.0711 4.92893C20.9464 6.8043 22 9.34784 22 12C22 14.6522 20.9464 17.1957 19.0711 19.0711C17.1957 20.9464 14.6522 22 12 22ZM12 20C14.1217 20 16.1566 19.1571 17.6569 17.6569C19.1571 16.1566 20 14.1217 20 12C20 9.87827 19.1571 7.84344 17.6569 6.34315C16.1566 4.84285 14.1217 4 12 4C9.87827 4 7.84344 4.84285 6.34315 6.34315C4.84285 7.84344 4 9.87827 4 12C4 14.1217 4.84285 16.1566 6.34315 17.6569C7.84344 19.1571 9.87827 20 12 20ZM9.7 11.3L11 12.59L14.3 9.29C14.4924 9.12744 14.7392 9.0435 14.9908 9.05496C15.2425 9.06643 15.4805 9.17246 15.6574 9.35185C15.8343 9.53125 15.9369 9.77078 15.9448 10.0226C15.9527 10.2744 15.8653 10.5199 15.7 10.71L11.7 14.71C11.5131 14.8932 11.2618 14.9959 11 14.9959C10.7382 14.9959 10.4869 14.8932 10.3 14.71L8.3 12.71C8.13472 12.5199 8.04729 12.2744 8.05519 12.0226C8.06309 11.7708 8.16573 11.5312 8.34259 11.3519C8.51946 11.1725 8.75752 11.0664 9.00918 11.055C9.26084 11.0435 9.50755 11.1274 9.7 11.29V11.3Z"
                          fill="text-current"
                        />
                      </svg>
                      {{ feature }}
                    </li>
                  </ul>
                </div>
              </div>
            </div>

            <div class="flex justify-between">
              <div>
                <span class="block text-xs text-gray-600 uppercase">starting from</span>
                <span class="text-3xl font-black">${{ plan.price }}</span>
              </div>

              <div class="text-right">
                <span class="block text-xs text-gray-600 uppercase">Hosting & Maintanance</span>
                <div v-if="plan.hostingPrice == 0">
                  <span  class="text-3xl font-black">FREE</span>
                </div>
                <div v-else>
                  <span class="text-3xl font-black">${{ plan.hostingPrice }}</span>
                  <span class="text-xs uppercase">/month</span>
                </div>
              </div>
            </div>
          </div>
        </div>

        <div
          class="px-4 py-2 rounded-full bg-yellow-300 text-black inline-flex items-center mt-8"
        >
          <span
            class="inline-flex items-center px-2 bg-yellow-500 uppercase tracking-wide text-xs font-black rounded-full mr-4"
          >
            <span class="text-xl mr-1">✌🏼</span> Bonus
          </span> All plans come with a
          <span class="font-bold underline px-1">free custom domain</span>,
          <span class="font-bold underline px-1">free ssl certificate</span>, and
          <span class="font-bold underline px-1">free hosting for the first month</span> .
        </div>

        <!-- Input section -->
        <div
          :class="{
            'hidden': !selectedPackages.includes('design') && !selectedPackages.includes('basic') && !selectedPackages.includes('rich') && !selectedPackages.includes('webapp')
          }"
        >

          <div class="mt-8">
            <h3 class="text-xl font-black mb-4">Briefly Describe your Project</h3>
            <div class="flex mb-4">
              <div class="mr-4">
                <label for="" class="block font-bold uppercase  mb-2">Your Name</label>
                <input type="text" autofocus class="form-input border-black border-2" placeholder="e.g John Doe">
              </div>

              <div class="mr-4">
                <label for="" class="block font-bold uppercase mb-2">Company Name</label>
                <input type="text" class="form-input border-black border-2" placeholder="e.g Progic Private Limited">
              </div>

              <div class="mr-4">
                <label for="" class="block font-bold uppercase mb-2">Company Website</label>
                  <input type="url" class="form-input border-black border-2" placeholder="e.g https://progic.co">
                </div>
              </div>
            </div>
            <div class="pr-4 mb-4">
              <label for="" class="block font-bold uppercase mb-2">Project Description</label>
              <textarea name class="form-textarea w-full border-black border-2" id rows="4"></textarea>
            </div>
        
            <label for="" class="block font-bold uppercase mb-2">Email address</label>
            <div class="bg-white p-4 flex rounded border-2 border-black mr-4">
              <input
                type="text"
                class="flex-1 p-4 outline-none text-black"
                placeholder="Your email address"
              />
              <button
                class="bg-black hover:shadow-md text-white text-lg py-4 px-16 font-bold rounded"
              >Choose Package(s) &rightarrow;</button>
            </div>
          </div>
  

        </div>
    </section>

    <section class="text-white text-xl py-64">
      <div class="container mx-auto flex flex-col items-center">
        <Accordion title="FAQ?" :items="frequentlyAskedQuestions" />

        <button
          class="border-2 border-white text-white text-lg p-4"
        >You could ask me anything &rightarrow;</button>
      </div>
    </section>

    <section class="text-white pb-64 relative">
      <div class="container mx-auto">
        <div class>
          <h1 class="text-6xl font-black">What people say about me</h1>
          <p class="text-2xl mb-8">Some people really say nice things about me you know.</p>
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

    <section class="text-white text-xl pb-32">
      <div class="container mx-auto flex justify-between rounded p-8 relative border-t">
        <div>
          <h3 class="text-2xl font-bold mb-6">Extras</h3>
          <ul>
            <li class="mb-4">Allanite Classified</li>
            <li class="mb-4">School Metrics</li>
            <li class="mb-4">Progic Wallet</li>
            <li class="mb-4">Progic</li>
          </ul>
        </div>

        <div>
          <h3 class="text-2xl font-bold mb-6">Stay in the Loop</h3>
          <p class="mb-2">Be the first to know if there is a new product or I have bought a new dog.</p>

          <p class="mb-4">No spam, I promise.</p>

          <div class="bg-white p-4 flex rounded">
            <input
              type="text"
              class="flex-1 p-4 outline-none text-black"
              placeholder="Your email address"
            />
            <button
              class="bg-yellow-brand hover:shadow-md text-black text-lg py-4 px-16 font-bold rounded"
            >Subscribe</button>
          </div>
        </div>
      </div>

      <div class="container mx-auto p-8 rounded bg-yellow-brand text-center text-black font-medium">
        This website was designed and coded with ❤️ by Kudakwashe Paradzayi -
        <a href="#" class="underline">Get yours too</a>
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
      selectedPackages: [],
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
      ],

      plans: [
        {
          title: "Website Design",
          code: "design",
          description:
            "Static websites, useful when you are just starting out and just want to bring your brand out there",
          price: 99,
          hostingPrice: 0,
          features: [
            "5 Pages",
            "Good Design",
            "Best Development",
            "Custom Domain"
          ]
        },
        {
          title: "Basic Websites",
          code: "basic",
          description:
            "Static websites, useful when you are just starting out and just want to bring your brand out there",
          price: 199,
          hostingPrice: 9,
          features: [
            "5 Pages",
            "Good Design",
            "Best Development",
            "Custom Domain"
          ]
        },
        {
          title: "Rich Websites",
          code: "rich",
          description:
            "Rich interactive websites that allow you to edit rich text, upload media and all",
          price: 699,
          isMostPopular: true,
          hostingPrice: 29,
          features: [
            "5 Pages",
            "Good Design",
            "Best Development",
            "Custom Domain"
          ]
        },
        {
          title: "Web Applications",
          code: "webapp",
          description:
            "Rich interactive websites that allow you to edit rich text, upload media and all",
          price: 999,
          hostingPrice: 99,
          features: [
            "5 Pages",
            "Good Design",
            "Best Development",
            "Custom Domain"
          ]
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
    },

    toggleSelectedPackages(pkg) {
      if (this.selectedPackages.includes(pkg)) {
        this.selectedPackages.splice(this.selectedPackages.indexOf(pkg), 1);
      } else {
        this.selectedPackages.push(pkg);
      }
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
