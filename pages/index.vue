<template>
  <section class="container">
    <div>
      {{users[0].id}},{{ users[0].name }}
    </div>
  </section>
</template>

<script>
const axios = require('axios')
// axiosのインスタンス作成
let url = 'https://jsonplaceholder.typicode.com/users'

export default {
  asyncData({ params }){
    return axios.get(url)
    // APIのデータ取得
    .then((res) => {
    // resにはサーバーからのレスポンスデータが入っている
      return {users:res.data}
    })
  }
}
</script>
