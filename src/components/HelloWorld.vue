<template>
  <div class="hello">
    <div class="login-session">
      <img src="../static/img/logo.png" alt="布谷"/>
      <el-form :model="loginForm" status-icon :rules="rules" ref="loginForm"  class="loginForm">
        <el-form-item label="" prop="username">
          <el-input class="input-item" v-model="loginForm.phone" clearable placeholder="手机号" prefix-icon="el-icon-user"></el-input>
        </el-form-item>
        <el-form-item label="" prop="password">
          <el-input class="input-item" type="password" v-model="loginForm.password" autocomplete="off" placeholder="密码" clearable prefix-icon="el-icon-lock"></el-input>
        </el-form-item>
        <el-form-item>
          <el-button type="primary" @click="submitForm('ruleForm')">
            登录
          </el-button>
        </el-form-item>
      </el-form>
      <div class='register'><router-link to='/register'>还没账号？去注册</router-link></div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data () {
    return {
      input2:"",
      msg: 'Welcome to Your Vue.js App',
      loginForm:{
        phone:"",
        password:""
      },
      rules:{

      }
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  img{
    width:150px;
    height:150px;
    border-radius:50%;
    margin-bottom:30px;
  }
  .login-session{
    padding-top:100px;
    display:flex;
    flex-direction:column;
    justify-content: center;
    align-items: center;
    z-index:3;
  }
  .hello{
    position: relative;
    height:100%;
    width:100%;
  }
  .hello::before{
    content:'';
    position: absolute;
    top:0;
    left:0;
    height:100%;
    width:100%;
    background:transparent url(../static/img/bg.jpg) center center no-repeat;
    filter: blur(25px);
    z-index: -1;
    background-size:cover;
  }
  .input-item >>> .el-input__inner{
    width:320px;
    opacity: 0.8;
    margin-top:6px;
    margin-bottom:6px;
    border-radius: 30px;
  }
  .el-button{
    width:320px;
    border-radius: 30px;
  }
  .register{
    width:320px;
    text-align:right;
    float:right;
  }
  a{
    margin-right:10px;
    color:black;
    text-decoration:none;
  }

</style>
