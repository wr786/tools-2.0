<template>
  <div class="app">
    <asfNavbar :nav-list="navList"></asfNavbar>
    <div class="route-view">
      <div class="componts-box">
        <router-view />
      </div>
    </div>
  </div>
</template>
<script lang="ts">
import { defineComponent } from 'vue'
import { useRouter } from 'vue-router'
import asfNavbar from '@/components/Navbar.vue'
export default defineComponent({
  components: { asfNavbar },
  setup() {
    const route = useRouter()
    const navList = [
      {
        name: '敬请期待',
      },
      {
        name: '敬请期待',

      },
      {
        name: '实用工具',
        secondaryList: [
          { name: '枝网查重', methods: 'router', link: '/duplicateChecking' },
          { name: '今日溜什么', methods: 'router', link: '/randomVideo' },
          { name: '成分姬', methods: 'router', link: '/ingredientChecking' },
          { name: "表情包", methods: "router", link: "/emojicollect" },
          { name: '方言词典', methods: 'router', link: '/zhijiangDict' },
        ],
      },
      {
        name: '敬请期待',
      },
    ]
    return {
      navList,
    }
  },
})
</script>
<style>
.app {
  font-family: system-ui, -apple-system, "Segoe UI", Roboto, "Helvetica Neue",
    Arial, "Noto Sans", "Liberation Sans", "PingFang SC", "Hiragino Sans GB",
    "Noto Sans CJK SC", "Source Han Sans SC", "Source Han Sans CN",
    "Microsoft YaHei", "Wenquanyi Micro Hei", "WenQuanYi Zen Hei", "ST Heiti",
    SimHei, "WenQuanYi Zen Hei Sharp", "Apple Color Emoji", "Segoe UI Emoji",
    "Segoe UI Symbol", "Noto Color Emoji", sans-serif;
}
.route-view {
  padding: 0 5.83vw;
}
.componts-box {
  margin: auto;
}
</style>
