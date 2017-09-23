<template>
  <div class="app flex-row align-items-center">
    <div class="background">
      <img v-bind:src=" loginimg" />
    </div>
    <div class="container">
      <div class="row justify-content-center">
        <div class="col-md-6">
          <div class="card mx-4">
            <div class="card-body p-4">
              <div class="alert alert-danger" :class="{alertshow: true}">
                This is a warning alert—check it out!
              </div>

              <h1 class="text-center p-4">会员注册</h1>
              <div class="input-group mb-3">
                <span class="input-group-addon"><i class="icon-user"></i></span>
                <input type="text" class="form-control" placeholder="用户名" v-model="user.name">
              </div>

              <div class="input-group mb-3">
                <span class="input-group-addon">@</span>
                <input type="text" class="form-control" placeholder="邮箱" v-model="user.email">
              </div>

              <div class="input-group mb-3">
                <span class="input-group-addon"><i class="icon-lock"></i></span>
                <input type="password" class="form-control" placeholder="密码" v-model="user.password">
              </div>

              <div class="input-group mb-4">
                <span class="input-group-addon"><i class="icon-lock"></i></span>
                <input type="password" class="form-control" placeholder="重复密码"  v-model="user.rePassword"  @blur="comparePassword">
                <span>密码输入不一致</span>
              </div>

              <button type="button" class="btn btn-block btn-success" @click="login">注册</button>
            </div>
            <div class="card-footer p-4">
              <p>如果您已经有账号了，可以点此登录  <router-link class="btn btn-primary mx-3 login" to="/Login">登录</router-link></p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Register',
  data () {
    return {
      loginimg: '/static/img/login/login (2).jpg',
      'alertshow': true,
      user: {
        name: '',
        email: '',
        password: '',
        rePassword: ''
      }
    }
  },
  methods: {
    switchImg () {
      var index = parseInt(Math.random() * 38)
      this.loginimg = '/static/img/login/login (' + index + ').jpg'
    },
    login () {
      console.log(this.user)
    },
    comparePassword () {
      if (this.user.password !== this.user.rePassword) {
        console.log('err')
      }
    }
  },
  mounted () {
    this.switchImg()
  }
}
</script>
<style scoped lang="scss">

  .background{
    height: 100%;
    width: 100%;
    position: absolute;
    overflow: hidden;
    img{
      width: 100%;
      height: 100%;
    }
    .card-body{
      color:#fff;
    }
    .card-body .alert-danger{
      display: none;
    }
    .alertshow{
      display: block;
      color: #00a67c;
    }

  }
</style>
