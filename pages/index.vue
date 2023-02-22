<template>
    <div>
        <section>
            <div class="flex mt-120 h-screen w-full items-center justify-center container mx-auto px-8">
              <div class="max-w-2xl text-center">
                <h1 class="text-3xl sm:text-5xl capitalize tracking-widest text-white lg:text-7xl">CleanWater</h1>

                <p class="mt-6 lg:text-lg text-white">We want you to drink clean water wherever you are</p>

                <div class="mt-8 flex flex-col space-y-3 sm:-mx-2 sm:flex-row sm:justify-center sm:space-y-0">
                
                  <NuxtLink to="/Countries" class="transform rounded-md bg-blue-700 px-8 py-2 text-sm font-medium capitalize tracking-wide text-white transition-colors duration-200 hover:bg-blue-600 focus:bg-blue-600 focus:outline-none sm:mx-2">Check Water Cleanliness</NuxtLink>
                </div>
              </div>
            </div>
        </section>        
    </div>
</template>

<script setup>
    definePageMeta({
        layout: 'index'
    })
</script>