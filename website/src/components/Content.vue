<template>
  <div class="Content">
    <div class="oDiv" ref="jump1">
      <label><img :src="saveIcon" alt="icon" /> 星火推荐</label>
      <el-row :gutter="12">
        <el-col :span="6">
          <el-card shadow="hover" @click="changeDialog">
            <img src="../assets/wechat.jpg" class="image" />
            <div class="text">
              <p>公众号 - 星火 Spark Coder</p>
              <span>扫码关注</span>
            </div>
          </el-card>
        </el-col>
        <el-col :span="6">
          <el-card shadow="hover" @click="changeXQDialog">
            <img src="../assets/xingqiuIcon.jpg" class="image" />
            <div class="text">
              <p>知识星球 - 星火 Spark</p>
              <span>连接一千位铁杆粉丝</span>
            </div>
          </el-card>
        </el-col>
        <el-col :span="6">
          <a href="https://www.zhihu.com/people/56-48-48-61" target="_blank">
            <el-card shadow="hover">
              <img src="../assets/zhihu.png" class="image" />
              <div class="text">
                <p>知乎 - 星火 Spark Coder 频道</p>
                <span>有问题，就会有答案</span>
              </div>
            </el-card>
          </a>
        </el-col>
      </el-row>
    </div>
    <div class="oDiv" ref="jump2">
      <label><img :src="toolIcon" alt="icon" /> 常用工具</label>
      <el-row :gutter="12">
        <el-col :span="6">
          <a href="https://tool.lu/js/" target="_blank">
            <el-card shadow="hover">
              <img src="../assets/jsIcon.jpg" class="image" />
              <div class="text">
                <p>JavaScript工具</p>
                <span>在线Js美化、解压缩、混淆</span>
              </div>
            </el-card>
          </a>
        </el-col>
        <el-col :span="6">
          <a href="https://tool.lu/java/" target="_blank">
            <el-card shadow="hover">
              <img src="../assets/javaIcon.jpg" class="image" />
              <div class="text">
                <p>Java在线工具</p>
                <span>Java代码在线美化</span>
              </div>
            </el-card>
          </a>
        </el-col>
        <el-col :span="6">
          <a href="https://tool.lu/pyc/" target="_blank">
            <el-card shadow="hover">
              <img src="../assets/pythonIcon.jpg" class="image" />
              <div class="text">
                <p>python工具</p>
                <span>python文件反编译、格式化</span>
              </div>
            </el-card>
          </a>
        </el-col>
        <el-col :span="6">
          <a href="https://tool.lu/sql/" target="_blank">
            <el-card shadow="hover">
              <img src="../assets/sqlIcon.jpg" class="image" />
              <div class="text">
                <p>SQL工具</p>
                <span>SQL在线美化、格式化、压缩</span>
              </div>
            </el-card>
          </a>
        </el-col>
      </el-row>
      <el-row :gutter="12">
        <el-col :span="6">
          <a href="https://c.runoob.com/" target="_blank">
            <el-card shadow="hover">
              <img src="../assets/caiIcon.jpg" class="image" />
              <div class="text">
                <p>菜鸟工具</p>
                <span>不止于工具</span>
              </div>
            </el-card>
          </a>
        </el-col>
        <el-col :span="6">
          <a href="https://tinypng.com/" target="_blank">
            <el-card shadow="hover">
              <img src="../assets/tinypngIcon.jpg" class="image" />
              <div class="text">
                <p>TinyPNG</p>
                <span>智能压缩您的webp、jpeg和png图片</span>
              </div>
            </el-card>
          </a>
        </el-col>
        <el-col :span="6">
          <a href="https://www.processon.com/" target="_blank">
            <el-card shadow="hover">
              <img src="../assets/ProcessOnIcon.jpg" class="image" />
              <div class="text">
                <p>ProcessOn</p>
                <span>免费在线流程图思维导图</span>
              </div>
            </el-card>
          </a>
        </el-col>
        <el-col :span="6">
          <a href="https://cn.bing.com/" target="_blank">
            <el-card shadow="hover">
              <img src="../assets/bingIcon.jpg" class="image" />
              <div class="text">
                <p>Bing</p>
                <span>全球领先的搜索引擎之一</span>
              </div>
            </el-card>
          </a>
        </el-col>
      </el-row>
      <el-row :gutter="12">
        <el-col :span="6">
          <a href="https://jakearchibald.github.io/svgomg/" target="_blank">
            <el-card shadow="hover">
              <img src="../assets/svgomg.jpg" class="image" />
              <div class="text">
                <p>SVGOMG</p>
                <span>SVG在线压缩平台</span>
              </div>
            </el-card>
          </a>
        </el-col>
        <el-col :span="6">
          <a href="https://www.aliyun.com/" target="_blank">
            <el-card shadow="hover">
              <img src="../assets/aliyun.jpg" class="image" />
              <div class="text">
                <p>阿里云</p>
                <span>为了无法计算的价值</span>
              </div>
            </el-card>
          </a>
        </el-col>
        <el-col :span="6">
          <a href="https://cloud.tencent.com/" target="_blank">
            <el-card shadow="hover">
              <img src="../assets/tengxun.jpg" class="image" />
              <div class="text">
                <p>腾讯云</p>
                <span>产业数字化助手</span>
              </div>
            </el-card>
          </a>
        </el-col>
      </el-row>
    </div>
    <div class="oDiv" ref="jump3">
      <label><img :src="devIcon" alt="icon" /> 开发设计</label>
      <el-row :gutter="12">
        <el-col :span="6">
          <a href="http://iconfont.cn/" target="_blank">
            <el-card shadow="hover">
              <img src="../assets/iconfontIcon.jpg" class="image" />
              <div class="text">
                <p>iconfont</p>
                <span>阿里巴巴矢量图标库</span>
              </div>
            </el-card>
          </a>
        </el-col>
        <el-col :span="6">
          <a href="https://fontawesome.com/icons/" target="_blank">
            <el-card shadow="hover">
              <img src="../assets/fontIcon.jpg" class="image" />
              <div class="text">
                <p>Font Awesome</p>
                <span>一套绝佳的图标字体库和CSS框架</span>
              </div>
            </el-card>
          </a>
        </el-col>
        <el-col :span="6">
          <a href="https://www.fastmock.site/#/" target="_blank">
            <el-card shadow="hover">
              <img src="../assets/fastIcon.jpg" class="image" />
              <div class="text">
                <p>Fast Mock</p>
                <span>简单好用的在线接口mock平台</span>
              </div>
            </el-card>
          </a>
        </el-col>
        <el-col :span="6">
          <a href="https://www.jq22.com/textDifference" target="_blank">
            <el-card shadow="hover">
              <img src="../assets/jqIcon.jpg" class="image" />
              <div class="text">
                <p>文本比较</p>
                <span>极速高效的在线文本对比工具</span>
              </div>
            </el-card>
          </a>
        </el-col>
      </el-row>
      <el-row :gutter="12">
        <el-col :span="6">
          <a href="https://www.logosc.cn/" target="_blank">
            <el-card shadow="hover">
              <img src="../assets/logoIcon.jpg" class="image" />
              <div class="text">
                <p>标小智</p>
                <span>智能Logo设计生成器</span>
              </div>
            </el-card>
          </a>
        </el-col>
        <el-col :span="6">
          <a href="https://www.postman.com/" target="_blank">
            <el-card shadow="hover">
              <img src="../assets/postmanIcon.jpg" class="image" />
              <div class="text">
                <p>Postman</p>
                <span>API & HTTP 请求调试插件</span>
              </div>
            </el-card>
          </a>
        </el-col>
        <el-col :span="6">
          <a href="https://ps.gaoding.com/#/" target="_blank">
            <el-card shadow="hover">
              <img src="../assets/gaoIcon.jpg" class="image" />
              <div class="text">
                <p>搞定 - 在线PS</p>
                <span>在线PS专业版</span>
              </div>
            </el-card>
          </a>
        </el-col>
        <el-col :span="6">
          <a href="https://hellosean1025.github.io/yapi/" target="_blank">
            <el-card shadow="hover">
              <img src="../assets/yapiIcon.jpg" class="image" />
              <div class="text">
                <p>Yapi</p>
                <span>高效、易用、功能强大的可视化接口管理平台</span>
              </div>
            </el-card>
          </a>
        </el-col>
      </el-row>
    </div>
    <div class="oDiv" ref="jump4">
      <label><img :src="wangpanIcon" alt="icon" /> 网盘资源</label>
      <el-row :gutter="12">
        <el-col :span="6">
          <a href="https://pan.baidu.com/" target="_blank">
            <el-card shadow="hover">
              <img src="../assets/baiduIcon.jpg" class="image" />
              <div class="text">
                <p>百度网盘</p>
                <span>记录每一份热爱</span>
              </div>
            </el-card>
          </a>
        </el-col>
      </el-row>
    </div>
    <div class="oDiv" ref="jump5">
      <label><img :src="communityIcon" alt="icon" /> 技术社区</label>
      <el-row :gutter="12">
        <el-col :span="6">
          <a href="https://www.csdn.net/" target="_blank">
            <el-card shadow="hover">
              <img src="../assets/csdnIcon.jpg" class="image" />
              <div class="text">
                <p>CSDN</p>
                <span>专业开发者社区</span>
              </div>
            </el-card>
          </a>
        </el-col>
        <el-col :span="6">
          <a href="https://www.oschina.net" target="_blank">
            <el-card shadow="hover">
              <img src="../assets/oschinaIcon.jpg" class="image" />
              <div class="text">
                <p>OSCHINA</p>
                <span>中文开源技术交流社区</span>
              </div>
            </el-card>
          </a>
        </el-col>
        <el-col :span="6">
          <a href="https://segmentfault.com/" target="_blank">
            <el-card shadow="hover">
              <img src="../assets/sfIcon.jpg" class="image" />
              <div class="text">
                <p>SegmentFault</p>
                <span>中国领先的开发者技术社区</span>
              </div>
            </el-card>
          </a>
        </el-col>
        <el-col :span="6">
          <a href="https://www.v2ex.com/" target="_blank">
            <el-card shadow="hover">
              <img src="../assets/v2Icon.jpg" class="image" />
              <div class="text">
                <p>V2EX</p>
                <span>创意工作者们的社区</span>
              </div>
            </el-card>
          </a>
        </el-col>
      </el-row>
      <el-row :gutter="12">
        <el-col :span="6">
          <a href="https://juejin.cn/" target="_blank">
            <el-card shadow="hover">
              <img src="../assets/jueIcon.jpg" class="image" />
              <div class="text">
                <p>掘金</p>
                <span>面向全球中文开发者的技术内容分享与交流平台</span>
              </div>
            </el-card>
          </a>
        </el-col>
        <el-col :span="6">
          <a href="https://www.cnblogs.com/" target="_blank">
            <el-card shadow="hover">
              <img src="../assets/blogIcon.jpg" class="image" />
              <div class="text">
                <p>博客园</p>
                <span>开发者的网上家园</span>
              </div>
            </el-card>
          </a>
        </el-col>
        <el-col :span="6">
          <a href="https://gitee.com/" target="_blank">
            <el-card shadow="hover">
              <img src="../assets/giteeIcon.jpg" class="image" />
              <div class="text">
                <p>Gitee</p>
                <span>基于Git的代码托管和研发协作平台</span>
              </div>
            </el-card>
          </a>
        </el-col>
      </el-row>
    </div>
    <div class="oDiv" ref="jump6">
      <label><img :src="learnIcon" alt="icon" /> 学习教程</label>
      <el-row :gutter="12">
        <el-col :span="6">
          <a href="https://www.imooc.com/" target="_blank">
            <el-card shadow="hover">
              <img src="../assets/muIcon.jpg" class="image" />
              <div class="text">
                <p>慕课网</p>
                <span>程序员的梦工厂</span>
              </div>
            </el-card>
          </a>
        </el-col>
        <el-col :span="6">
          <a href="https://www.w3cschool.cn/" target="_blank">
            <el-card shadow="hover">
              <img src="../assets/w3cIcon.jpg" class="image" />
              <div class="text">
                <p>W3Cschool</p>
                <span>随时随地学编程</span>
              </div>
            </el-card>
          </a>
        </el-col>
        <el-col :span="6">
          <a href="https://www.runoob.com/" target="_blank">
            <el-card shadow="hover">
              <img src="../assets/caiIcon.jpg" class="image" />
              <div class="text">
                <p>菜鸟教程</p>
                <span>学的不仅是技术,更是梦想!</span>
              </div>
            </el-card>
          </a>
        </el-col>
        <el-col :span="6">
          <a href="https://www.naixuejiaoyu.com/" target="_blank">
            <el-card shadow="hover">
              <img src="../assets/naiIcon.jpg" class="image" />
              <div class="text">
                <p>奈学教育</p>
                <span>IT职业能力提升的在线教育平台</span>
              </div>
            </el-card>
          </a>
        </el-col>
      </el-row>
    </div>
    <el-dialog
      v-model="qrcodeDialog"
      title="星火 Spark Coder 公众号"
      width="300px"
      align-center
      :close-on-click-modal="false"
      :close-on-press-escape="false"
      :before-close="closeBtn"
      :close-delay="300"
    >
      <span><img src="../assets/qrcode.jpg" alt="qrcode" /></span>
    </el-dialog>
    <el-dialog
      v-model="xingqiuDialog"
      title="星火 Spark 知识星球"
      width="300px"
      align-center
      :close-on-click-modal="false"
      :close-on-press-escape="false"
      :before-close="closeXQBtn"
      :close-delay="300"
    >
      <span><img src="../assets/xingqiu.jpg" alt="xingqiu" /></span>
    </el-dialog>
  </div>
