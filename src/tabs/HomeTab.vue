<template>
  <view class="container">
    <text class="heading">Home</text>
    <text class="text">This is the Home screen</text>
    <text class="text">Use the swipe gesture to open the drawer navigator</text>
    <button title="View fuck" @press="goToIOSTabNavigator"></button>
    <button title="View aaa" @press="goToAndroidTabNavigator"></button>
  </view>
</template>

<script>
export default {
  props: {
    navigation: { type: Object }
  },
  methods: {
    goToIOSTabNavigator() {
      this.navigation.navigate("MenuTab")
    },
    goToAndroidTabNavigator() {
      this.navigation.navigate("HistoryTab")
    }
  }
}
</script>

<style>
.container {
  align-items: center;
  justify-content: center;
  flex: 1;
  padding: 50px;
}
.heading {
  font-size: 30px;
  font-weight: bold;
  color: darkolivegreen;
  margin: 20px;
}
.text {
  text-align: center;
  margin: 10px;
}
</style>