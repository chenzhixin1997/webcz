<template>
  <div>
    <ul class="intab head">
      <li v-for="(v,i) in arr" :key="i">{{v.text}}</li>
    </ul>
  </div>
</template>

<script>
  export default{
    name:'header',
    data(){
      return{
        arr:[
          {id:'1',text:'首页'},
          {id:'2',text:'首页2'},
          {id:'3',text:'首页3'},
          {id:'4',text:'首页4'},
          {id:'5',text:'首页5'},
          {id:'6',text:'首页6'}
        ]
      }

    },

  }
</script>

<style scoped>
  .head{
    height:90px;
    line-height: 90px;
    padding-left: 20px;
  }
  .head li{
    float: left;
    cursor:pointer;
    margin-right:50px;
  }
</style>
