

<template>
  <div class="section-head" >
      <div>{{title}}</div>
      <div class="section-head-line"></div>
      <div class="section-head-des">{{des}}</div>
  </div>
</template>

<script>

export default {
  name: "SectionHead",
  props: {
    "title": {
      type: String
    },
    "des": {
      type: String
    } 
  }
};
</script>
<style scoped lang="less">
@import "../../../assets/less/main";
.section-head{
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    margin-bottom:40px;
    .fz(@fontSize18);
    .section-head-line{
        width: 100px;
        border-bottom: 1px solid @colorBj333;
        margin: 5px 0;
    }
    .section-head-des{
        .fz(@fontSize14);
        color:@colorFont999;
    }
}
</style>
