<template>
<div class="w1/3 mx-auto balala">

<h1 class="text-5xl mb-8 flex justify-center">{{post.title}}</h1>
<div class="flex justify-between">
<img class="w-1/2 picture mt-32" :src="post.image" />
<div class="w-2/4">
   <nuxt-content class=" w-4/5 mt-4" :document="post" ></nuxt-content>
</div>
</div>

</div>
</template>

<script>
export default {
  async asyncData({$content, params}) {
    let post = await $content('blogposts/post'+params.id).fetch()

    return {
     post
    }
  },
}
</script>

<style>
.balala{
  background-color: #dfdfdf;
}
.picture{
  margin: 20px;
}
</style>
