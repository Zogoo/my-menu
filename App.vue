<template>
  <app-navigator></app-navigator>
</template>

<script>
import {
  createAppContainer,
  createBottomTabNavigator,
  createMaterialTopTabNavigator,
  createStackNavigator
} from "vue-native-router";

import HomeTab from "./src/tabs/HomeTab";
import MenuTab from "./src/tabs/MenuTab";
import HistoryTab from "./src/tabs/HistoryTab";

// An iOS style bottom tab-bar navigator
const BottomTabNavigator = createBottomTabNavigator(
  {
    Menu: MenuTab,
    History: HistoryTab
  }
);

// An Android style top tab-bar navigator
const MaterialTopTabNavigator = createMaterialTopTabNavigator(
  {
    Menu: MenuTab,
    History: HistoryTab
  }
);

// The navigators can be used as regular screens in any other navigator
const StackNavigator = createStackNavigator(
  {
    Home: HomeTab,
    IOSTabs: BottomTabNavigator,
    AndroidTabs: MaterialTopTabNavigator
  }
);

const AppNavigator = createAppContainer(StackNavigator);
</script>