<template>
    <p class="container rounded-xl mt-4 pb-4 pt-4 md:w-50 text-xl font-bold bg-blue-400 mx-auto px-4 flex justify-center items-center">Click to view data for specific country</p>
    <div>
        <section class="container mx-auto bg-blue-200 h-full rounded-xl">
            <div class="text-xl mt-4 pt-8 grid grid-cols-4 gap-5 pb-8 px-4 mb-4">
                <div v-for="c in countries">
                    <NuxtLink :to="`/Countries/${c.id}`"> {{ c.countryName }}</NuxtLink>
                </div>
            </div>
        </section>
    </div>
</template>

<script setup>

const { data: countries } = await useFetch('http://localhost:3030/countries')

</script>

<style  scoped>

</style>   