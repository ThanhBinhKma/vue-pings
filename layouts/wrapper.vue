<template>
  <el-container :class="{ 'is-collapse': isCollapse }">
    <!-- <TheSideBar /> -->
    <el-container
      :style="{ marginLeft: isCollapse ? '70px' : '200px' }"
      class="is-vertical"
      style="transition: all .3s"
    >
      <TheHeader :is-collapse="isCollapse" />
      <el-main style="margin-top: 60px">
        <nuxt />
      </el-main>
    </el-container>
  </el-container>
</template>

<script>
import TheHeader from '~/components/layout-wrapper/TheHeader'
// import TheSideBar from '~/components/layout-wrapper/TheSideBar'

export default {
  components: {
    TheHeader
    // TheSideBar
  }
  // computed: {
  //   isCollapse() {
  //     return this.$store.state.isCollapse
  //   }
  // }
}
</script>
