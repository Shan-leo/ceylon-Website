<template>
  <div class="container">
      <h2>{{post.title}}</h2>
      <img :src="require(`../assets/images/provinces/${post.image}`)" alt="">
      <p>{{post.body}}</p>
  </div>
</template>

<script>
export default {
    name:'Post',
    props:['post']

}
</script>

<style scoped>

.container{
    width: 70%;
    margin: 1rem auto;
    border-style:solid;
    border-color: #42b983;
    padding: 1rem;
    border-radius: 1rem;
}

img{
    width: 70%;
    border-radius: 1rem;
}

h2{
    margin: 1rem;
}
p{
    margin: 1rem;
}

</style>