</template>

<script>
export default {
  name: "Content",
  data() {
    return {
      navIcon: require("../assets/nav.svg"),
      saveIcon: require("../assets/save.svg"),
      toolIcon: require("../assets/tool.svg"),
      devIcon: require("../assets/dev.svg"),
      wangpanIcon: require("../assets/wangpan.svg"),
      communityIcon: require("../assets/community.svg"),
      learnIcon: require("../assets/learn.svg"),
      aboutIcon: require("../assets/about.svg"),
      qrcodeDialog: false,
      xingqiuDialog: false,
    };
  },
  methods: {
    changeDialog() {
      this.qrcodeDialog = true;
      this.$emit("handleDialog", true);
    },
    closeBtn() {
      this.qrcodeDialog = false;
      setTimeout(() => {
        this.$emit("handleDialog", false);
      }, 500);
    },
    changeXQDialog() {
      this.xingqiuDialog = true;
      this.$emit("handleDialog", true);
    },
    closeXQBtn() {
      this.xingqiuDialog = false;
      setTimeout(() => {
        this.$emit("handleDialog", false);
      }, 500);
    },
    toJump1() {
      this.$refs["jump1"].scrollIntoView(true);
      this.$emit("handleClose", false);
    },
    toJump2() {
      this.$refs["jump2"].scrollIntoView(true);
      this.$emit("handleClose", false);
    },
    toJump3() {
      this.$refs["jump3"].scrollIntoView(true);
      this.$emit("handleClose", false);
    },
    toJump4() {
      this.$refs["jump4"].scrollIntoView(true);
      this.$emit("handleClose", false);
    },
    toJump5() {
      this.$refs["jump5"].scrollIntoView(true);
      this.$emit("handleClose", false);
    },
    toJump6() {
      this.$refs["jump6"].scrollIntoView(true);
      this.$emit("handleClose", false);
    },
  },
};
</script>

