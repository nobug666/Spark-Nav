<template>
  <el-row style="height: 100vh">
    <div
      :style="{
        width: leftWidth,
        background: '#fff',
        overflow: 'hidden',
      }"
    >
      <Menu
        :isCollapse="collapse"
        :isShow="show"
        :isDrawer="drawer"
        @handleClose="changeClose"
        @jump1="jump(1)"
        @jump2="jump(2)"
        @jump3="jump(3)"
        @jump4="jump(4)"
        @jump5="jump(5)"
        @jump6="jump(6)"
        @jump7="jump(7)"
      ></Menu>
    </div>
    <div :style="{ width: contentWidth }" class="content">
      <div class="top">
        <Search
          :maxWidth="innerWidthMax"
          :isShow="show"
          :isCollapse="collapse"
          @handleBtn="changeBtn"
          @handleDraw="changeDraw"
        ></Search>
      </div>
      <div
        :class="[!showDialog ? 'bottom' : 'bottom dialog']"
        v-show="!showAbout"
      >
        <Content
          ref="content"
          @handleClose="changeClose"
          @handleDialog="dialogClick"
        ></Content>
      </div>
      <div
        :class="[!showDialog ? 'bottom' : 'bottom dialog']"
        v-show="showAbout"
      >
        <About ref="about"></About>
      </div>
    </div>
  </el-row>
</template>

<script>
import Menu from "./components/Menu.vue";
import Search from "./components/Search.vue";
import Content from "./components/Content.vue";
import About from "./components/About.vue";

export default {
  name: "App",
  components: {
    Menu,
    Search,
    Content,
    About,
  },
  data() {
    return {
      timer: "",
      collapse: false,
      leftWidth: "300px",
      contentWidth: "calc(100% - 300px)",
      show: true,
      drawer: false,
      innerWidthMax: true,
      showDialog: false,
      showAbout: false,
    };
  },
  mounted() {
    this.searchFormWidth();
    window.onresize = () => {
      if (!this.timer) {
        this.timer = true;
        let that = this;
        setTimeout(function () {
          that.searchFormWidth();
          that.timer = false;
        }, 100);
      }
    };
  },
  unmounted() {
    window.onresize = null;
  },
  methods: {
    searchFormWidth() {
      let w = window.innerWidth;
      if (w <= 1000) {
        this.collapse = true;
        this.leftWidth = "0px";
        this.contentWidth = "100%";
        this.show = false;
      } else {
        this.collapse = false;
        this.leftWidth = "300px";
        this.contentWidth = "calc(100% - 300px)";
        this.show = true;
        this.innerWidthMax = true;
      }
    },
    changeBtn(event) {
      this.collapse = event;
      let w = window.innerWidth;
      if (event) {
        this.collapse = true;
        if (w <= 1000) {
          this.leftWidth = "0px";
          this.contentWidth = "100%";
        } else {
          this.leftWidth = "50px";
          this.contentWidth = "calc(100% - 50px)";
          this.innerWidthMax = false;
        }
      } else {
        this.collapse = false;
        this.leftWidth = "300px";
        this.contentWidth = "calc(100% - 300px)";
        this.innerWidthMax = true;
      }
    },
    changeDraw() {
      this.drawer = true;
    },
    changeClose() {
      this.drawer = false;
    },
    dialogClick(event) {
      this.showDialog = event;
    },
    jump(event) {
      this.showAbout = false;
      if (event == 1) {
        setTimeout(() => {
          this.$refs["content"].toJump1();
        }, 200);
      } else if (event == 2) {
        setTimeout(() => {
          this.$refs["content"].toJump2();
        }, 200);
      } else if (event == 3) {
        setTimeout(() => {
          this.$refs["content"].toJump3();
        }, 200);
      } else if (event == 4) {
        setTimeout(() => {
          this.$refs["content"].toJump4();
        }, 200);
      } else if (event == 5) {
        setTimeout(() => {
          this.$refs["content"].toJump5();
        }, 200);
      } else if (event == 6) {
        setTimeout(() => {
          this.$refs["content"].toJump6();
        }, 200);
      } else if (event == 7) {
        this.showAbout = true;
        this.drawer = false;
        setTimeout(() => {
          this.$refs["about"].toJump7();
        }, 200);
      }
    },
  },
};
</script>

<style scoped>
.content {
  position: relative;
  background: url(assets/banner.jpg) no-repeat;
  background-size: 100% 100%;
  overflow-y: auto;
}
.bottom {
  z-index: 1;
  position: absolute;
  top: 60px;
  left: 0;
  right: 0;
  bottom: 0;
}
.dialog {
  z-index: 2 !important;
}
@media screen and (max-width: 1000px) {
  .search {
    position: fixed;
    top: 0;
    left: 0;
    right: 0;
    height: 50px;
    z-index: 2;
  }
  .bottom {
    z-index: 1;
  }
}
</style>
