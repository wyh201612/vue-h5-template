<!-- home -->
<template>
    <div>
        <h1>home</h1>
        <van-button type="primary" @click="tbn">主要按钮</van-button>
    </div>
</template>

<script>
  import { api } from '@/config'
  import { login } from '@/api/user.js'
  import {
    Button
  } from 'vant'
  export default {
    components: {
      'van-button': Button
    },

    data() {
      return {}
    },

    computed: {},

    mounted() {
      console.log(process.env)
      console.log(api)
    },

    methods: {
        tbn() {
            let params = {}
            login(params).then(result => {
                console.log(result)
            })
        }
    }
  }

</script>
<style lang='scss' scoped>
    h1 {
        background: red;
        width: 375px;
    }
</style>
