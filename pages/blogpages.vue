<template>
     <div>
        <div>
          <h1 class="text-4xl text-center backgroundshit h-24 z-20">
            My Experiences
          </h1>
        </div>
        <div>
             <img class="z-0 relative" src="../static/images/background3.png">
             <img class="z-0 relative" src="../static/images/background3.png">
        </div>

  <div class="flex absolute flex-wrap justify-evenly z-30 top-2/4">

    <div @click="goToPost(post.id)" class="w-80 h-92m-4 z-10" v-for="post in blogposts" :key="post.id">


      <PostListItem :item="post"></PostListItem>



      <div class="posts" v-for="post in blogposts"
        :key="post.id">

      </div>



 </div>
 </div>



</div>

</template>

<script>
export default {
  name: 'IndexPage',
  async asyncData({$content}) {
    let blogposts = await $content('blogposts').without(['body'])
    .sortBy('createdAt', 'asc').fetch();
    return {
      blogposts
    }
  },
  methods: {
    goToPost(id) {
      this.$router.push('/post-details/'+id)
    }
  }
}
</script>

<style>
.backgroundshit{
  background-color: #dfdfdf;
}
</style>


