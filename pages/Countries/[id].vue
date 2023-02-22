<template>
    <div>
        <p class="container rounded-xl mt-4 pb-4 pt-4 md:w-50 text-xl text-gray-800 font-semibold bg-blue-400 mx-auto px-4 flex justify-center items-center">Water details for {{ country.countryName }}</p>
    </div>
    <!-- component -->
<div class="relative py-16 bg-gradient-to-br from-sky-50 to-gray-200">  
    <div class="relative container m-auto px-6 text-gray-500 md:px-12 xl:px-40">
        <div class="m-auto md:w-8/12 lg:w-6/12 xl:w-6/12">
            <div class="rounded-xl bg-blue-200 shadow-xl">
                <div class="p-6 sm:p-16">
                    <div class="space-y-4">
                    </div>
                    <div class=" grid space-y-4">
                            <div class="relative flex items-center space-x-4 justify-center">
                                <span class="block w-max font-semibold tracking-wide text-gray-700 text-xl transition duration-300 group-hover:text-blue-600 ">Water quality: {{ country.waterQuality }} </span>
                            </div>
                            <div class="relative flex items-center space-x-4 justify-center">
                                <span class="block w-max font-semibold tracking-wide text-gray-700 text-xl transition duration-300 group-hover:text-blue-600">Water consumption per year: {{ country.waterComsumption }} m³</span>
                            </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</div>
</template>

<script setup>
  
    const { id } = useRoute().params
    const uri = 'http://localhost:3030/countries/' + id 

    const { data: country } = await useFetch(uri)

</script>

<style scoped>

</style>