<template>
  <div class="About" ref="jump7">
    <div class="text">
      <h1>关于我们 - 星火是谁？</h1>
      <p>
        2022年互联网行业遭遇寒冬，很多同学被裁，招聘职位减少，期望薪资无法达标，面试难度提升....
      </p>
      <p>
        也许你是一位35+
        Coder，处于上有老下有小的你，面对房贷，车贷，孩子学费时，资金链断裂会牵一发而动全身
      </p>
      <p>也许你是一位刚初为人父/人母的Coder，突然失业会打的你措手不及</p>
      <p>
        也许你是一位刚刚步入职场的年轻Coder，本来雄心壮志却遭遇了刚毕业即失业的不堪
      </p>
      <p>
        现实中许多人数月都没有面试机会，或者面试被pass的次数比之前明显提升，这时我们难免会自我怀疑，烦闷，焦虑，感觉压力压的我们喘不过气
      </p>
      <p>
        也许你可以加入我们，我们希望能在这寒冬之中传递出一把火，点燃希望，照亮前路，分享求职经验，提供就业机会。让每一位在求职之路上的Coder可以走的更稳更远
      </p>
      <p>
        同时也希望可以帮助渴望创业的Coder们，止于想，敢于行！大家一起出谋划策，共襄盛举。
      </p>
      <p>我们的初衷是凝聚每一位Coder，不光用代码改变世界，更能用代码温暖人心</p>

      <p>请问，你还相信光吗？</p>
      <p>
        <img src="../assets/qrcode.jpg" alt="qrcode" />
        <img src="../assets/xingqiu.jpg" alt="qrcode" />
      </p>
    </div>
  </div>
</template>

<script>
export default {
  name: "About",
  methods: {
    toJump7() {
      this.$refs["jump7"].scrollIntoView(true);
      this.$emit("handleClose", false);
    },
  },
};
</script>
<style scoped>
.About {
  padding: 0 20px;
}
.text {
  max-width: 1000px;
  margin: 0 auto;
  padding-top: 40px;
  margin-top: 0px;
}
img {
  width: 200px;
  margin: 0 20px 0 0;
}
@media screen and (max-width: 1000px) {
  .About {
    padding: 10px;
  }
  img {
    width: 200px;
    margin: 0 auto;
  }
}
</style>
