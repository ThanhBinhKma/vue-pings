<template>
  <el-header :style="{ left: isCollapse ? '70px' : '200px' }" class="is-header">
    <el-dropdown trigger="click" class="mx-3" @command="handleCommand">
      <img :src="flagLanguage" alt />
      <el-dropdown-menu slot="dropdown">
        <el-dropdown-item command="en">
          <div class="d-flex justify-content-between align-items-center">
            <div class="mr-4">
              <img :src="require('~/assets/images/flags/en.png')" />
            </div>
            <span></span>
          </div>
        </el-dropdown-item>
        <el-dropdown-item command="ja">
          <div class="d-flex justify-content-around align-items-center">
            <div class="mr-4">
              <img :src="require('~/assets/images/flags/ja.png')" />
            </div>
            <span></span>
          </div>
        </el-dropdown-item>
      </el-dropdown-menu>
    </el-dropdown>
    <el-dropdown trigger="click" @command="handleCommand">
      <el-avatar></el-avatar>
      <el-dropdown-menu slot="dropdown">
        <el-dropdown-item command="changePassword"></el-dropdown-item>
        <el-dropdown-item command="changeAvatar"></el-dropdown-item>
        <el-dropdown-item command="logout"></el-dropdown-item>
      </el-dropdown-menu>
    </el-dropdown>
  </el-header>
</template>

<script>
export default {
  // computed: {
  //   isCollapse() {
  //     return this.$store.state.isCollapse
  //   },
  //   locale() {
  //     return this.$store.state.locale
  //   },
  //   avatar() {
  //     return this.$store.state.user.avatar
  //   },
  //   flagLanguage() {
  //     return require(`~/assets/images/flags/${this.locale}.png`)
  //   }
  // }
  // methods: {
  //   async handleCommand(command) {
  //     switch (command) {
  //       case 'logout':
  //         await this.$auth.logout()
  //         // document.location.reload()
  //         break
  //     }
  //   }
  // }
}
</script>

<style scoped>
.is-header {
  height: 60px;
  text-align: right;
  font-size: 12px;
  position: fixed;
  z-index: 100;
  right: 0;
  transition: all 0.3s;
  background: #fff;
}
</style>
