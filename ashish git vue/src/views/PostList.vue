<template>
    <div class="post-list">
        <div class="card mb-5" v-for="post of posts" :key="post.id">
        <div class="card-body">
            <h3><router-link :to="`/post-details/${post.id}`">{{post.title}}
            </router-link>
            </h3>
            <p>{{post.body}}</p>
      
        </div>
        </div>
        <div class="card mb-5" v-if="errors && errors.length">
        <div class="card-bo dy">
        
            <p v-for="(error,index) of errors" :key="index">{{}error.message}</p>
      
        </div>
        </div>
    </div>
</template>


<script>


export default {
    name:"PostList",
    props: ["posts"]

};
</script>

<style>

</style>