<style scoped>
.Content {
  padding: 20px;
}
:deep(.el-card__body) {
  cursor: pointer;
}
.oDiv {
  margin-bottom: 40px;
}
.oDiv label {
  display: block;
  margin-bottom: 20px;
  padding-top: 80px;
  margin-top: -80px;
}
.oDiv label img {
  width: 24px;
  vertical-align: middle;
  margin-top: -4px;
}
.oDiv a {
  text-decoration: none;
}
.image {
  width: 40px;
  height: 40px;
  display: inline-block;
  vertical-align: middle;
}
.text {
  display: inline-block;
  vertical-align: middle;
  margin-left: 10px;
  width: calc(100% - 60px);
}
.text p {
  margin: 0;
  font-size: 16px;
  font-weight: bold;
  color: #000;
  overflow: hidden;
  text-overflow: ellipsis;
  white-space: nowrap;
}
.text span {
  font-size: 12px;
  color: #6c757d;
  overflow: hidden;
  text-overflow: ellipsis;
  display: -webkit-box;
  -webkit-line-clamp: 1;
  -webkit-box-orient: vertical;
}
.el-dialog img {
  width: 100%;
}
:deep(.el-col) {
  margin-bottom: 10px;
}
@media screen and (max-width: 1000px) {
  .Content {
    padding: 10px;
  }
  :deep(.el-col) {
    max-width: 100% !important;
    margin-bottom: 10px;
    flex: 0 0 100% !important;
  }
  :deep(.el-card__body) {
    padding: 10px;
  }
  .image {
    width: 30px;
    height: 30px;
  }
  .text p {
    font-size: 0.9rem !important;
  }
  .text span {
    font-size: 0.7rem !important;
  }
}
</style>
