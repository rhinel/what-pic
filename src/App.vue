<template>
  <div id="app">
    <div class="menu-wrap">
      <el-menu class="menu" theme="dark" :default-active="$route.path" mode="horizontal" router>
        <el-menu-item index="/top">Top</el-menu-item>
        <el-menu-item index="/new">New</el-menu-item>
        <el-menu-item index="/show">Show</el-menu-item>
        <el-menu-item index="/ask">Ask</el-menu-item>
        <el-menu-item index="/job">Jobs</el-menu-item>
      </el-menu>
    </div>
    <transition name="fade" mode="out-in">
      <router-view class="view"></router-view>
    </transition>
  </div>
</template>

<style lang="stylus">
body
  font-family -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Oxygen, Ubuntu, Cantarell, "Fira Sans", "Droid Sans", "Helvetica Neue", sans-serif;
  font-size 15px
  background-color lighten(#eceef1, 30%)
  margin 0
  padding-top 55px
  color #34495e
  overflow-y scroll

a
  color #34495e
  text-decoration none

.menu-wrap
  position fixed
  background-color #324157
  z-index 999
  top 0
  left 0
  right 0
  
.menu
  max-width 1000px
  margin 0 auto
  
.view
  max-width 1000px
  margin 0 auto
  position relative

.fade-enter-active, .fade-leave-active
  transition all .2s ease

.fade-enter, .fade-leave-active
  opacity 0

@media (max-width 860px)
  .header .inner
    padding 15px 30px

@media (max-width 600px)
  .header
    .inner
      padding 15px
    a
      margin-right 1em
    .github
      display none
</style>
