<template>
<div class="w1/2 mx-auto">
<h1>{{$route.params.id}}</h1>
<h1 class="text-5xl mb-8">{{dish.title}}</h1>
<img :src="dish.image" />
<p class="mb-8">{{dish.description}}</p>
<nuxt-content document="dish"></nuxt-content>
</div>
</template>

<script>
export default {
  async asyncData({$content, params}) {
    let dish = await $content('dishes/dish'+params.id).fetch()

    return {
     dish
    }
  },
}
</script>