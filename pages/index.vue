<template>
  <section class="container">
    <p>{{message}}</p>
    <router-link to="/price">pricepage</router-link>
  </section>
</template>

<script>
export default {
 data: function(){
    return {
    message: "Helloworld"
  }
 }
}
</script>
