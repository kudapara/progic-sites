<template>
  <Layout>
    <section class="text-black bg-black relative">
      <div class="pt-12 sm:pt-24 container mx-auto flex justify-between flex-wrap">
        <div class="px-4 sm:px-0">
          <h1 class="font-serif text-white font-black text-4xl max-w-xl">
            Without an online presence,
            <br />does your brand even exist?
          </h1>

          <a href="#services" class="inline-block  text-center bg-yellow-brand text-black py-4 px-8 rounded font-medium mt-8">Get in touch</a>
        </div>

        <g-image src="~/showcase.png" width="600px"
          class="mt-8 sm:mt-0"
          style=" margin-bottom: -100px; box-shadow: 40px 40px 40px rgba(0, 0, 0, 0.25);"></g-image>
      </div>
    </section>

    <section id="why-progic" class="pt-48 pb-16 sm:py-32 container mx-auto px-4 sm:px-0">
      <h3 class="font-serif font-black text-3xl max-w-xl">
        You'll be delighted if we work together
        <br />
        <span class="text-2xl text-gray-700">because you get...</span>
      </h3>

      <div class="flex justify-between mt-6 sm:mt-16 flex-wrap ">
        <div v-for="why in theWhys" :key="why.tag" class="bg-black p-6 text-white max-w-sm relative overflow-hidden mt-8 sm:mt-0">
          <div class="absolute h-64 w-64 bg-yellow-brand-15 top-0 right-0 -mr-32 -mt-32 rounded-full">
            <span v-html="why.logoHTML"></span>
          </div>
          <div class="flex flex-col justify-between h-full">
            <div>
              <span
                class="inline-block bg-indigo-700-25 text-indigo-400 p-4 uppercase tracking-wide">{{ why.tag }}</span>

              <h4 class="font-serif text-2xl mt-8 mb-4">{{ why.title }}</h4>
              <p>{{ why.description }}</p>
            </div>
            <a href="#services" class="inline-block  text-center bg-yellow-brand text-black py-4 px-8 rounded font-medium mt-8">Get in touch</a>
          </div>
        </div>
      </div>
    </section>

    <section id="showcase" class="bg-black text-white px-4 sm:px-0 py-16 sm:pt-32 sm:pb-64">
      <div class="container mx-auto">
        <h3 class="font-serif font-black text-3xl max-w-xl">
          What if your website looked like these
          <br />
          <span class="text-2xl text-gray-200">... or better?</span>
        </h3>

        <div class="flex items-start justify-between mt-16 flex-wrap">
          <div class="bg-indigo-600 p-0 sm:p-4 -mx-4 sm:mx-0">
            <g-image src="~/progic-website.png" width="600px"></g-image>
          </div>

          <div class="max-w-lg">
            <h4 class="font-serif font-black text-3xl mb-4">Progic</h4>
            <span class="inline-block bg-indigo-700-25 text-indigo-400 p-4 uppercase tracking-wide mr-4 mt-2">Website
              development</span>
            <span class="inline-block bg-indigo-700-25 text-indigo-400 p-4 uppercase tracking-wide mt-2">Branding</span>

            <p class="mt-8">Progic is the new startup dyfying the standards of creating knock off websites and
              webaplications. It focuses on creating premium quality websites and applications that aim to solve
              specific business cases.</p>

            <p class="mt-4">We designed progic.co from scratch to showcase our design and development skills, now
              reputable brands such as yours are browsing the site and enjoying the view.</p>

            <div class="max-w-sm border-t-4 border-indigo-700 bg-white text-black p-4 mt-8">
              <p>Not to toot our own horn, I think the team did an incredible job at developing this site. I would
                definatly recommend all forward thinking companies to get work with us.</p>

              <div class="bg-gray-200 -mx-4 -mb-4 p-4 mt-4 flex items-center">
                <g-image src="~/me.jpg" class="h-12 w-12 rounded-full mr-4 shadow-inner"></g-image>
                <div class="flex flex-col">
                  <span>Kudakwashe Paradzayi</span>
                  <span class="text-sm text-gray-700">CEO, Progic</span>
                </div>
              </div>
            </div>

            <a href="#services" class="inline-block  text-center bg-yellow-brand text-black py-4 px-8 rounded font-medium mt-8 max-w-sm w-full">Get in
              touch</a>
          </div>
        </div>

        <div class="flex items-start justify-between mt-32 flex-wrap">
          <div class="bg-indigo-600 overflow-hidden sm:overflow-auto sm:order-1 p-0 sm:p-4 -mx-4 sm:mx-0">
            <div class="scroll-bg-shadow z-50 relative">
              <div class="container overflow-hidden relative" style="height: 600px; width: 600px;">
                <div class="sliding-background absolute"></div>
              </div>
            </div>
          </div>

          <div class="max-w-lg order-0">
            <h4 class="font-serif font-black text-3xl mb-4">Your company</h4>
            <span class="inline-block bg-indigo-700-25 text-indigo-400 p-4 uppercase tracking-wide mr-4 mt-2">Website
              development</span>
            <span class="inline-block bg-indigo-700-25 text-indigo-400 p-4 uppercase tracking-wide mt-2">Branding</span>

            <p class="mt-8">Your company is the industry standard but it is lagging behind because you either have no
              website or the one you have is outdated and gets abandoned by customers everytime they visit.</p>

            <p class="mt-4">You’d be realising more revenue if only your website truly showed off the value you provide
              to your customers.</p>

            <p class="mt-4">But we can help fix that! One day when we satify you you'll give us a testimonial along
              these lines 👇🏽👇🏽👇🏽.</p>

            <div class="max-w-sm border-t-4 border-indigo-700 bg-white text-black p-4 mt-8">
              <p>I trusted my gut and went with Progic. I was never dissapointed. shout out to their creative team. They
                are the best!!</p>

              <div class="bg-gray-200 -mx-4 -mb-4 p-4 mt-4 flex items-center">
                <g-image src="~/me.jpg" class="h-12 w-12 rounded-full mr-4 shadow-inner"></g-image>
                <div class="flex flex-col">
                  <span>You, yes you</span>
                  <span class="text-sm text-gray-700">Staff, Your company</span>
                </div>
              </div>
            </div>

            <a href="#services" class="inline-block  text-center bg-yellow-brand text-black py-4 px-8 rounded font-medium mt-8 max-w-sm w-full">Get in
              touch</a>
          </div>
        </div>
      </div>
    </section>
    <section id="services" class="container mx-auto flex items-center justify-center py-32 text-base"
      style="margin-top: -15%">
      <!-- pt-32 to compensate for the lost padding above-->
      <div class="w-full bg-white text-black px-4 sm:p-8 relative">
        <h3 class="text-3xl font-black font-serif">We could build something great, together</h3>

        <!-- <label for class="block text-xl font-black mb-4">Select the packages that suite your needs</label> -->
        <form name="projects" netlify netlify-honeypot="bot-field" hidden>
          <input type="hidden" name="form-name" value="projects" />
          <input type="checkbox" name="selectedPackages" />
          <input type="text" name="name" />
          <input type="text" name="company_name" />
          <input type="url" name="company_website" />
          <textarea name="project_description"></textarea>
          <input type="text" name="email" />
        </form>
        <form name="projects" method="POST" netlify-honeypot="bot-field" data-netlify="true">
          <input type="hidden" name="form-name" value="projects" />
          <p class="py-4 max-w-xl">
            Every company is unique. Choose the plan that truly captures the needs of your company and fill in the form
            that apears below. We will get back to you with a quotation.
          </p>
          <p class="mb-4 max-w-xl">
            Please note that these prices are starting prices and may vary with the scope of the projects. All prices
            are in United States Dollar (USD).
          </p>
          <div class="flex justify-center flex-wrap  -mx-4">
            <div v-for="plan in plans" :key="plan.code" class=" w-full sm:w-1/3 sm:p-2 p-4">
              <div
              :class="{
                'border-black': selectedPackages.includes(plan.code),
                'bg-black': selectedPackages.includes(plan.code),
                'text-white': selectedPackages.includes(plan.code),
                'shadow-xl': selectedPackages.includes(plan.code)
              }" @click="toggleSelectedPackages(plan.code)"
              class="flex flex-col justify-between  border-4 hover:bg-gray-200 hover:cursor-pointer hover:text-black rounded  h-full p-4 sm:p-8">
                <div>
                  <div class="flex justify-center -mt-8 sm:-mt-12 relative" v-show="plan.isMostPopular">
                    <div class="span px-6 bg-yellow-brand uppercase text-black border-4 rounded" :class="{
                'border-white': selectedPackages.includes(plan.code)
                }">most popular</div>
                  </div>
                  <div class="flex items-center justify-between mb-4" :class="{'mt-4': plan.isMostPopular}">
                    <span class="text-3xl font-medium">{{ plan.title }}</span>
                    <input type="checkbox" v-model="selectedPackages" name="selectedPackages" :value="plan.code"
                      class="form-checkbox text-yellow-brand h-8 w-8" />
                  </div>
  
                  <div class="mb-4">{{ plan.description }}</div>
                </div>
                <div>
                  <div class="py-4">
                    <ul>
                      <li class="flex items-center py-1" v-for="feature in plan.features" :key="feature">
                        <svg class="mr-4 h-6 w-6 fill-current" viewBox="0 0 24 24" fill="fill-current"
                          xmlns="http://www.w3.org/2000/svg">
                          <path
                            d="M12 22C9.34784 22 6.8043 20.9464 4.92893 19.0711C3.05357 17.1957 2 14.6522 2 12C2 9.34784 3.05357 6.8043 4.92893 4.92893C6.8043 3.05357 9.34784 2 12 2C14.6522 2 17.1957 3.05357 19.0711 4.92893C20.9464 6.8043 22 9.34784 22 12C22 14.6522 20.9464 17.1957 19.0711 19.0711C17.1957 20.9464 14.6522 22 12 22ZM12 20C14.1217 20 16.1566 19.1571 17.6569 17.6569C19.1571 16.1566 20 14.1217 20 12C20 9.87827 19.1571 7.84344 17.6569 6.34315C16.1566 4.84285 14.1217 4 12 4C9.87827 4 7.84344 4.84285 6.34315 6.34315C4.84285 7.84344 4 9.87827 4 12C4 14.1217 4.84285 16.1566 6.34315 17.6569C7.84344 19.1571 9.87827 20 12 20ZM9.7 11.3L11 12.59L14.3 9.29C14.4924 9.12744 14.7392 9.0435 14.9908 9.05496C15.2425 9.06643 15.4805 9.17246 15.6574 9.35185C15.8343 9.53125 15.9369 9.77078 15.9448 10.0226C15.9527 10.2744 15.8653 10.5199 15.7 10.71L11.7 14.71C11.5131 14.8932 11.2618 14.9959 11 14.9959C10.7382 14.9959 10.4869 14.8932 10.3 14.71L8.3 12.71C8.13472 12.5199 8.04729 12.2744 8.05519 12.0226C8.06309 11.7708 8.16573 11.5312 8.34259 11.3519C8.51946 11.1725 8.75752 11.0664 9.00918 11.055C9.26084 11.0435 9.50755 11.1274 9.7 11.29V11.3Z"
                            fill="text-current" />
                        </svg>
                        {{ feature }}
                      </li>
                    </ul>
                  </div>
                  <div class="flex justify-between">
                    <div>
                      <span class="block text-xs text-gray-600 uppercase">starting from</span>
                      <span class="text-3xl font-black">${{ plan.price }}</span>
                    </div>
  
                    <div class="text-right">
                      <span class="block text-xs text-gray-600 uppercase">Hosting & Maintanance</span>
                      <div v-show="plan.hostingPrice == 0">
                        <span class="text-3xl font-black">FREE</span>
                      </div>
                      <div v-show="plan.hostingPrice > 0">
                        <span class="text-3xl font-black">${{ plan.hostingPrice }}</span>
                        <span class="text-xs uppercase">/month</span>
                      </div>
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </div>
          
          <div class="flex justify-center">
            <div class="px-4 py-2 -mx-4 sm:mx-0 sm:rounded-full bg-yellow-300 text-black sm:inline-flex items-center mt-8">
              <span
                class="inline-flex items-center px-2 bg-yellow-500 uppercase tracking-wide text-xs font-black rounded-full mr-4">
                <span class="text-xl mr-1">✌🏼</span> Bonus
              </span> All plans come with a
              <span class="font-bold underline px-1">free custom domain</span>,
              <span class="font-bold underline px-1">free ssl certificate</span>, and
              <span class="font-bold underline px-1">free hosting</span>  for the first month.
            </div>
          </div>

          <!-- Input section -->
          <div :class="{
            'hidden': !selectedPackages.includes('design') && !selectedPackages.includes('basic') && !selectedPackages.includes('rich') && !selectedPackages.includes('webapp')
          }">
            <div class="mt-8">
              <h3 class="text-xl font-black mb-4">Briefly Describe your Project</h3>
              <div class="flex mb-4 flex-wrap ">
                <div class="mr-4 w-full sm:w-auto">
                  <label for class="block font-bold uppercase mb-2">Your Name</label>
                  <input required type="text" autofocus name="name" class="mb-4 w-full sm:w-auto form-input border-black border-2"
                    placeholder="e.g John Doe" />
                </div>

                <div class="mr-4 w-full sm:w-auto">
                  <label for class="block font-bold uppercase mb-2">Company Name</label>
                  <input required type="text" name="company_name" class="mb-4 w-full sm:w-auto form-input border-black border-2"
                    placeholder="e.g Progic Private Limited" />
                </div>

                <div class="mr-4 w-full sm:w-auto">
                  <label for class="block font-bold uppercase mb-2">Company Website</label>
                  <input type="url" name="company_website" class="mb-4 w-full sm:w-auto form-input border-black border-2"
                    placeholder="e.g https://progic.co" />
                </div>
              </div>
            </div>
            <div class="pr-4 mb-4">
              <label for class="block font-bold uppercase mb-2">Project Description</label>
              <textarea required name="project_description" class="form-textarea h-32 w-full border-black border-2"></textarea>
            </div>

            <label for class="block font-bold uppercase mb-2">Email address</label>
            <div class="bg-white p-4 flex items-center flex-wrap sm:flex-no-wrap rounded border-2 border-black mr-4">
              <input type="text" required name="email" class="flex-1 p-4 outline-none text-black"
                placeholder="Your email address" />
              <button type="submit"
                class="bg-yellow-brand text-black hover:shadow-md text-lg whitespace-no-wrap w-full sm:w-auto py-2  sm:py-4 px-4 sm:px-16 font-bold rounded">Choose Package(s)
                &rightarrow;</button>
            </div>
          </div>
        </form>
      </div>
    </section>

    <section id="get-in-touch" class="pt-32 bg-black text-white px-4 sm:px-0">
      <div class="container mx-auto pb-32 mb-8 sm:mb-32 border-b">
        <div class="flex justify-between flex-wrap">
          <div class="sm:w-1/2 flex flex-col justify-between">
            <div>
              <h3 class="font-serif font-black text-3xl">
                We're humans too
                <br />
                <span class="text-2xl text-gray-200">Let's talk</span>
              </h3>

              <p class="mt-16">
                If you are convinced that we are the best agency to bring your
                digital presence to the next level, get in touch with us.
                We are available on all main media platforms and our friendly
                team will get to you as soon as humanely possible.
              </p>
            </div>

            <div class="flex flex-wrap max-w-sm mt-8">
              <div class="border-b border-r border-white w-1/2">
                <h5 class="font-serif font-bold text-xl">Email</h5>
                <span class="inline-block my-4">hey@progic.co</span>
              </div>
              <div class="border-b border-white w-1/2 text-right">
                <h5 class="font-serif font-bold text-xl">Twitter</h5>
                <span class="inline-block my-4">@ProgicHQ</span>
              </div>
              <div class="border-r border-white w-1/2 pt-4">
                <h5 class="font-serif font-bold text-xl">Phone</h5>
                <span class="inline-block my-4">+263 785 274 391</span>
              </div>
              <div class="w-1/2 text-right">
                <h5 class="font-serif font-bold text-xl pt-4">Website</h5>
                <span class="inline-block my-4">www.progic.co</span>
              </div>
            </div>
          </div>

          <div class="text-black mt-8 sm:mt-0">
            <div class="bg-white p-4 w-full max-w-md border-t-4 border-indigo-700">
              <form name="contact" netlify>

                <label>
                  <span class="tracking-wide text-sm">What is your name?</span>
                  <input type="text" name="name" class="form-input w-full mt-2 mb-4 border-black border-2" />
                </label>
                <label>
                  <span class="tracking-wide text-sm">What is your company's name?</span>
                  <input type="text" name="company_name" class="form-input w-full mt-2 mb-4 border-black border-2" />
                </label>
                <label>
                  <span class="tracking-wide text-sm">What is your best email address?</span>
                  <input type="text" name="email" class="form-input w-full mt-2 mb-4 border-black border-2" />
                </label>

                <label>
                  <span class="tracking-wide text-sm">What is your message?</span>
                  <textarea id rows="10" name="message" class="form-textarea w-full border-black border-2"></textarea>
                </label>
                <button type="submit" class="bg-yellow-brand text-black py-4 px-8 rounded font-medium mt-8 w-full">Get
                  in touch</button>
              </form>

            </div>
          </div>
        </div>
      </div>

      <div class="container mx-auto flex items-end justify-between flex-wrap pb-8 sm:pb-32  border-b">
        <div>
          <h5 class="font-serif font-bold text-xl">Extras</h5>
          <nav class="flex flex-col mt-8">
            <a href="#" class="mb-4">Why Progic?</a>
            <a href="#" class="mb-4">Services</a>
            <a href="#" class="mb-4">Showcase</a>
            <a href="#" class="mb-4">Get in touch</a>
          </nav>
          <div class="flex mt-8">
            <g-image src="~/progic-logo-light.svg" alt class="mr-8" />
            <g-image src="~/brought-to-you-by-kudapara.svg" alt />
          </div>
        </div>

        <vue-mailchimp-email-signup-form
          class="mt-8 sm:mt-0"
          style="margin-bottom:0"
          :elementId="'first-email-signup-form'"
          :url="'https://progic.us8.list-manage.com/subscribe/post?u=fc1ef1701381304c7ce6dbb0f&amp;id=550879120c'"
          :title="'Subscribe to the Newsletter'"
          :subtitle="'Be the first to know when we release new products, design case studies or technical articles.\n  No spam, we promise.'"/>
      </div>

      <div class="flex items-center justify-center text-center py-8 white">
        <span class="text-left">
          Designed and coded with
        </span>
        <svg fill="currentColor" viewBox="0 0 20 20" class="w-8 h-8 mx-4">
          <path fill-rule="evenodd"
            d="M3.172 5.172a4 4 0 015.656 0L10 6.343l1.172-1.171a4 4 0 115.656 5.656L10 17.657l-6.828-6.829a4 4 0 010-5.656z"
            clip-rule="evenodd"></path>
        </svg>
        <span class="text-right">
          by Progic - <a href="#services" class="underline">Get yours too</a>
        </span>
      </div>
    </section>
  </Layout>
