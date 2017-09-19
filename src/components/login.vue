<template>
    <div class="login">
      <input class="form-control" id="inputEmail" placeholder="请输入账号" v-model="account"/>
      <input class="form-control" type="password" id="inputPassword" placeholder="请输入密码" v-model="password"/>
      <button type="submit" class="btn btn-default" @click="login">登录</button>
    </div>
</template>

<script>
    export default {
        name: 'login',
        data () {

        }
    }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
