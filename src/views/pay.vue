<!--
*支付订单
-->
<template>
    <div class="zf">
        <div class="zleft">
            <img src="../assets/imgs/zffs.png">
        </div>
        <div class="zright">
            <img src="../assets/imgs/ewm.png">
            <br>
            <button @click="addOrder">我已完成支付</button>
        </div>
    </div>
</template>

<script>
import { mapGetters } from "vuex";
import { mapActions } from "vuex";
export default {
    name: "",
    computed: {
    // 结算的商品数量; 结算商品总计; 结算商品信息
    ...mapGetters(["getCheckNum", "getTotalPrice", "getCheckGoods"])
    },
    methods: {
    ...mapActions(["deleteShoppingCart"]),
    addOrder() {
      this.$axios
        .post("/api/user/order/addOrder", {
          user_id: this.$store.getters.getUser.user_id,
          products: this.getCheckGoods
        })
        .then(res => {
          let products = this.getCheckGoods;
          switch (res.data.code) {
            // “001”代表结算成功
            case "001":
              for (let i = 0; i < products.length; i++) {
                const temp = products[i];
                // 删除已经结算的购物车商品
                this.deleteShoppingCart(temp.id);
              }
              // 提示结算结果
              this.notifySucceed(res.data.msg);
              // 跳转我的订单页面
              this.$router.push({ path: "/order" });
              break;
            default:
              // 提示失败信息
              this.notifyError(res.data.msg);
          }
        })
        .catch(err => {
          return Promise.reject(err);
        });
    }
  }
};
</script>

<style>
.zf{
    width: 1225px;
}

.zleft{
    float: left;
}

.zright{
    float: right;
}
</style>