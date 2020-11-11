<template>
  <el-form
    class="loginForm"
    :model="loginForm"
    :rules="loginRule"
    ref="loginForm"
    label-width="100px"
  >
    <el-form-item label="账号" prop="username">
      <el-input v-model="loginForm.username" placeholder="请输入账号"></el-input>
    </el-form-item>
    <el-form-item label="密码" prop="password">
      <el-input v-model="loginForm.password" show-password placeholder="请输入密码"></el-input>
    </el-form-item>
    <el-form-item>
      <el-button type="primary" @click="submitForm('loginForm')">登录</el-button>
      <el-button @click="toRegist()">注册</el-button>
    </el-form-item>
  </el-form>
</template>

<script>
export default {
  data () {
    return {
      loginForm: {
        username: 'admin',
        password: '123456'
      },
      loginRule: {
        username: [
          { required: true, message: '请输入账号！', trigger: 'blur' },
          { min: 8, max: 15, message: '长度在 8 到 15 个字符', trigger: 'blur' }
        ],
        password: [
          { required: true, message: '请输入密码！', trigger: 'blur' },
          { min: 8, max: 15, message: '长度在 8 到 15 个字符', trigger: 'blur' }
        ]
      }
    }
  }
}
</script>

<style scoped>
.loginForm {
  
}
</style>
