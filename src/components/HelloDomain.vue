<template>
  <div>
    hello domain
  </div>
</template>

<script>
import axios from 'axios'

export default {
  name: 'hello-domain',
  created () {
    console.log(process.env)
    axios.post(process.env.API_HOST + 'api/0/app2/goods/homeAdInfo.do', {
      'appTypeId': '0',
      'lang': '0',
      'countryCode': 'SA',
      'appVersion': '5.4',
      'currency': 'sar',
      'terminalType': '2',
      'type': 17,
      'tabCode': 'JCRC'
    }).then((res) => {
      console.log('post请求', res)
    })
    axios.get(process.env.API_HOST1 + 'virtualGoods/getGoodsDetail.do', {
      params: {
        'appTypeId': '0',
        'lang': '0',
        'countryCode': 'SA',
        'appVersion': '5.4',
        'currency': 'sar',
        'terminalType': '2',
        'type': 1
      }
    }).then((res) => {
      console.log('get请求', res)
    })
  }
}
</script>

<style scoped>

</style>
