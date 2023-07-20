<template>
    <div>
        
        <div class="grid grid-cols-3 gap-5 items-center py-10">
            <div class="col-span-1">
                <img :src="meal.meals[0].strMealThumb" alt="" width="400" height="400" class="ronded-full">
            </div>
        </div>
        <div class="col-span-2">
            <h1 class="text-2xl font-bold">{{ meal.meals[0].strMeal }}</h1>
            <p>{{meal.meals[0].strInstructions  }}</p>
            <h1 class="text-xl text-red-500">Video Tutorial</h1>
           
            
    
        </div>
    </div>
</template>

<script setup>
const route = useRoute();
const {data:meal} = await useFetch(`https://www.themealdb.com/api/json/v1/1/lookup.php?i=${route.params.id}`)
</script>

<style scoped>

</style>