</template>

<script>
  import Accordion from "@/components/Accordion";
  import { VueMailchimpEmailSignupForm } from "vue-mailchimp-email-signup-form";

  export default {
    metaInfo: {
      title: "Progic.co | Premium designs for premium brands"
    },

    components: {
      Accordion,
      VueMailchimpEmailSignupForm
    },

    data() {
      return {
        selectedPackages: [],
        shownDescription: null,
        services: ["Design", "Programming", "Consulting", "Talks", "Trainings"],

        theWhys: [
          {
            tag: "Quality",
            title: "Handcrafted sites & Premium quality",
            description:
              "We put our heart and soul into crafting the perfect site, that will be absolutely stunning to your customers. No knock offs.",
            logoHTML: `<svg fill="none" stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" viewBox="0 0 24 24" class="text-yellow-brand w-8 h-8 absolute bottom-0 left-0 ml-16 mb-16 z-40"><path d="M9 12l2 2 4-4m5.618-4.016A11.955 11.955 0 0112 2.944a11.955 11.955 0 01-8.618 3.04A12.02 12.02 0 003 9c0 5.591 3.824 10.29 9 11.622 5.176-1.332 9-6.03 9-11.622 0-1.042-.133-2.052-.382-3.016z"></path></svg>`
          },
          {
            tag: "Timely",
            title: "Quality work delivered, on time",
            description:
              "Technology moves fast! So we race against time to ensure your site is ready before your competitors, all without compromising quality.",
            logoHTML: `<svg fill="none" stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" viewBox="0 0 24 24" class="text-yellow-brand w-8 h-8 absolute bottom-0 left-0 ml-16 mb-16 z-40"><path d="M12 8v4l3 3m6-3a9 9 0 11-18 0 9 9 0 0118 0z"></path></svg>`
          },
          {
            tag: "Value",
            title: "Value for your money",
            description:
              "Our premium pricing, premium quality. Our promise to you is that you’ll get real value for your money. We throw in a few extras, no cap.",
            logoHTML: `<svg fill="none" stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" viewBox="0 0 24 24" class="text-yellow-brand w-8 h-8 absolute bottom-0 left-0 ml-16 mb-16 z-40"><path d="M12 8c-1.657 0-3 .895-3 2s1.343 2 3 2 3 .895 3 2-1.343 2-3 2m0-8c1.11 0 2.08.402 2.599 1M12 8V7m0 1v8m0 0v1m0-1c-1.11 0-2.08-.402-2.599-1M21 12a9 9 0 11-18 0 9 9 0 0118 0z"></path></svg>`
          }
        ],
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
              "Get hand crafted designs for your website. Build it yourself",
            price: 99,
            hostingPrice: 0,
            features: [
              "Access to original design assets",
              "Maximum of 2 revisions",
              "Get mobile and desktop variations"
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
              "5 standard Pages",
              "Includes design of the website",
              "Website ready in 2 weeks",
              "Maximum of 2 revisions"
            ]
          },
          {
            title: "Rich Websites",
            code: "rich",
            description:
              "Rich interactive websites that allow you to showcase your brand and manage your blog and integrate with social media",
            price: 699,
            isMostPopular: true,
            hostingPrice: 29,
            features: [
              "Up to 10 standard Pages",
              "Includes design of the website",
              "Website ready in 3 weeks",
              "Maximum of 2 revisions",
              "Access to the code repository"
            ]
          },
          {
            title: "Web Applications",
            code: "webapp",
            description:
              "Custom web applications to fulfill the business needs for your company.",
            price: 999,
            hostingPrice: 99,
            features: [
              "Agile development",
              "Custom features",
              "Prototype ready in 3 weeks",
              "Access to the code repository"
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
  .sliding-background {
    background: url("../scroll-bg.png");
    height: 400%;
    width: 400%;
    background-size: 548px auto;
    top: -25%;
    left: -100%;
    animation: slide 15s linear infinite;
  }

  @keyframes slide {
    0% {
      /* transform: translate3d(0, 0, 0); */
      transform: rotate(-13deg) translateY(0%);
    }

    100% {
      /* the y value is half of the height of the image */
      transform: rotate(-13deg) translateY(-437px);
    }
  }

  .bg-indigo-700-25 {
    background-color: #4c52bf70;
  }

  .bg-yellow-brand-15 {
    background-color: #fdd13128;
  }

  .scroll-bg {
    -webkit-animation-name: scrollLarge;
    animation-name: scrollLarge;
    -webkit-animation-duration: 35s;
    animation-duration: 35s;
    -webkit-animation-timing-function: linear;
    animation-timing-function: linear;
    -webkit-animation-iteration-count: infinite;
    animation-iteration-count: infinite;
  }

  @keyframes scrollLarge {
    0% {
      translate: rotate(-12deg);
    }
  }

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

  /* Custom Mailchimp styles */

  .subscribe-container {
    background: #f9fafb;
    border: 1px solid #e6e6e6;
    border-radius: 4px;
    box-shadow: 0 2px 15px 0 rgba(210, 214, 220, 0.3);
    display: flex;
    flex-direction: column;
    font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Oxygen, Ubuntu, Cantarell, "Open Sans", "Helvetica Neue", sans-serif;
    font-size: 16px;
    line-height: 1.5;
    margin-bottom: 2rem;
    max-width: 600px;
    padding: 1.25rem 1rem;
    width: 100%;
  }
  .subscribe-container,
    .subscribe-container * {
      box-sizing: border-box;
  }
  .subscribe-container form {
      margin-bottom: 0;
  }
  .subscribe-container__title {
      @apply font-serif font-bold text-xl;
      color: #000;
      display: inline-block;
      line-height: 1.2;
      margin-bottom: 0.5rem;
  }
  .subscribe-container__subtitle {
      @apply text-xl;
      color: #777;
      padding-bottom: 0;
      margin-block-start: 0;
      margin-bottom: 1rem;
  }
  .subscribe-container__email {
      border-color: #e6e6e6;
      border-radius: 4px;
      color: black;
      font-weight: 400;
      width: 100%;
      background: #fff;
      font-size: 15px;
      padding: 12px;
      border: 1px solid #e6e6e6;
      flex: 1 0 auto;
      line-height: 1.4;
      margin: 0;
      transition: border-color 0.3s ease-out;
      overflow: visible;
      margin-bottom: 1rem;
  }
  .subscribe-container__submit {
      @apply bg-yellow-brand text-black rounded font-medium; 
      border-radius: 8px;
      cursor: pointer;
      font-size: 1.2rem;
      font-weight: 700;
      transition: background-color 0.3s ease-in-out;
      padding: 12px 18px;
      width: 100%;
  }

  .subscribe-container__submit:hover {
    background-color: #dcb629;
  }

</style>
