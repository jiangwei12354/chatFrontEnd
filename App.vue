<script>
import config from "./config";
import store from "@/store";
import { getToken } from "@/utils/auth";

export default {
  onLaunch: function () {
    this.initApp();
    // 设置用户信息
    if (uni.getStorageSync("App-Token")) {
      this.$store.dispatch("GetInfo").then((res) => {
        // this.$tab.reLaunch("/pages/index");
      });
    }
  },
  methods: {
    // 初始化应用
    initApp() {
      // 初始化应用配置
      this.initConfig();
      // 检查用户登录状态
      //#ifdef H5
      this.checkLogin();
      //#endif
    },
    initConfig() {
      this.globalData.config = config;
    },
    checkLogin() {
      if (!getToken()) {
        this.$tab.reLaunch("/pages/login");
      }
    },
  },
};
</script>

<style lang="scss">
@import "@/static/scss/index.scss";
</style>
