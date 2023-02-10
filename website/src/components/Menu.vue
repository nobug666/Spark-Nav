<template>
  <div v-if="isShow">
    <div>
      <router-link to="/" :class="[isCollapse && 'hidden']">
        <img class="logo" :src="logo" alt="logo" /><b>星火导航</b>
      </router-link>
    </div>
    <el-menu
      class="el-menu-vertical"
      default-active="1"
      :collapse="isCollapse"
      :collapse-transition="false"
    >
      <el-menu-item
        index="1"
        :class="[isCollapse && 'hidden']"
        @click="toJump1"
      >
        <img class="icon" :src="saveIcon" alt="icon" />
        <template #title>星火推荐</template>
      </el-menu-item>
      <el-menu-item
        index="2"
        :class="[isCollapse && 'hidden']"
        @click="toJump2"
      >
        <img class="icon" :src="toolIcon" alt="icon" />
        <template #title>常用工具</template>
      </el-menu-item>
      <el-menu-item
        index="3"
        :class="[isCollapse && 'hidden']"
        @click="toJump3"
      >
        <img class="icon" :src="devIcon" alt="icon" />
        <template #title>开发设计</template>
      </el-menu-item>
      <el-menu-item
        index="4"
        :class="[isCollapse && 'hidden']"
        @click="toJump4"
      >
        <img class="icon" :src="wangpanIcon" alt="icon" />
        <template #title>网盘资源</template>
      </el-menu-item>
      <el-menu-item
        index="5"
        :class="[isCollapse && 'hidden']"
        @click="toJump5"
      >
        <img class="icon" :src="communityIcon" alt="icon" />
        <template #title>技术社区</template>
      </el-menu-item>
      <el-menu-item
        index="6"
        :class="[isCollapse && 'hidden']"
        @click="toJump6"
      >
        <img class="icon" :src="learnIcon" alt="icon" />
        <template #title>学习教程</template>
      </el-menu-item>
      <el-menu-item
        index="7"
        :class="[isCollapse && 'hidden']"
        @click="toJump7"
      >
        <img class="icon" :src="aboutIcon" alt="icon" />
        <template #title>关于我们</template>
      </el-menu-item>
    </el-menu>
  </div>
  <div v-else>
    <el-drawer
      v-model="drawer"
      :with-header="false"
      direction="ltr"
      :before-close="handleClose"
    >
      <div>
        <router-link to="/">
          <img class="logo" :src="logo" alt="logo" /><b>星火导航</b>
        </router-link>
      </div>
      <el-menu
        class="el-menu-vertical-mobile"
        default-active="1"
        :collapse="false"
        :collapse-transition="false"
      >
        <el-menu-item index="1" @click="toJump1">
          <img class="icon" :src="saveIcon" alt="icon" />
          <template #title>星火推荐</template>
        </el-menu-item>
        <el-menu-item index="2" @click="toJump2">
          <img class="icon" :src="toolIcon" alt="icon" />
          <template #title>常用工具</template>
        </el-menu-item>
        <el-menu-item index="3" @click="toJump3">
          <img class="icon" :src="devIcon" alt="icon" />
          <template #title>开发设计</template>
        </el-menu-item>
        <el-menu-item index="4" @click="toJump4">
          <img class="icon" :src="wangpanIcon" alt="icon" />
          <template #title>网盘资源</template>
        </el-menu-item>
        <el-menu-item index="5" @click="toJump5">
          <img class="icon" :src="communityIcon" alt="icon" />
          <template #title>技术社区</template>
        </el-menu-item>
        <el-menu-item index="6" @click="toJump6">
          <img class="icon" :src="learnIcon" alt="icon" />
          <template #title>学习教程</template>
        </el-menu-item>
        <el-menu-item index="7" @click="toJump7">
          <img class="icon" :src="aboutIcon" alt="icon" />
          <template #title>关于我们</template>
        </el-menu-item>
      </el-menu>
    </el-drawer>
  </div>
</template>

<script>
export default {
  name: "Menu",
  props: ["isCollapse", "isShow", "isDrawer"],
  data() {
    return {
      logo: require("../assets/spark.svg"),
      saveIcon: require("../assets/save.svg"),
      toolIcon: require("../assets/tool.svg"),
      devIcon: require("../assets/dev.svg"),
      wangpanIcon: require("../assets/wangpan.svg"),
      communityIcon: require("../assets/community.svg"),
      learnIcon: require("../assets/learn.svg"),
      aboutIcon: require("../assets/about.svg"),
      drawer: this.isDrawer,
    };
  },
  watch: {
    isDrawer(newValue) {
      this.drawer = newValue;
    },
  },
  methods: {
    handleClose() {
      this.drawer = false;
      this.$emit("handleClose", false);
    },
    toJump1() {
      this.$emit("jump1", "toJump1");
    },
    toJump2() {
      this.$emit("jump2", "toJump2");
    },
    toJump3() {
      this.$emit("jump3", "toJump3");
    },
    toJump4() {
      this.$emit("jump4", "toJump4");
    },
    toJump5() {
      this.$emit("jump5", "toJump5");
    },
    toJump6() {
      this.$emit("jump6", "toJump6");
    },
    toJump7() {
      this.$emit("jump7", "toJump7");
    },
  },
};
</script>

<style scoped>
img.icon {
  height: 24px !important;
  margin-right: 10px;
  margin-top: -2px;
}
span {
  color: #333;
}
:deep(.el-menu) {
  border: 0 !important;
}
:deep(.el-sub-menu__title) {
  height: 60px;
  padding-left: 45px !important;
}
:deep(.el-sub-menu__title:hover) {
  background-color: transparent !important;
  color: #000;
  font-weight: bold;
}
:deep(.el-menu-item-group__title) {
  display: none;
}
:deep(.el-menu-item) {
  padding-left: 45px !important;
  height: 60px !important;
}
:deep(.el-menu-item:hover) {
  background-color: transparent;
  font-weight: bold !important;
  color: #666;
}
a {
  text-decoration: none;
  color: #333;
  font-size: 30px;
  line-height: 80px;
  background-image: linear-gradient(45deg, red 30%, #2575fc);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  height: 80px;
  display: block;
  margin-top: 10px;
  text-align: left;
  padding-left: 35px;
}
.logo {
  width: 50px;
  margin-right: 0 !important;
  vertical-align: top;
  margin-top: 10px;
}
:deep(.el-menu-item.is-active) {
  color: #000;
  font-weight: bold;
}
.hidden {
  padding-left: 0 !important;
}
:deep(.hidden .el-menu-tooltip__trigger) {
  padding-left: 12px !important;
}
@media screen and (max-width: 1000px) {
  a {
    padding-left: 0 !important;
  }
  :deep(.el-menu-tooltip__trigger) {
    padding-left: 12px !important;
  }
  :deep(.el-drawer) {
    width: 60% !important;
  }
  :deep(.el-menu-item) {
    padding-left: 12px !important;
  }
}
</style>
