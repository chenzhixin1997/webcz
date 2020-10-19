<template>
  <div class="login">

    <div class="login_form">
      <h3>首页登录</h3>
      <div class="xon">
        <el-input v-model="txt" placeholder="请输入账号" style="margin-bottom: 20px;"></el-input>
        <el-input v-model="pad" placeholder="请输入密码" show-password></el-input>
        <div class="dl xscale" @click="login()">登录</div>
        <div class="zc xscale" @click="register()">注册</div>
      </div>
    </div>
  </div>
</template>

<script>
  export default {
    name: 'login',
    data () {
      return {
        msg: '',
        txt: '',
        pad:''
      }
    },
    methods:{
      login(){
        if(this.txt==''){
          this.$message({
            showClose:true,
            message: '请输入账号',
            type: 'warning'
          });
        }else if(this.pad==''){
          this.$message({
            showClose:true,
            message: '请输入密码',
            type: 'warning'
          });
        }else{
          this.$message({
            showClose:true,
            message: '登录成功',
            type: 'success'
          });
          this.$router.push({
            path:'/index'
          })
        }

      },
      register(){
        this.$message.error('功能暂未开通');
      }
    },
    mounted(){

    }
  }
</script>

<style scoped>
  .xscale{
    cursor: pointer;
  }
  .xscale:hover{
    box-shadow:0px 0px 30px 10px #f6f6f6 inset;
  }
  .login{
    position: fixed;
    width:100%;
    height:100%;
    background: url(../assets/bjimage.jpg) no-repeat fixed 50% 50%/cover;
/*    background-repeat: no-repeat; */
  }
  .login_form{
    width:480px;
    height:350px;
    margin: 150px auto;
    background: #87CEEB;
    padding-top:15px;
  }
  .login_form h3{
    margin-bottom:20px;
  }
  .xon{
    width:80%;
    margin:0px auto;
  }
  .dl{
    width:100%;
    height:40px;
    line-height: 40px;
    text-align: center;
    margin-top: 20px;
    border-radius: 4px;
    background: #26A2FF;
    color:#fff;
  }
  .zc{
    width:100%;
    height:40px;
    line-height: 40px;
    text-align: center;
    margin-top: 20px;
    border-radius: 4px;
    background:#42B983;
    color:#fff;
  }
</style>
