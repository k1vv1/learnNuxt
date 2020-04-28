<template>
  <div>
    <h1>xxx: {{info.data.banner.context.currentTime}}</h1>
  </div>
</template>

<script>
import axios from 'axios'
export default {
  data() {
    return {
      name: "Hello World"
    }
  },

  async asyncData() {
    let {data} = await axios.get('http://123.207.32.32:8000/home/multidata')
    return {info: data}
  }
  // asyncData() {
  //   return axios.get('http://123.207.32.32:8000/home/multidata')
  //   .then(res => {
  //     return {info: res.data.data.banner.context}
  //   })
  // }
}
</script>