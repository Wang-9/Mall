<!--
 * @Description: 首页组件
 -->
<template>
  <div class="home" id="home" name="home">
    <!-- 轮播图 -->
    <div class="block">
      <el-carousel height="460px">
        <el-carousel-item v-for="item in carousel" :key="item.carousel_id">
          <img style="height:460px;" :src="$target + item.imgPath" :alt="item.describes" />
        </el-carousel-item>
      </el-carousel>
      <div class="leftnav">
        <ul>
          <li @mouseover="shownav" @mouseout="disshow">手机 电话卡
          <div class="inside" v-show="isshow" >
            <ul>
              <li><a href="#"><span>K30</span></a></li>
              <li><a href="#"><span>red</span></a></li>
              <li><a href="#"><span>K30</span></a></li>
              <li><a href="#"><span>K30</span></a></li>
              <li><a href="#"><span>K30</span></a></li>
              <li><a href="#"><span>K30</span></a></li>
            </ul>
          </div>
          </li>
          <li @mouseover="shownav" @mouseout="disshow">电视 盒子
            <div class="inside" v-show="isshow" >
            <ul>
              <li><a href="#"><span>redmi</span></a></li>
              <li><a href="#"><span>redmi</span></a></li>
              <li><a href="#"><span>redmi</span></a></li>
              <li><a href="#"><span>redmi</span></a></li>
              <li><a href="#"><span>redmi</span></a></li>
              <li><a href="#"><span>redmi</span></a></li>
            </ul>
          </div>
          </li>
          <li @mouseover="shownav" @mouseout="disshow">笔记本 显示器
            <div class="inside" v-show="isshow" >
            <ul>
              <li><a href="#"><span>K30</span></a></li>
              <li><a href="#"><span>K30</span></a></li>
              <li><a href="#"><span>K30</span></a></li>
              <li><a href="#"><span>K30</span></a></li>
              <li><a href="#"><span>K30</span></a></li>
              <li><a href="#"><span>K30</span></a></li>
            </ul>
          </div>
          </li>
          <li @mouseover="shownav" @mouseout="disshow">家电 插线板
            <div class="inside" v-show="isshow" >
            <ul>
              <li><a href="#"><span>K30</span></a></li>
              <li><a href="#"><span>K30</span></a></li>
              <li><a href="#"><span>K30</span></a></li>
              <li><a href="#"><span>K30</span></a></li>
              <li><a href="#"><span>K30</span></a></li>
              <li><a href="#"><span>K30</span></a></li>
            </ul>
          </div>
          </li>
          <li @mouseover="shownav" @mouseout="disshow">出行 穿戴
            <div class="inside" v-show="isshow" >
            <ul>
              <li><a href="#"><span>K30</span></a></li>
              <li><a href="#"><span>K30</span></a></li>
              <li><a href="#"><span>K30</span></a></li>
              <li><a href="#"><span>K30</span></a></li>
              <li><a href="#"><span>K30</span></a></li>
              <li><a href="#"><span>K30</span></a></li>
            </ul>
          </div>
          </li>
          <li @mouseover="shownav" @mouseout="disshow">智能 路由器
            <div class="inside" v-show="isshow" >
            <ul>
              <li><a href="#"><span>K30</span></a></li>
              <li><a href="#"><span>K30</span></a></li>
              <li><a href="#"><span>K30</span></a></li>
              <li><a href="#"><span>K30</span></a></li>
              <li><a href="#"><span>K30</span></a></li>
              <li><a href="#"><span>K30</span></a></li>
            </ul>
          </div>
          </li>
          <li @mouseover="shownav" @mouseout="disshow">电源 配件
            <div class="inside" v-show="isshow" >
            <ul>
              <li><a href="#"><span>K30</span></a></li>
              <li><a href="#"><span>K30</span></a></li>
              <li><a href="#"><span>K30</span></a></li>
              <li><a href="#"><span>K30</span></a></li>
              <li><a href="#"><span>K30</span></a></li>
              <li><a href="#"><span>K30</span></a></li>
            </ul>
          </div>
          </li>
          <li @mouseover="shownav" @mouseout="disshow">健康 儿童
            <div class="inside" v-show="isshow" >
            <ul>
              <li><a href="#"><span>K30</span></a></li>
              <li><a href="#"><span>K30</span></a></li>
              <li><a href="#"><span>K30</span></a></li>
              <li><a href="#"><span>K30</span></a></li>
              <li><a href="#"><span>K30</span></a></li>
              <li><a href="#"><span>K30</span></a></li>
            </ul>
          </div>
          </li>
          <li @mouseover="shownav" @mouseout="disshow">耳机 音箱
            <div class="inside" v-show="isshow" >
            <ul>
              <li><a href="#"><span>K30</span></a></li>
              <li><a href="#"><span>K30</span></a></li>
              <li><a href="#"><span>K30</span></a></li>
              <li><a href="#"><span>K30</span></a></li>
              <li><a href="#"><span>K30</span></a></li>
              <li><a href="#"><span>K30</span></a></li>
            </ul>
          </div>
          </li>
          <li @mouseover="shownav" @mouseout="disshow">生活 箱包
            <div class="inside" v-show="isshow" >
            <ul>
              <li><a href="http://localhost:8080/#/goods/details?productID=1"><span>Redmi K30</span></a></li>
              <li><a href="http://localhost:8080/#/goods/details?productID=3"><span>小米CC9 Pro</span></a></li>
              <li><a href="http://localhost:8080/#/goods/details?productID=9"><span>小米电视4A 32英寸</span></a></li>
              <li><a href="http://localhost:8080/#/goods/details?productID=23"><span>小米USB充电器30W快充版</span></a></li>
              <li><a href="http://localhost:8080/#/goods/details?productID=30"><span>小米无线充电宝青春版</span></a></li>
              <li><a href="http://localhost:8080/#/goods/details?productID=22"><span>小米CC9e 标准高透贴膜</span></a></li>
            </ul>
          </div>
          </li>
        </ul>
      </div>
      <div class="tuijian">
        <div class="span1">推&nbsp;&nbsp;荐</div>
        <div class="span2">
          <ul class="pailie2">
            <li><img src="../assets/imgs/6.png"></li>
            <li><img src="../assets/imgs/7.png"></li>
            <li><img src="../assets/imgs/8.png"></li>
          </ul>
        </div>
      </div>
    </div>
    
    <!-- 轮播图END -->
    <div class="main-box">
      <div class="main">
        <!-- 手机商品展示区域 -->
        <div class="phone">
          <div class="box-hd">
            <div class="title">手机</div>
          </div>
          <div class="box-bd">
            <div class="promo-list">
              <router-link to>
                <img :src="$target +'public/imgs/phone/phone.png'" />
              </router-link>
            </div>
            <div class="list">
              <MyList :list="phoneList" :isMore="true"></MyList>
            </div>
          </div>
        </div>
        <!-- 手机商品展示区域END -->

        <!-- 家电商品展示区域 -->
        <div class="appliance" id="promo-menu">
          <div class="box-hd">
            <div class="title">家电</div>
            <div class="more" id="more">
              <MyMenu :val="2" @fromChild="getChildMsg">
                <span slot="1">热门</span>
                <span slot="2">电视影音</span>
              </MyMenu>
            </div>
          </div>
          <div class="box-bd">
            <div class="promo-list">
              <ul>
                <li>
                  <img :src="$target +'public/imgs/appliance/appliance-promo1.png'" />
                </li>
                <li>
                  <img :src="$target +'public/imgs/appliance/appliance-promo2.png'" />
                </li>
              </ul>
            </div>
            <div class="list">
              <MyList :list="applianceList" :isMore="true"></MyList>
            </div>
          </div>
        </div>
        <!-- 家电商品展示区域END -->

        <!-- 配件商品展示区域 -->
        <div class="accessory" id="promo-menu">
          <div class="box-hd">
            <div class="title">配件</div>
            <div class="more" id="more">
              <MyMenu :val="3" @fromChild="getChildMsg2">
                <span slot="1">热门</span>
                <span slot="2">保护套</span>
                <span slot="3">充电器</span>
              </MyMenu>
            </div>
          </div>
          <div class="box-bd">
            <div class="promo-list">
              <ul>
                <li>
                  <img :src="$target +'public/imgs/accessory/accessory-promo1.png'" alt />
                </li>
                <li>
                  <img :src="$target +'public/imgs/accessory/accessory-promo2.png'" alt />
                </li>
              </ul>
            </div>
            <div class="list">
              <MyList :list="accessoryList" :isMore="true"></MyList>
            </div>
          </div>
        </div>
        <!-- 配件商品展示区域END -->
      </div>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      carousel: "", // 轮播图数据
      phoneList: "", // 手机商品列表
      miTvList: "", // 小米电视商品列表
      applianceList: "", // 家电商品列表
      applianceHotList: "", //热门家电商品列表
      accessoryList: "", //配件商品列表
      accessoryHotList: "", //热门配件商品列表
      protectingShellList: "", // 保护套商品列表
      chargerList: "", //充电器商品列表
      applianceActive: 1, // 家电当前选中的商品分类
      accessoryActive: 1,// 配件当前选中的商品分类
      isshow: false,
    };
  },
  watch: {
    // 家电当前选中的商品分类，响应不同的商品数据
    applianceActive: function(val) {
      // 页面初始化的时候把applianceHotList(热门家电商品列表)直接赋值给applianceList(家电商品列表)
      // 所以在切换商品列表时判断applianceHotList是否为空,为空则是第一次切换,把applianceList赋值给applianceHotList
      if (this.applianceHotList == "") {
        this.applianceHotList = this.applianceList;
      }
      if (val == 1) {
        // 1为热门商品
        this.applianceList = this.applianceHotList;
        return;
      }
      if (val == 2) {
        // 2为电视商品
        this.applianceList = this.miTvList;
        return;
      }
    },
    accessoryActive: function(val) {
      // 页面初始化的时候把accessoryHotList(热门配件商品列表)直接赋值给accessoryList(配件商品列表)
      // 所以在切换商品列表时判断accessoryHotList是否为空,为空则是第一次切换,把accessoryList赋值给accessoryHotList
      if (this.accessoryHotList == "") {
        this.accessoryHotList = this.accessoryList;
      }
      if (val == 1) {
        // 1为热门商品
        this.accessoryList = this.accessoryHotList;
        return;
      }
      if (val == 2) {
        // 2为保护套商品
        this.accessoryList = this.protectingShellList;
        return;
      }
      if (val == 3) {
        //3 为充电器商品
        this.accessoryList = this.chargerList;
        return;
      }
    }
  },
  created() {
    // 获取轮播图数据
    this.$axios
      .post("/api/resources/carousel", {})
      .then(res => {
        this.carousel = res.data.carousel;
      })
      .catch(err => {
        return Promise.reject(err);
      });
    // 获取各类商品数据
    this.getPromo("手机", "phoneList");
    this.getPromo("电视机", "miTvList");
    this.getPromo("保护套", "protectingShellList");
    this.getPromo("充电器", "chargerList");
    this.getPromo(
      ["电视机", "空调", "洗衣机"],
      "applianceList",
      "/api/product/getHotProduct"
    );
    this.getPromo(
      ["保护套", "保护膜", "充电器", "充电宝"],
      "accessoryList",
      "/api/product/getHotProduct"
    );
  },
  methods: {
    // 获取家电模块子组件传过来的数据
    getChildMsg(val) {
      this.applianceActive = val;
    },
    // 获取配件模块子组件传过来的数据
    getChildMsg2(val) {
      this.accessoryActive = val;
    },
    // 获取各类商品数据方法封装
    getPromo(categoryName, val, api) {
      api = api != undefined ? api : "/api/product/getPromoProduct";
      this.$axios
        .post(api, {
          categoryName
        })
        .then(res => {
          this[val] = res.data.Product;
        })
        .catch(err => {
          return Promise.reject(err);
        });
    },
    shownav(){
      this.isshow=true;
    },
    disshow(){
      this.isshow=false;
    }
  }
};
</script>
<style scoped>
@import "../assets/css/index.css";
</style>