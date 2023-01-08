<template>
  <div>111</div>
</template>

<script>
export default {
 async asyncData({$axios}) {
    const url = 'http://localhost:9090/test'
    const res = await $axios.$get(url)
    console.log(res);
  },
}
</script>
