<template>
  <div class="search">
    <div :class="[maxWidth ? 'top max' : 'top small']" v-if="isShow">
      <img :src="isCollapse ? hidden : open" alt="icon" @click="handleEmit" />
      <div id="he-plugin-simple"></div>
    </div>
    <div class="top" v-else>
      <img :src="hidden" alt="icon" @click="handleDrawer" />
      <div id="he-plugin-simple"></div>
    </div>
    <!-- <div class="bottom">
      <el-input v-model="input" placeholder="搜索" class="input-with-select">
        <template #append>
          <img :src="Search" alt="icon" />
        </template>
      </el-input>
    </div> -->
  </div>
</template>

<script>
export default {
  name: "Search",
  props: ["isCollapse", "isShow", "maxWidth"],
  data() {
    return {
      show: true,
      open: require("../assets/open.svg"),
      hidden: require("../assets/hidden.svg"),
      Search: require("../assets/search.svg"),
      input: "",
    };
  },
  mounted() {
    window.WIDGET = {
      CONFIG: {
        modules: "01234",
        background: "4",
        backgroundColor: "EEEEEE",
        tmpColor: "000000",
        tmpSize: "16",
        cityColor: "000000",
        citySize: "16",
        aqiColor: "000000",
        aqiSize: "16",
        weatherIconSize: "24",
        alertIconSize: "18",
        padding: "10px 10px 10px 10px",
        shadow: "0",
        language: "zh",
        fixed: "false",
        vertical: "top",
        horizontal: "left",
        key: "473cc2d0a0764025802ef0fbdb3a4632",
      },
    };
    (function (d) {
      var c = d.createElement("link");
      c.rel = "stylesheet";
      c.href =
        "https://widget.heweather.net/simple/static/css/he-simple.css?v=1.4.0";
      var s = d.createElement("script");
      s.src =
        "https://widget.heweather.net/simple/static/js/he-simple.js?v=1.4.0";
      var sn = d.getElementsByTagName("script")[0];
      sn.parentNode.insertBefore(c, sn);
      sn.parentNode.insertBefore(s, sn);
    })(document);
  },
  methods: {
    handleEmit() {
      this.$emit("handleBtn", !this.isCollapse);
    },
    handleDrawer() {
      this.$emit("handleDraw", true);
    },
  },
};
</script>

<style scoped>
.top {
  padding: 10px;
}
.top img {
  width: 30px;
  cursor: pointer;
  vertical-align: middle;
}
:deep(#he-plugin-simple) {
  display: inline-block !important;
  vertical-align: middle;
  z-index: 999;
  max-width: 200px !important;
}
.bottom {
  text-align: center;
}
.bottom .el-input {
  height: 50px;
  line-height: 50px;
  margin: 0 auto;
  width: 60%;
}
:deep(.bottom .el-input__inner) {
  height: 50px;
  line-height: 50px;
  width: 100%;
}
:deep(.el-input-group__append) {
  vertical-align: middle;
}
:deep(.el-input__wrapper.is-focus),
:deep(.el-input__wrapper:hover) {
  box-shadow: 0 0 0 1px transparent !important;
}
.max {
  position: fixed;
  left: 300px;
  right: 0;
  top: 0;
  background-color: #eee;
  z-index: 2;
}
.small {
  position: fixed;
  left: 50px;
  right: 0;
  top: 0;
  background-color: #eee;
  z-index: 2;
}
@media screen and (max-width: 1000px) {
  .top {
    background: #eee;
  }
}
</style>
