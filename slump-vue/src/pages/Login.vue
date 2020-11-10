<template>
  <el-form :model="loginForm" :rules="loginRule" ref="loginForm" label-width="100px">
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
        username: '17370012735',
        password: '123456'
      },
      loginRule: {
        username: [
          { required: true, message: '请输入账号！', trigger: 'blur' },
          { min: 3, max: 5, message: '长度在 3 到 5 个字符', trigger: 'blur' }
        ],
        password: []
      }
    }
  }
}
</script>

<style></style>
