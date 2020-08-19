<template>
  <view>
    <order/>
    <u-tabbar
        v-model="current"
        :show="show"
        :bg-color="bgColor"
        :mid-button="midButton"
        :list="list"
        :inactive-color="inactiveColor"
        :activeColor="activeColor"
    ></u-tabbar>
  </view>
</template>

<script>
import Order from '@/pages/order'
export default {
  name: 'home',
  components: {
    Order
  },
  data() {
    return {
      current: 0,
      show: true,
      bgColor: '#ffffff',
      borderTop: true,
      list: [{
        iconPath: "home",
        selectedIconPath: "home-fill",
        text: '首页',
        count: 2,
        isDot: true,
        customIcon: false,
      },
        {
          iconPath: "photo",
          selectedIconPath: "photo-fill",
          text: '放映厅',
          customIcon: false,
        },
        {
          iconPath: "play-right",
          selectedIconPath: "play-right-fill",
          text: '直播',
          midButton: true,
          customIcon: false,
        },
        {
          iconPath: "lock",
          selectedIconPath: "lock-fill",
          text: '发布',
          customIcon: false,
        },
        {
          iconPath: "account",
          selectedIconPath: "account-fill",
          text: '我的',
          count: 23,
          isDot: false,
          customIcon: false,
        },
      ],
      midButton: false,
      inactiveColor: '#909399',
      activeColor: '#5098FF'
    }
  }
}
</script>

<style lang="sass" scoped>
</style>