<template>
  <section class="container">
    <div>
      <!-- {{users[0].id}},{{ users[0].name }} -->
      <ul>
        <li v-for="user in users" :key="user.id">
          {{ user.id }},{{ user.name }},{{ user.company.name }}
        </li>
      </ul>
    </div>
  </section>
</template>

<script>
const axios = require('axios')
// axiosのインスタンス作成
let url = 'https://jsonplaceholder.typicode.com/usersdd'

export default {
  asyncData({ params, error }){
    return axios.get(url)
    // APIのデータ取得
    .then((res) => {
    // resにはサーバーからのレスポンスデータが入っている
      return {users:res.data}
    })
    .catch((e => {
      // console.log(e.response.status)
      error({ users: e.response.status, messanger: 'Error!!' })
    }))


  }
}
</script>
