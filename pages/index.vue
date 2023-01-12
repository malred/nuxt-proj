<template>
  <div>{{ test }}</div>
</template>

<script>
export default {
  // 获取服务端渲染的数据
  // 在服务端和客户端渲染前执行
  async asyncData({$axios}) {
    // 获取本地static文件夹下的文件
    const url = 'http://localhost:3000/data.json'
    const res = await $axios({
      url,
      method: 'get'
    })
    // 这里导出的数据(和data(){}返回的数据混合并导出)可以直接使用
    return res.data
  },
}
</script>
