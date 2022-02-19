<template>
  <section>
    <h1>{{message}}</h1>
    <p>id: {{ this.$route.params.id }}</p>
    <!-- urlパラメーターとして取得するにはこのように記述 -->
  </section>
</template>

<script>
export default {
  data: function(){
    return {
      message: '/users/_id.vueを表示'
    }
  }
}
</script>

