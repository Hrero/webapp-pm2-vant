<template>
  <div>

  </div>
</template>

<script>
import { unitPipe, priceFormat } from "@/vueFuntion/vueFilter";

export default {
  name: "CommodityItemModel",
  props: {
    goodsList: {
      type: Array
    }
  },
  mounted() {
    this.$emit("componentDidMount"); // 组件加载成功的回调
  },
  methods: {
    click() {
      this.$emit("click", itemGoods); // 组件点击事件的触发
    }
  }
};
</script>
<style scoped lang="less">
@import "../assets/less/main";
div {
  .size(100%, auto);
                margin-bottom:-1px ;
  li {
    .size(25%, auto);
    .goods-pic {
      .size(100%, auto);
      padding: 20px 0;
      img {
        .size(100px, auto);
        min-height: 100px;
      }
    }
    .goods-down-info {
      padding: 0.25rem;
      .goods-title {
        color: @colorFont333;
        font-size: @fontSize14;
      }
      .goods-price {
        font-size: @fontSize14;
        color: @colorFontF60;
        font-weight: bold;
      }
      .mounth-day {
        color: @colorFontF60;
        font-size: @fontSize12;
      }
    }
  }
}
</style>
