<template>
  <div>
    <!-- nuxt hook, the page we load from pages folder 
    will get renderd at the place of nuxt hook -->
    <TheHeader/>
    <main class="main-content">
      <nuxt/>
    </main>
  </div>
</template>

<script>
  import TheHeader from "~/components/TheHeader/TheHeader";

  export default{
    components:{
      TheHeader: TheHeader
    }
  }

</script>


<style>
* {
  box-sizing: border-box;
}

body{
  font-family: "Titillium Web", sans-serif;
}

.main-content{
  margin: 4.5rem;
  padding: 1.2rem;
  /* border: solid 1px #271941; */
}
</style>

