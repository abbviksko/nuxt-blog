<template>
<div>
    <img :src="item.image" alt="post.image" class=" object-cover object-right" style="width: 300px; height:450px;">
    <h3>{{item.title}}</h3> 
    <p>{{item.description}}</p>
    
</div>
</template>

<script>
export default {
    props:['item'],
    data() {
        return {

        }
    }
}
</script>