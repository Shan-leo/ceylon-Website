<template>
<h1>Contact us</h1>
  <form action="/" class="decor">
      <div class="form-inner">        
        <input type="text" placeholder="First Name"><br>
        <input type="text" placeholder="Last Name"><br>
        <input type="email" placeholder="Email"><br>
        <textarea placeholder="Message..." rows="5"></textarea><br>
        <button type="submit" href="/">Submit</button>
      </div>
    </form>
</template>

<script>
export default {
    name:'ContactUs'

}
</script>

<style scoped>

form{
  width: 350px;
  margin: 1rem auto;
  padding: 2rem;
  background-color: aquamarine;
  border-radius: 1rem;

}

input{
  height: 1.5rem;
  margin: 0.5rem;
  width: 80%;
  padding: 2px;
}

textarea{
  width: 80%;
  margin: 0.5rem;
  padding: 3px;
}

button{
  width: 50%;
  height: 1.5rem;
  font-size: 1rem;
  font-weight: 600;
  padding: ;
}
</style>