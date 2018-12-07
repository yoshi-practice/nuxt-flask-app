<template>
  <div>
    <h1>{{ data.message }}</h1>
  </div>
</template>

<script>
import axios from 'axios'

export default {
  async asyncData () {
    let data = await axios.get('/api')
    console.log(data)
    return data.data
  }
}
</script>