<template>
  <div class="">
    <Header></Header>
  </div>
</template>

<script>
import Header from '@/components/header'
export default {
  name: 'index',
  data () {
    return {
      msg: ''
    }
  },
  components:{
    Header
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
