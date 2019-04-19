<template>
  <ul>
    <li v-for="(itemGoods, index) in goodsList" :key="index" @click.stop.prevent="click(itemGoods)">
      <div class="goods-pic">
        <img :src="itemGoods.picture">
      </div>
      <div class="goods-down-info">
        <div class="goods-title">{{itemGoods.goodsName}}</div>
        <div class="goods-price">
          ¥
          {{itemGoods.leaseMinPrice | priceFormat}}
          <span
            class="mounth-day"
          >/{{itemGoods.unit | unitPipe}}</span>
        </div>
      </div>
    </li>
  </ul>
</template>

<script>
import { unitPipe, priceFormat } from "@/vueFuntion/vueFilter";
import CommodityItemModel from "./CommodityItemModel";

export default {
  name: "CommodityListModel",
  props: {
    goodsList: {
      type: Array
    }
  },
  components: {
    CommodityItemModel
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
ul {
  .size(1200px, auto);
  margin: 70px auto;
  display: flex;
  flex-wrap: wrap;
  flex-direction: row;
  li {
    .size(25%, auto);
    border: 1px solid @colorBjE6E;
    margin: 0px -1px -1px 0px;
    .goods-pic {
      .size(100%, 220px);
      .center(flex);
      img {
        .size(130px, 130px);
      }
    }
    .goods-down-info {
      margin: 20px 0;
      line-height: 40px;
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
  li:hover{
      box-shadow:0 0 10px #ccc ;
  }
}
</style>
