<template>
  <div class="border-1 p-2 border-zinc-800 bg-neutral-900 flex flex-row justify-evenly items-center gap-4">
    <!-- Date -->
    <div class="text-gray-100 hover:text-gray-700 text-sm animate-pulse">
      {{
        new Date().toLocaleDateString("en-us", {
          weekday: "long",
          year: "numeric",
          month: "long",
          day: "numeric",
        })
      }}
    </div>
    <!-- Discover -->
    <div class="text-gray-100 hover:text-neutral-700 animate-pulse flex flex-row gap-2">
      <h1 class="text-sm">Discover Your Dream Property with estatein</h1>
      <h1 class="underline text-sm">Learn More</h1>
    </div>

    <div>
      <i class="bi bi-x-lg text-xl text-white"></i>
    </div>
  </div>

  <!-- Navbar -->
  <div class="border-1 border-neutral-800 bg-neutral-900 p-3 flex justify-between items-center">
    <!-- Logo -->
    <div class="flex items-center gap-2">
      <i class="bi bi-fire text-3xl text-purple-700"></i>
      <h1 class="text-xl text-zinc-100 mt-2">Estatein</h1>
    </div>

    <!-- Hamburger (Mobile Only) -->
    <div class="lg:hidden">
      <i v-if="!isOpen" @click="isOpen = true" class="bi bi-list text-zinc-100 text-2xl cursor-pointer"></i>
    </div>

    <!-- Desktop Nav -->
    <div class="space-x-5 hidden lg:flex items-center">
      <a href="#" class="text-sm text-white no-underline">Home</a>
      <a href="#" class="text-sm text-white no-underline">About Us</a>
      <a href="#" class="text-sm text-white no-underline bg-zinc-900 rounded-xl p-2 border border-zinc-600">
        Properties
      </a>
      <a href="#" class="text-sm text-white no-underline">Services</a>
    </div>

    <!-- Desktop Contact -->
    <a href="#"
      class="hidden lg:inline text-sm text-white no-underline bg-zinc-900 rounded-xl p-2 border border-zinc-600">
      Contact Us
    </a>
  </div>

  <!-- Right Slide-in Mobile Menu -->
  <transition name="slide">
    <div v-if="isOpen" class="fixed top-0 right-0 w-64 h-full bg-zinc-900 shadow-lg z-50 p-4 lg:hidden">
      <!-- Close Button -->
      <div class="flex justify-end">
        <i @click="isOpen = false" class="bi bi-x text-zinc-100 text-2xl cursor-pointer"></i>
      </div>

      <!-- Mobile Nav Links -->
      <nav class="mt-6 flex flex-col gap-4">
        <a href="#" class="text-zinc-100 hover:text-purple-400">Home</a>
        <a href="#" class="text-zinc-100 hover:text-purple-400">About</a>
        <a href="#" class="text-zinc-100 hover:text-purple-400">Services</a>
        <a href="#" class="text-zinc-100 hover:text-purple-400">Contact</a>
      </nav>
    </div>
  </transition>

  <!-- dream -->
  <div class=" flex flex-col-reverse md:flex-row justify-between bg-neutral-900 border-1 border-neutral-800 w-full p-2">
    <div class="bg-neutral-900 p-14 flex flex-col gap-5 md:gap-3">
      <h1 class="text-5xl text-white ">Discover Your Dream <br> Property with Estatein</h1>
      <h1 class="text-neutral-300 text-sm ">Your Journey to finding the perfect property begins here. Explore our
        listings to find the home
        that matches your dreams.</h1>
      <div class="flex flex-col md:flex-row gap-3">
        <button class="text-white border border-neutral-100 p-2 rounded-lg">Learn More</button>
        <button class="text-white p-2 rounded-lg bg-purple-800">Browse Properties</button>
      </div>
      <div class="grid grid-cols-2 md:grid-cols-3 gap-2">
        <!-- 200k+ -->
        <div class=" bg-neutral-800 border-1 border-neutral-500 p-2 rounded-xl flex flex-col ">
          <i class="text-white text-2xl">200+</i>
          <i class="text-neutral-300 text-sm">Happy Customers</i>
        </div>
        <!-- 100k+ -->
        <div class=" bg-neutral-800 border-1 border-neutral-500 p-2 rounded-xl flex flex-col">
          <i class="text-white text-2xl">10+</i>
          <i class="text-neutral-300 text-sm">Properties for CLients</i>
        </div>
        <!-- 16+ -->
        <div class="col-span-2 md:col-span-1 bg-neutral-800 border-1 border-neutral-500 p-2 rounded-xl flex flex-col">
          <i class="text-white text-2xl">6+</i>
          <i class="text-neutral-300 text-sm">Years of experience</i>
        </div>
        <!-- end -->
      </div>
    </div>
    <img src="/images/logo.png" alt="Logo" loading="lazy" class=" rounded-xl h-[300px] w-[500px] md:h-[500px] md:w-[400px] ">
  </div>
  <!-- some boxes -->
  <div class="grid grid-cols-2 md:grid-cols-4 p-2 gap-3">
    <!-- find -->
    <div class="bg-neutral-800 p-6 rounded-lg shadow-md">
      <i class="bi bi-arrow-up-right flex justify-end text-neutral-500 text-xl"></i>
      <div class="flex flex-col justify-center items-center gap-2">
        <img src="/images/first.png" alt="First" loading="lazy" class=" rounded-xl h-[50px] w-[60px] md:h-[50px] md:w-[50px] ">
        <i class="text-white text-lg">Find Your dream Home</i>
      </div>
    </div>
    <!-- find -->
    <div class="bg-neutral-800 p-6 rounded-lg shadow-md">
      <i class="bi bi-arrow-up-right flex justify-end text-neutral-500 text-xl"></i>
      <div class="flex flex-col justify-center items-center gap-2">
        <img src="/images/second.png" alt="Second" loading="lazy" class=" rounded-xl h-[50px] w-[60px] md:h-[50px] md:w-[50px] ">
        <i class="text-white text-lg">Find Your dream Home</i>
      </div>
    </div>
    <!-- find -->
    <div class="bg-neutral-800 p-6 rounded-lg shadow-md">
      <i class="bi bi-arrow-up-right flex justify-end text-neutral-500 text-xl"></i>
      <div class="flex flex-col justify-center items-center gap-2">
        <img src="/images/third.png" alt="Third" loading="lazy" class=" rounded-xl h-[50px] w-[60px] md:h-[50px] md:w-[50px] ">
        <i class="text-white text-lg">Find Your dream Home</i>
      </div>
    </div>
    <!-- find -->
    <div class="bg-neutral-800 p-6 rounded-lg shadow-md">
      <i class="bi bi-arrow-up-right flex justify-end text-neutral-500 text-xl"></i>
      <div class="flex flex-col justify-center items-center gap-2">
        <img src="/images/fourth.png" alt="Fourth" loading="lazy" class=" rounded-xl h-[50px] w-[60px] md:h-[50px] md:w-[50px] ">
        <i class="text-white text-lg">Find Your dream Home</i>
      </div>
    </div>
    <!-- end -->
  </div>

  <!-- feature -->
  <div class="flex flex-col md:flex-row p-10 gap-3 md:gap-0 justify-between mt-5">
    <div class="">
      <h1 class="text-white">Featured Properties</h1>
      <h2 class="text-neutral-300 text-sm">Explore our handpicked selection of featured properties. Each listing offers
        a glimpse into exceptional homes and investments available
        through Estatein. <br> Click "View Details" for more information.</h2>
    </div>
    <div class="flex items-center">
      <button class="bg-neutral-700 text-white text-xl px-7 h-20 flex items-center rounded-xl"> View all properties
      </button>
    </div>
  </div>

  <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3">
    <!-- images details div -->
    <div class="p-8 rounded-lg flex flex-col md:flex-row">
      <div class="p-2 gap-3 border-1 border-neutral-700 rounded-lg flex flex-col">
        <img src="/images/first-1.png" alt="First-1" loading="lazy" class=" rounded-xl h-[200px] w-[400px] md:h-[300px] md:w-[300px] ">
        <h1 class="text-white text-sm">Seaside Serenity Villa</h1>
        <h2 class="text-white text-sm">A stunning 4-bedroom, 3-bathroom villa in a peaceful suburban neighborhood...
          Read More</h2>
        <div class="grid grid-cols-2 gap-3">
          <div class="bg-neutral-700 text-white text-sm p-2 h-10 rounded-xl flex flex-row gap-2">
            <i class="bi bi-box2-heart text-2xl flex items-center"></i>
            <h1 class="text-xs mt-1">4-Bedroom</h1>
          </div>
          <!-- bathroom -->
          <div class="bg-neutral-700 text-white text-sm p-2 h-10 rounded-xl flex flex-row gap-2">
            <i class="bi bi-truck-flatbed text-2xl flex items-center"></i>
            <h1 class="text-xs mt-1">3-Bathroom</h1>
          </div>
          <!-- villa -->
          <div
            class="col-span-2 md:col-span-1 bg-neutral-700 text-white text-sm p-2 h-10 rounded-xl flex flex-row gap-2">
            <i class="bi bi-bookmark-heart text-2xl flex items-center"></i>
            <h1 class="text-sm mb-5">Villa</h1>
          </div>
        </div>
        <!-- price -->
        <div class="flex flex-row gap-3 justify-between">
          <div class="flex flex-col">
            <h1 class="text-neutral-700 text-lg">Price</h1>
            <h1 class="text-white text-xl">$550,000</h1>
          </div>
          <div class="bg-purple-700 px-6 md:px-10 py-2 text-white rounded-lg flex items-center justify-center">View
            Property details</div>
        </div>
      </div>
    </div>
    <!-- second -->
    <div class="hidden md:block">
      <div class="p-8 rounded-lg flex flex-col md:flex-row">
        <div class="p-2 gap-3 border-1 border-neutral-700 rounded-lg flex flex-col">
          <img src="/images/second-2.png" alt="Second-2" loading="lazy" class=" rounded-xl h-[200px] w-[400px] md:h-[300px] md:w-[300px] ">
          <h1 class="text-white text-sm">Metropolitan Haven</h1>
          <h2 class="text-white text-sm">A chic and fully-furnished 2-bedroom apartment with panoramic city views...
            Read More</h2>
          <div class="grid grid-cols-2  gap-3">
            <div class="bg-neutral-700 text-white text-sm p-2 h-10 rounded-xl flex flex-row gap-2">
              <i class="bi bi-box2-heart text-2xl flex items-center"></i>
              <h1 class="text-xs mt-1">2-bedroom</h1>
            </div>
            <!-- bathroom -->
            <div class="bg-neutral-700 text-white text-sm p-2 h-10 rounded-xl flex flex-row gap-2">
              <i class="bi bi-truck-flatbed text-2xl flex items-center"></i>
              <h1 class="text-xs mt-1">2-bathroom</h1>
            </div>
            <!-- villa -->
            <div
              class="col-span-2 md:col-span-1 bg-neutral-700 text-white text-sm p-2 h-10 rounded-xl flex flex-row gap-2">
              <i class="bi bi-bookmark-heart text-2xl flex items-center"></i>
              <h1 class="text-sm mb-5">Villa</h1>
            </div>
          </div>
          <!-- price -->
          <div class="flex flex-row gap-3 justify-between">
            <div class="flex flex-col">
              <h1 class="text-neutral-700 text-lg">Price</h1>
              <h1 class="text-white text-xl">$550,000</h1>
            </div>
            <div class="bg-purple-700 px-6 md:px-10 py-2 text-white rounded-lg flex items-center justify-center">View
              Property details</div>
          </div>
        </div>
      </div>
    </div>
    <!-- third -->
    <div class="hidden md:block">
      <div class="p-8 rounded-lg flex flex-col md:flex-row">
        <div class="p-2 gap-3 border-1 border-neutral-700 rounded-lg flex flex-col">
          <img src="/images/third-3.png" alt="Third-3" loading="lazy" class=" rounded-xl h-[200px] w-[400px] md:h-[300px] md:w-[300px] ">
          <h1 class="text-white text-sm">Rustic Retreat Cottage</h1>
          <h2 class="text-white text-sm">An elegant 3-bedroom, 2.5-bathroom townhouse in a gated community... Read More
          </h2>
          <div class="grid grid-cols-2 gap-3">
            <div class="bg-neutral-700 text-white text-sm p-2 h-10 rounded-xl flex flex-row gap-2">
              <i class="bi bi-box2-heart text-2xl flex items-center"></i>
              <h1 class="text-xs mt-1">3-bedroom</h1>
            </div>
            <!-- bathroom -->
            <div class="bg-neutral-700 text-white text-sm p-2 h-10 rounded-xl flex flex-row gap-2">
              <i class="bi bi-truck-flatbed text-2xl flex items-center"></i>
              <h1 class="text-xs flex items-center mt-1">3-bathroom</h1>
            </div>
            <!-- villa -->
            <div
              class="col-span-2 md:col-span-1 bg-neutral-700 text-white text-sm p-2 h-10 rounded-xl flex flex-row gap-2">
              <i class="bi bi-bookmark-heart text-2xl flex items-center"></i>
              <h1 class="text-sm mb-5">Villa</h1>
            </div>
          </div>
          <!-- price -->
          <div class="flex flex-row gap-3 justify-between">
            <div class="flex flex-col">
              <h1 class="text-neutral-700 text-lg">Price</h1>
              <h1 class="text-white text-xl">$550,000</h1>
            </div>
            <div class="bg-purple-700 px-6 md:px-10 py-2 text-white rounded-lg flex items-center justify-center">View
              Property details</div>
          </div>
        </div>
      </div>
    </div>
  </div>

  <!-- what our clients say -->

  <div class="flex flex-col md:flex-row justify-between p-6 mt-5">
    <div class="flex flex-col">
      <h1 class="text-white">What Our clients say</h1>
      <h2 class="text-neutral-500 text-sm">Road to sucess stores and hertfelts testimonials from our valued clients.
        Discover why they chose Estatein for their real estate needs.</h2>
    </div>
    <div class="flex items-center">
      <button class="bg-neutral-700 text-white text-xl px-7 h-20 flex items-center rounded-xl"> View all Testimonials
      </button>
    </div>
  </div>

  <!-- reviews -->
  <div class="p-6 grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 gap-3">
    <div class="border-1 rounded-lg p-4 border-neutral-700 flex flex-col gap-3 ">
      <div class="flex flex-row gap-3">
        <i class="bi bi-star-fill text-xl text-yellow-500"></i>
        <i class="bi bi-star-fill text-xl text-yellow-500"></i>
        <i class="bi bi-star-fill text-xl text-yellow-500"></i>
        <i class="bi bi-star-fill text-xl text-yellow-500"></i>
        <i class="bi bi-star-fill text-xl text-yellow-500"></i>
      </div>
      <h1 class="text-xl text-white">Exceptional Service!</h1>
      <h1 class="text-lg text-white">Our experience with Estatein was outstanding Their team's dedication and
        professionalism made finding our dream home a breeze. Highly recommended!</h1>
      <div class="flex flex-row gap-2">
        <img src="/images/stars.png" alt="Stars" loading="lazy" class="h-[50px] w-[50px] rounded-full">
        <div class="flex flex-col">
          <h1 class="text-sm text-white ">Wade Warren</h1>
          <h1 class="text-sm text-neutral-500">USA, California</h1>
        </div>
      </div>
    </div>
    <!-- second -->
    <div class="hidden md:block">
      <div class="border-1 rounded-lg p-4 border-neutral-700 flex flex-col gap-3">
        <div class="flex flex-row gap-3">
          <i class="bi bi-star-fill text-xl text-yellow-500"></i>
          <i class="bi bi-star-fill text-xl text-yellow-500"></i>
          <i class="bi bi-star-fill text-xl text-yellow-500"></i>
          <i class="bi bi-star-fill text-xl text-yellow-500"></i>
          <i class="bi bi-star-fill text-xl text-yellow-500"></i>
        </div>
        <h1 class="text-xl text-white">Efficient and reliable!</h1>
        <h1 class="text-lg text-white">Estatein provided us with top-notch service they helped us sell our property
          quickly and at a great price. We coudnlt be happier with the results</h1>
        <div class="flex flex-row gap-2">
          <img src="/images/stars.png" alt="Stars" loading="lazy" class="h-[50px] w-[50px] rounded-full">
          <div class="flex flex-col">
            <h1 class="text-sm text-white ">Emelie Thomson</h1>
            <h1 class="text-sm text-neutral-500">USA, Florida</h1>
          </div>
        </div>
      </div>
    </div>
    <!-- third -->
    <div class="hidden md:block">
      <div class="border-1 rounded-lg p-4 border-neutral-700 flex flex-col gap-3 ">
        <div class="flex flex-row gap-3">
          <i class="bi bi-star-fill text-xl text-yellow-500"></i>
          <i class="bi bi-star-fill text-xl text-yellow-500"></i>
          <i class="bi bi-star-fill text-xl text-yellow-500"></i>
          <i class="bi bi-star-fill text-xl text-yellow-500"></i>
          <i class="bi bi-star-fill text-xl text-yellow-500"></i>
        </div>
        <h1 class="text-xl text-white">Trusted Advisors</h1>
        <h1 class="text-lg text-white">The Estatein team guided us through the entire buying process. Their knowledge
          and commitment to our needs were impressive. Thank you for your support!</h1>
        <div class="flex flex-row gap-2">
          <img src="/images/stars.png" alt="Stars" loading="lazy" class="h-[50px] w-[50px] rounded-full">
          <div class="flex flex-col">
            <h1 class="text-sm text-white ">John Mans</h1>
            <h1 class="text-sm text-neutral-500">USA, Nevada</h1>
          </div>
        </div>
      </div>
    </div>
  </div>

  <!-- frequently asked questions -->
  <div class="flex flex-col md:flex-row justify-between p-6 mt-5">
    <div class="flex flex-col">
      <h1 class="text-white">Frequently Asked Questions</h1>
      <h2 class="text-neutral-500 text-sm">Find answers to common questions about Estatein services property listings
        and the real estate process We're here to provide clarity and assist you every step of the way.</h2>
    </div>
    <div class="flex items-center">
      <button class="bg-neutral-700 text-white text-xl px-7 h-20 flex items-center rounded-xl"> View all FAQ'S
      </button>
    </div>
  </div>

  <!-- how -->
  <div class="p-6 grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 gap-3">
    <div class="border-1 rounded-lg p-4 border-neutral-700 flex flex-col gap-3 ">
      <h1 class="text-2xl text-white">How do i search for Properties on Estatein?</h1>
      <h1 class="text-lg text-white">Learn how to use our user friendly search tools to find properties that match your
        criteria</h1>
      <button class="text-white text-lg bg-neutral-800 p-2 rounded-lg w-[150px]">Read More</button>
    </div>
    <!-- skjs -->
    <div class="hidden md:block">
      <div class="border-1 rounded-lg p-4 border-neutral-700 flex flex-col gap-3">
        <h1 class="text-2xl text-white">What documents do i need to sell my property through Estatein</h1>
        <h1 class="text-lg text-white">Find out about the necessary documentation for listing your property with us.
        </h1>
        <button class="text-white text-lg bg-neutral-800 p-2 rounded-lg w-[150px]">Read More</button>
      </div>
    </div>

    <!-- skjs -->
    <div class="hidden md:block">
      <div class="border-1 rounded-lg p-4 border-neutral-700 flex flex-col gap-3">
        <h1 class="text-2xl text-white">What documents do i need to sell my property through Estatein</h1>
        <h1 class="text-lg text-white">Find out about the necessary documentation for listing your property with us.
        </h1>
        <button class="text-white text-lg bg-neutral-800 p-2 rounded-lg w-[150px]">Read More</button>
      </div>
    </div>
  </div>

  <!-- start -->

  <div class="flex flex-col md:flex-row justify-between p-6 mt-5 gap-3">
    <div class="flex flex-col">
      <h1 class="text-white">Start Your Real Estate Journey Today</h1>
      <h2 class="text-neutral-500 text-sm">Your dream property is just a click away. Whether you're looking for a new
        home, a strategic investment or export real estate advice. <br>
        Estatein is here to assist you every step of the way. take the first step towards you real estate goals and
        explore our available properties <br>
        or get in touch with our team for personalized assistance. </h2>
    </div>
    <div class="flex items-center">
      <button class="bg-purple-700 text-white text-xl px-7 h-20 flex items-center rounded-xl"> Explore Properties
      </button>
    </div>
  </div>


  <!-- Logo -->
 <div class="p-6 grid grid-cols-2 md:grid-cols-7 gap-16">
  <!-- Move this block to the top of HTML -->
  <div class="flex flex-col gap-3 col-span-2 md:col-span-2">
    <div class="flex flex-row gap-1">
        <i class="bi bi-fire text-3xl text-purple-700"></i>
        <h1 class="text-xl text-zinc-100 mt-2">Estatein</h1>
      </div>
      <div class=" bg-neutral-900 border-1 border-neutral-700 rounded-lg flex flex-row items-center justify-center p-1">
        <i class="bi bi-envelope text-neutral-300 text-xl block md:hidden"></i>
        <input class="text-neutral-700 bg-neutral-900 rounded-lg p-3 w-full sm:w-3/4 md:w-1/2 lg:w-1/3 xl:w-1/4"
          type="text" placeholder="Enter your email">

        <i class="bi bi-send-fill text-white text-xl block md:hidden"></i>
      </div>
    </div>
    <div>
      <h1 class="text-xl text-neutral-700">Home</h1>
      <h1 class="text-xl text-white">Hero Section</h1>
      <h1 class="text-xl text-white">Features</h1>
      <h1 class="text-xl text-white">Properties</h1>
      <h1 class="text-xl text-white">Testimonials</h1>
      <h1 class="text-xl text-white">FAQ's</h1>
    </div>
    <div>
      <h1 class="text-xl text-neutral-700">About Us</h1>
      <h1 class="text-xl text-white">Our Story</h1>
      <h1 class="text-xl text-white">Our Works</h1>
      <h1 class="text-xl text-white">How it Works</h1>
      <h1 class="text-xl text-white">Our Team</h1>
      <h1 class="text-xl text-white">Our Clients</h1>
    </div>
    <div>
      <h1 class="text-xl text-neutral-700">Properties</h1>
      <h1 class="text-xl text-white">Portfolio</h1>
      <h1 class="text-xl text-white">Categories</h1>
    </div>
    <div>
      <h1 class="text-xl text-neutral-700">Services</h1>
      <h1 class="text-xl text-white">Valuation Mastery</h1>
      <h1 class="text-xl text-white">Strategic Marketing </h1>
      <h1 class="text-xl text-white">Negotiation Wizardy </h1>
      <h1 class="text-xl text-white">Closing Success </h1>
      <h1 class="text-xl text-white">Property Management </h1>
    </div>
    <div>
      <h1 class="text-xl text-neutral-700">Contact Us</h1>
      <h1 class="text-xl text-white">Contact Form</h1>
      <h1 class="text-xl text-white">Our Offices</h1>
    </div>
  </div>
</template>

<script setup>
import { ref } from "vue";

const isOpen = ref(false);
</script>

<style scoped>
/* Slide in from the right */
.slide-enter-active,
.slide-leave-active {
  transition: transform 0.3s ease;
}

.slide-enter-from,
.slide-leave-to {
  transform: translateX(100%);
}

.slide-enter-to,
.slide-leave-from {
  transform: translateX(0%);
}
</style>
