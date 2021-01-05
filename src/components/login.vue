<template>
  <div class="login-wrapper">
    <el-form ref="form" :model="form" label-width="80px" class="login-form">
      <el-form-item label="用户名">
        <el-input v-model="form.name"></el-input>
      </el-form-item>
      <el-form-item label="密码">
        <el-input type="password" v-model="form.password"></el-input>
      </el-form-item>
      <el-form-item>
        <el-button type="primary" @click="login">登陆</el-button>
        <el-button type="info" @click="reset">重置</el-button>
      </el-form-item>
    </el-form>
  </div>
</template>
<script>
export default {
  name: "",
  data() {
    return {
      form: {
        name: "",
        password: ""
      }
    };
  },
  methods: {
      login() {
        console.log(this.form.name);
        console.log(this.form.password);
      },
      reset() {
        this.form.name = ''
        this.form.password = ''
      }
  }
};
</script>
<style scoped lang="less">
.login-wrapper {
  width: 100%;
  height: 100%;
  background-color: #274a6c;
  display: flex;
  align-items: center;
  justify-content: center;
  .login-form {
    width: 600px;
    height: 400px;
    padding: 20px;
    background-color: #fff;
  }
}
</style>
