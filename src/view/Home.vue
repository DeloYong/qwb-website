<template>
  <div id="HomePage" class="wow fadeIn" data-wow-duration="1s" data-wow-delay="1s">
    <!-- 轮播图 -->
    <div id="swiper" class="container-fuild">
      <div class="swiper-container banner-swiper">
        <div class="swiper-wrapper">
          <div class="swiper-slide" v-for="(item,index) in swiperList" :key="index">
            <img class="swiper-lazy" src="">
            <div class="video-container">
              <video autoplay loop muted>
                <source src="@/assets/img/video/earth.mp4" type="video/mp4">
                Your browser does not support the video tag.
              </video>
            </div>
            <div class="swiper-lazy-preloader"></div>
            <div class="swiper-slide-title">
                <p class="tt1">{{item.title}}</p>
                <p class="tt2">{{item.content}}</p>
                <p class="tt3">{{item.content2}}</p>
                <div class="btn">
                  <div class="btn-b1">下载免费版</div>
                  <div class="btn-b2">下载企业版</div>
                </div>
            </div>
          </div>
        </div>
      </div>
    </div>
    <!-- banner-nav -->
    <div class="banner-nav">
      <ul>
        <li>
          <img src="@/assets/img/场景1-进存销-1@2x.png">
          <span>
            进存销
          </span>
        </li>
        <li>
          <img src="@/assets/img/场景1-会计-1@2x.png">
          <span>
            智能会议
          </span>
        </li>
        <li>
          <img src="@/assets/img/场景1-商店-1@2x.png">
          <span>
            商品门店
          </span>
        </li>
        <li>
          <img src="@/assets/img/场景1-物流-1@2x.png">
          <span>
            物流配送
          </span>
        </li>
        <li>
          <img src="@/assets/img/场景1-外勤-1@2x.png">
          <span>
            业务外勤
          </span>
        </li>
      </ul>
    </div>
    <!-- 写作方式 -->
    <div id="writingStyle" class="container-fuild">
      <div class="writingStyle-container">
        <div class="common-title flxc">
          重新定义数字化写作方式
        </div>
        <div class="writingStyle-main flxc">
          <div class="nav-wrapper flxc">
            <div
              v-for="(item, index) in writingStyleNavList"
              :key="index"
              class="nav-wrapper-item flxc"
              :class="{ active: writingActiveIndex === index }"
              @click="setWritingActive(index)"
            >
              <img :src="item.img" />
              <p>{{item.title}}</p>
              <div v-if="writingActiveIndex === index" class="line"></div>
            </div>
          </div>
          <div class="writingStyle-main-content flxc">
            <div class="writingStyle-main-content-fll">
              <div class="ttl">
                赋能企业门店数字化技术使用
              </div>
              <div class="ct-list">
                <ul>
                  <li>
                    <div class="vector">
                      <img src="@/assets/img/Vector.png">
                    </div>
                    <span>有效降低订单执行成本</span>
                  </li>
                  <li>
                    <div class="vector">
                      <img src="@/assets/img/Vector.png">
                    </div>
                    <span>新渠道快速落地</span>
                  </li>
                  <li>
                    <div class="vector">
                      <img src="@/assets/img/Vector.png">
                    </div>
                    <span>数字化管理新渠道</span>
                  </li>
                  <li>
                    <div class="vector">
                      <img src="@/assets/img/Vector.png">
                    </div>
                    <span>全渠道会员精准营销</span>
                  </li>
                  <li>
                    <div class="vector">
                      <img src="@/assets/img/Vector.png">
                    </div>
                    <span>数字化管理新渠道</span>
                  </li>
                  <li>
                    <div class="vector">
                      <img src="@/assets/img/Vector.png">
                    </div>
                    <span>全渠道会员精准营销</span>
                  </li>
                  <li>
                    <div class="vector">
                      <img src="@/assets/img/Vector.png">
                    </div>
                    <span>数字化管理新渠道</span>
                  </li>
                  <li>
                    <div class="vector">
                      <img src="@/assets/img/Vector.png">
                    </div>
                    <span>全渠道会员精准营销</span>
                  </li>
                </ul>
              </div>
            </div>
            <div class="writingStyle-main-content-flr flxc">
              <img src="@/assets/img/插画-1-1@2x.png" alt="">
            </div>
          </div>
        </div>
      </div>
    </div>
    <!-- problem -->
    <div id="problem" class="container-fuild">
      <div class="problem-container">
        <div class="common-title flxc">
          您的企业是否面临这些难题
        </div>
        <div class="problem-main flxc">
          <ul>
            <li v-for="(item, index) in problemList" :key="index">
              <div class="top">
                <div class="ttl">
                  <p>{{item.ttl1}}</p>
                  <p>{{item.ttl2}}</p>
                </div>
                <div class="ttr">
                  <img :src="item.img" alt="">
                </div>
              </div>
              <div class="bottom">
                {{item.btt}}
              </div>
            </li>
          </ul>
        </div>
      </div>
      <div id="deal" class="problem-container" style="padding-top: 37px">
        <div class="common-title flxc">
          在企微宝，这些问题都能解决
        </div>
        <div class="common-title-tips flxc">轻流进销系统不仅提供了采购、销售、生成、库存管理的标准化解决方案，还打破了各板块间的数据信息壁垒，实现进、销、存、产一体化管理</div>
        <div class="deal-main flxc">
          <div class="nav-wrapper flxc">
            <div
              v-for="(item, index) in dealNavList"
              :key="index"
              class="nav-wrapper-item flxc"
              :class="{ active: dealActiveIndex === index }"
              @click="setDealActive(index)"
            >
              <img :src="item.img" />
              <span>{{item.title}}</span>
              <div v-if="dealActiveIndex === index" class="line"></div>
            </div>
          </div>
          <div class="deal-main-content">
            <div class="deal-main-content-fll">
              <div class="ttl">
                赋能企业门店数字化技术使用
              </div>
              <div class="ct-list">
                <ul>
                  <li v-for="(item, index) in dealCtList" :key="index">
                    <div class="vector">
                      <img :src="item.img">
                    </div>
                    <span>{{item.title}}</span>
                  </li>
                </ul>
              </div>
            </div>
            <div class="deal-main-content-flr flxc">
              <img src="@/assets/img/插画-2-1@2x.png" alt="">
            </div>
          </div>
        </div>
      </div>
    </div>
    <!-- 数字生态圈 -->
    <div id="math" class="container-fuild">
      <div class="math-container">
        <div class="common-title flxc">
          数字生态圈，契合多场景应用，一站式解决方案
        </div>
        <div class="math-content"></div>
      </div>
    </div>
    <!-- 多元化 -->
    <div class="dyh-main container-fuild">
      <div class="business-container">
        <div class="common-title flxc">
          丰富的业务模块，满足多元化需求
        </div>
        <div class="business-content flxc">
          <ul v-for="(item, index) in businessList" :key="index">
            <li v-for="(item2, index2) in item.children" :key="index2">
              <img :src="item2.img" alt="">
              <span>
                {{item2.title}}
              </span>
            </li>
          </ul>
        </div>
      </div>
      <!-- 食品 -->
      <div class="container-fuild">
        <div class="food-container">
          <div class="common-title flxc">
            快消、调味品、小食品渠道商专属数字化平台
          </div>
          <div class="food-content"></div>
        </div>
      </div>
    </div>
    <!-- 创业 -->
    <div class="container-fuild">
      <div class="start-container">
        <div class="common-title flxc">
          能陪你创业，也能陪你上市
        </div>
        <div class="start-content flxc">
          <ul>
            <li class="flxc">
              <div class="title">个人免费版</div>
              <div class="nr">
                <dl>
                  <dt>· 多人现在协作表格，收集处理数据</dt>
                  <dt>· 多人现在协作表格，收集处理数据</dt>
                  <dt>· 多人现在协作表格，收集处理数据</dt>
                  <dt>· 多人现在协作表格，收集处理数据</dt>
                </dl>
              </div>
              <div class="btn">
                免费试用
              </div>
            </li>
            <li class="flxc">
              <div class="title">个人免费版</div>
              <div class="nr">
                <dl>
                  <dt>· 多人现在协作表格，收集处理数据</dt>
                  <dt>· 多人现在协作表格，收集处理数据</dt>
                  <dt>· 多人现在协作表格，收集处理数据</dt>
                  <dt>· 多人现在协作表格，收集处理数据</dt>
                </dl>
              </div>
              <div class="btn">
                免费试用
              </div>
            </li>
            <li class="flxc">
              <div class="title">个人免费版</div>
              <div class="nr">
                <dl>
                  <dt>· 多人现在协作表格，收集处理数据</dt>
                  <dt>· 多人现在协作表格，收集处理数据</dt>
                  <dt>· 多人现在协作表格，收集处理数据</dt>
                  <dt>· 多人现在协作表格，收集处理数据</dt>
                </dl>
              </div>
              <div class="btn">
                免费试用
              </div>
            </li>
          </ul>
        </div>
      </div>
    </div>
    <!-- 上市 -->
    <div class="container-fuild">
      <div class="shangshi-container">
        <div class="common-title flxc">
          能陪你创业，也能陪你上市
        </div>
        <div class="shangshi-content">
          <div class="lfr">
            <div>
              <div class="ttl">
                智能ERP
              </div>
              <div class="desc">
                用户可通过扫码下单
              </div>
            </div>
            <div class="ct-list">
              <ul>
                <li v-for="(item, index) in erpCtList" :key="index">
                  <div class="vector">
                    <img :src="item.img">
                  </div>
                  <span>{{item.title}}</span>
                </li>
              </ul>
            </div>
            <div class="btn-b flxc">
              立即使用
            </div>
          </div>
          <div class="lfc">
            <div class="item">
              <div class="erp">商城版ERP</div>
              <div class="desc">支持认证客户，线下线上一体化下单</div>
              <a href="">立即使用 ></a>
            </div>
            <div class="item">
              <p class="erp">商城版ERP</p>
              <p class="desc">支持认证客户，线下线上一体化下单</p>
              <a href="">立即使用 ></a>
            </div>
          </div>
          <div class="lfc">
            <div class="item">
              <p class="erp">商城版ERP</p>
              <p class="desc">支持认证客户，线下线上一体化下单</p>
              <a href="">立即使用 ></a>
            </div>
            <div class="item">
              <p class="erp">商城版ERP</p>
              <p class="desc">支持认证客户，线下线上一体化下单</p>
              <a href="">立即使用 ></a>
            </div>
          </div>
        </div>
      </div>
    </div>
    <!-- 经销商 -->
    <div class="container-fuild">
      <div class="dealer-container">
        <div class="common-title flxc">
          他们的经销商都在用
        </div>
        <div class="dealer-content">
          <ul class="nava1">
            <li class="item1">
              <img src="@/assets/img/dealer/image@1x-2.png" alt="">
            </li>
            <li class="item1">
              <img src="@/assets/img/dealer/image@1x-3.png" alt="">
            </li>
            <li class="item1">
              <img src="@/assets/img/dealer/image@1x-4.png" alt="">
            </li>
            <li class="item1">
              <img src="@/assets/img/dealer/image@1x-5.png" alt="">
            </li>
            <li class="item1">
              <img src="@/assets/img/dealer/image@1x-6.png" alt="">
            </li>
            <li class="item1">
              <img src="@/assets/img/dealer/image@1x-7.png" alt="">
            </li>
          </ul>
          <ul class="nava1">
            <li class="item1">
              <img src="@/assets/img/dealer/image@1x-8.png" alt="">
            </li>
            <li class="item1">
              <img src="@/assets/img/dealer/image@1x-9.png" alt="">
            </li>
            <li class="item1">
              <img src="@/assets/img/dealer/image@1x-10.png" alt="">
            </li>
            <li class="item1">
              <img src="@/assets/img/dealer/image@1x-11.png" alt="">
            </li>
            <li class="item1">
              <img src="@/assets/img/dealer/image@1x-12.png" alt="">
            </li>
          </ul>
          <ul class="nava1">
            <li class="item1">
              <img src="@/assets/img/dealer/image@1x-13.png" alt="">
            </li>
            <li class="item1">
              <img src="@/assets/img/dealer/image@1x-14.png" alt="">
            </li>
            <li class="item1">
              <img src="@/assets/img/dealer/image@1x-15.png" alt="">
            </li>
            <li class="item1">
              <img src="@/assets/img/dealer/image@1x-16.png" alt="">
            </li>
            <li class="item1">
              <img src="@/assets/img/dealer/image@1x-17.png" alt="">
            </li>
            <li class="item1">
              <img src="@/assets/img/dealer/image@1x-18.png" alt="">
            </li>
          </ul>
          <ul class="nava1">
            <li class="item1">
              <img src="@/assets/img/dealer/image@1x-19.png" alt="">
            </li>
            <li class="item1">
              <img src="@/assets/img/dealer/image@1x-20.png" alt="">
            </li>
            <li class="item1">
              <img src="@/assets/img/dealer/image@1x-21.png" alt="">
            </li>
            <li class="item1">
              <img src="@/assets/img/dealer/image@1x-22.png" alt="">
            </li>
            <li class="item1">
              <img src="@/assets/img/dealer/image@1x.png" alt="">
            </li>
          </ul>
        </div>
      </div>
    </div>
    <!-- 供应商 -->
    <div id="deal" class="dealer-container">
      <div class="deal-main flxc">
        <div class="nav-wrapper flxc">
          <div
            v-for="(item, index) in dealerNavList"
            :key="index"
            class="nav-wrapper-item flxc"
            :class="{ active: supplierActiveIndex === index }"
            @click="setSupplierActive(index)"
          >
            <img :src="item.img" />
            <p>{{item.title}}</p>
            <div v-if="supplierActiveIndex === index" class="line"></div>
          </div>
        </div>
      </div>
    </div>
    <!-- 资讯 -->
    <div id="info" class="problem-container">
      <div class="common-title flxc">
        企微资讯
      </div>
      <div class="info-main">
        <div class="lfl">
           <div class="info-img">
            <img src="@/assets/img/house.png" alt="">
           </div>
           <div class="lfr-ct">
            <div class="ttl">
              成都在远方供应链，企微宝如何助力物流转型三方仓日发货9万单？
            </div>
            <span>
              2023-03-12
            </span>
            <div class="nr">
              最开始在远方是一家快递物流发货仓，当时有部分客户，经由在远方的客服协助，登录不同客户的ERP来进行发货，订单量一大，出现了库存数据混乱的情况，管理上难度很大，各家数据统计起来也很麻烦，财务结算上比较繁琐。
            </div>
           </div>
        </div>
        <div class="lfr">
          <ul>
            <li class="active">
               <div class="lf">
                <div class="date">12</div>
                <div class="year">2024-03</div>
               </div>
               <div class="lr">
                <div class="ttl">
                  成都在远方供应链，企微宝如何助力物流转型三方仓日发货9万单？
                </div>
                <div class="ct">
                  最开始在远方是一家快递物流发货仓，当时有部分客户，经由在远方的客服协助，登录不同客户的ERP来进行发货，订单量一大，出现了库存数据混乱的...
                </div>
               </div>
            </li>
            <li>
               <div class="lf">
                <div class="date">12</div>
                <div class="year">2024-03</div>
               </div>
               <div class="lr">
                <div class="ttl">
                  成都在远方供应链，企微宝如何助力物流转型三方仓日发货9万单？
                </div>
                <div class="ct">
                  最开始在远方是一家快递物流发货仓，当时有部分客户，经由在远方的客服协助，登录不同客户的ERP来进行发货，订单量一大，出现了库存数据混乱的...
                </div>
               </div>
            </li>
            <li>
               <div class="lf">
                <div class="date">12</div>
                <div class="year">2024-03</div>
               </div>
               <div class="lr">
                <div class="ttl">
                  成都在远方供应链，企微宝如何助力物流转型三方仓日发货9万单？
                </div>
                <div class="ct">
                  最开始在远方是一家快递物流发货仓，当时有部分客户，经由在远方的客服协助，登录不同客户的ERP来进行发货，订单量一大，出现了库存数据混乱的...
                </div>
               </div>
            </li>
            <li>
               <div class="lf">
                <div class="date">12</div>
                <div class="year">2024-03</div>
               </div>
               <div class="lr">
                <div class="ttl">
                  成都在远方供应链，企微宝如何助力物流转型三方仓日发货9万单？
                </div>
                <div class="ct">
                  最开始在远方是一家快递物流发货仓，当时有部分客户，经由在远方的客服协助，登录不同客户的ERP来进行发货，订单量一大，出现了库存数据混乱的...
                </div>
               </div>
            </li>
          </ul>
        </div>
      </div>
    </div>
    <!-- 合伙人 -->
    <div id="partner" class="partner-container">
      <div class="common-title flxc">
        成为企微宝合伙人
      </div>
      <div class="partner-main">
        <ul>
          <li class="parner-1">
            <div class="icon">
              <img src="@/assets/img/partner/partner-1.png" alt="">
            </div>
            <p class="ttl">企微招募人</p>
            <div class="ctr">
              <p>聚焦制造业人是难题</p>
              <p>招募人聚焦制造业人是难题</p>
              <p>招募人</p>
            </div>
          </li>
          <li class="parner-2">
            <div class="icon">
              <img src="@/assets/img/partner/partner-2.png" alt="">
            </div>
            <p class="ttl">企微推荐人</p>
            <div class="ctr">
              <p>聚焦制造业人是难题</p>
              <p>招募人聚焦制造业人是难题</p>
              <p>招募人</p>
            </div>
          </li>
          <li class="parner-3">
            <div class="icon">
              <img src="@/assets/img/partner/partner-3.png" alt="">
            </div>
            <p class="ttl">企微分销</p>
            <div class="ctr">
              <p>聚焦制造业人是难题</p>
              <p>招募人聚焦制造业人是难题</p>
              <p>招募人</p>
            </div>
          </li>
          <li class="parner-4">
            <div class="icon">
              <img src="@/assets/img/partner/partner-4.png" alt="">
            </div>
            <p class="ttl">区域代理</p>
            <div class="ctr">
              <p>聚焦制造业人是难题</p>
              <p>招募人聚焦制造业人是难题</p>
              <p>招募人</p>
            </div>
          </li>
          <li class="parner-5">
            <div class="icon">
              <img src="@/assets/img/partner/partner-5.png" alt="">
            </div>
            <p class="ttl">金牌合伙人</p>
            <div class="ctr">
              <p>聚焦制造业人是难题</p>
              <p>招募人聚焦制造业人是难题</p>
              <p>招募人</p>
            </div>
          </li>
        </ul>
      </div>
    </div>
  </div>
</template>
<script>
import Swiper from "swiper";
import { WOW } from 'wowjs';
import { writingStyleNavList, writeCtList, problemList, dealNavList, dealCtList, businessList, dealerNavList, erpCtList } from './config';

export default {
  name: "HomePage",
  data() {
    return {
      swiperList: [
        {
          img: require("@/assets/img/banner-1@2x.png"),
          path: "",
          title: '致力打造一款小微企业终身免费的ERP系统',
          content: '自主研发，毕生锻造',
          content2: '适合中小微企业，通俗操作、AI应用、零门槛',
        }
      ],
      writingActiveIndex: 0,
      dealActiveIndex: 0,
      supplierActiveIndex: 0,
      writeCtList,
      writingStyleNavList,
      problemList,
      dealNavList,
      dealCtList,
      businessList,
      dealerNavList,
      erpCtList
    };
  },
  mounted() {
    /* banner-swiper */
    new Swiper(".banner-swiper", {
      loop: true, // 循环模式选项
      effect: 'fade',
      //自动播放
      autoplay: {
        delay: 3000,
        stopOnLastSlide: false,
        disableOnInteraction: false
      },
      // 如果需要分页器
      pagination: false,
      // 如果需要前进后退按钮
      navigation: false,
      // 延迟加载
      lazy: {
        loadPrevNext: true
      },
      observer: true, //修改swiper自己或子元素时，自动初始化swiper
      observeParents: true //修改swiper的父元素时，自动初始化swiper
    });
    /* wowjs动画 */
    var wow = new WOW({
      boxClass: 'wow',
      animateClass: 'animated',
      offset: 0,
      mobile: true,
      live: true
    })
    wow.init();
  },
  methods: {
    setWritingActive(index) {
      this.writingActiveIndex = index;
    },
    setDealActive(index) {
      this.dealActiveIndex = index;
    },
    setSupplierActive(index) {
      this.supplierActiveIndex = index;
    }
  }
};
</script>
<style scoped>
div {
  max-width: 100%;
}
/* 整体盒子 */
#HomePage {
  width: 100%;
  overflow-x: hidden;
  background-color: #F5F7FA;
}

.flxc {
  display: flex;
  justify-content: center;
  align-items: center;
}

/* 轮播图 */
#swiper {
  height: 472px;
}
#swiper .banner-swiper {
  width: 100%;
  height: 100%;
}
.video-container {
  position: absolute; /* 使用绝对定位 */
  bottom: -80px;
  right: 0; /* 定位到右边 */
  width: 1400px;
  height: 600px;
}
video {
  width: 100%;
  height: 100%;
}
#swiper .banner-swiper .swiper-slide{
  position: relative;
  background-color: #f5f5f5;
}
#swiper .banner-swiper .swiper-slide img {
  width: 0;
  height: 0;
}
#swiper .banner-swiper .swiper-slide-title {
  position: absolute;
  top: 100px;
  left: 118px;
  width: 1200px;
  color: #fff;
  text-align: left;
  line-height: 80px;
}
#swiper .banner-swiper .swiper-slide-title > .tt1 {
  font-family: DingTalk JinBuTi, PingFang SC;
  font-size: 36px;
  font-weight: normal;
  line-height: normal;
  letter-spacing: 0em;
  color: #232323;
}
#swiper .banner-swiper .swiper-slide-title > .tt2 {
  font-family: PingFang SC;
  font-size: 16px;
  font-weight: normal;
  line-height: normal;
  letter-spacing: 0em;
  color: #585858;
  margin-top: 14px;
  margin-left: 194px;
}
#swiper .banner-swiper .swiper-slide-title > .tt3 {
  font-family: PingFang SC;
  font-size: 16px;
  font-weight: normal;
  line-height: normal;
  letter-spacing: 0em;
  color: #585858;
  margin-top: 14px;
  margin-left: 226px;
}
#swiper .banner-swiper .swiper-slide-title > .btn {
  margin-top: 16px;
  margin-left: 372px;
  display: flex;
}
#swiper .banner-swiper .swiper-slide-title > .btn .btn-b1 {
  width: 80px;
  height: 36px;
  border-radius: 4px;
  opacity: 1;

  /* 自动布局 */
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;

  /* 主题色/蓝色 */
  background: #3975FB;
  color: #fff;
  font-size: 14px;
}
#swiper .banner-swiper .swiper-slide-title > .btn .btn-b2 {
  width: 80px;
  height: 36px;
  border-radius: 4px;
  opacity: 1;

  /* 自动布局 */
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  padding: 10px 24px;

  box-sizing: border-box;
  /* 主题色/蓝色 */
  border: 1px solid #3975FB;
  color: #3975FB;
  font-size: 14px;
  margin-left: 16px;
}
/* banner-nav */
.banner-nav {
  margin-top: -62px;
  display: flex;
  align-items: center;
  justify-content: center;
}
.banner-nav ul {
  width: 1104px;
  height: 124px;
  border-radius: 8px;
  opacity: 1;

  /* 自动布局 */
  display: flex;
  flex-direction: row;
  align-items: center;

  background: #FFFFFF;

  box-shadow: 0px 4px 10px 0px rgba(0, 0, 0, 0.3);

  z-index: 3;
  list-style: none;
  padding: 0;
}
.banner-nav ul li {
  display: flex;
  position: relative;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  width: 220px;
  height: 124px;
}
.banner-nav li:not(:last-child)::after {
  content: ""; /* 伪元素需要 content 属性 */
  position: absolute;
  right: 0; /* 竖线放在元素的最右侧 */
  top: 50%; /* 垂直居中 */
  transform: translateY(-50%); /* 精确居中调整 */
  width: 1px;
  height: 40px;
  background-color: #EEEEEE;
}
.banner-nav ul li img {
  width: 60px;
  height: 60px;
}
.banner-nav ul li span {
  font-family: PingFang SC;
  font-size: 14px;
  padding-top: 3px;
  /* 文字色/232323 */
  color: #232323;
}
/* 大数据管理系统 */
#writingStyle {
  transition: all ease 0.6s;
  box-sizing: border-box;
  display: flex;
  justify-content: center;
  flex-direction: column;
  align-items: center;
  padding-top: 68px;
}
.common-title {
  font-family: PingFang SC;
  font-size: 28px;
  font-weight: 600;
  line-height: normal;
  letter-spacing: 0em;

  /* 文字色/232323 */
  color: #232323;
}
.common-title-tips {
  padding: 16px 0 0;
  font-family: PingFang SC;
  font-size: 14px;
  font-weight: 600;
  line-height: normal;
  letter-spacing: 0em;

  color: #999999;
}
.writingStyle-main {
  margin: 48.5px auto 0;
  display: flex;
  flex-direction: column;
}
.writingStyle-main .nav-wrapper {
  width: 800px;
  height: 130px;
}

.writingStyle-main .nav-wrapper-item {
  width: 266.67px;
  height: 130px;
  /* 自动布局 */
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  padding: 0px;
  gap: 4px;
  flex-grow: 1;
  align-self: stretch;
  position: relative;
}
.writingStyle-main .nav-wrapper-item.active {}
.writingStyle-main .nav-wrapper-item img {
  width: 80px;
  height: 80px;
  opacity: 1;
}
.writingStyle-main .nav-wrapper-item p {
  font-family: PingFang SC;
  font-size: 18px;
  font-weight: normal;
  line-height: normal;
  letter-spacing: 0em;

  /* 文字色/232323 */
  color: #232323;
}
.writingStyle-main .nav-wrapper-item.active  p {
  color: #3975FB;
}
.nav-wrapper-item.active .line {
  position: absolute;
  bottom: 0;
  left: 50%;
  margin-left: -50px;
  width: 100px;
  height: 2px;
  opacity: 1;

  /* 主题色/蓝色 */
  background: #3975FB;
}

.writingStyle-main-content {
  width: 1440px;
  display: flex;
  flex-direction: row;
  align-items: center;
  padding: 0px 120px;
}
.writingStyle-main-content-fll {
  /* 自动布局 */
  display: flex;
  flex-direction: column;
  justify-content: center;
  padding: 40px 0px;
  align-self: stretch;
  width: 50%;
  align-self: flex-end;
}
.writingStyle-main-content-fll .ttl {
  font-family: PingFang SC;
  font-size: 24px;
  font-weight: 600;

  /* 文字色/232323 */
  color: #232323;
}
.writingStyle-main-content-fll .ct-list {
  padding-top: 8px;
}
.writingStyle-main-content-fll .ct-list ul {
  display: flex;
  flex-wrap: wrap;
  width: 100%;
}
.writingStyle-main-content-fll .ct-list ul li {
  width: 50%;
  height: 50px;
  display: flex;
  align-items: center;
}
.writingStyle-main-content-fll .ct-list ul .vector {
  padding-right: 5px;
}
.writingStyle-main-content-fll .ct-list ul .vector img {
  width: 12px;
  height: 8.67px;
  display: inline-block;
}
.writingStyle-main-content-fll .ct-list ul li span {
  font-family: PingFang SC;
  font-size: 14px;
  font-weight: normal;
  line-height: normal;
  letter-spacing: 0em;

  color: #4B5C76;
}

.writingStyle-main-content-flr {
  width: 50%;
}
.writingStyle-main-content-flr img {
  width: 945.02px;
  height: 410px;
}

/* 问题 */
.problem-container {
  padding-top: 70px;
  opacity: 1;
  display: flex;
  flex-direction: column;
  align-items: center;

  background: linear-gradient(0deg, rgba(255, 255, 255, 0.6), rgba(255, 255, 255, 0.6)), url(../assets/img/image@3x.png);
  background-size: 100% 100%;
}
.problem-main {
  margin: 48.5px 0;
  display: flex;
  justify-content: center;
  align-items: center;
  width: 100%;
}
.problem-main ul {
  /* 自动布局 */
  display: flex;
  justify-content: center;
  flex-wrap: wrap;
  padding: 0px;
  gap: 20px;
  width: 1200px;
}
.problem-main li {
  width: 283px;
  margin-bottom: 20px;
  border-radius: 4px;
  opacity: 1;

  /* 自动布局 */
  display: flex;
  flex-direction: column;
  padding: 10px 0px;
  flex-grow: 1;
  align-self: stretch;

  background: #FDFDFD;
}
.problem-main .top {
  display: flex;
  justify-content: space-between;
  padding: 21px 24px 0 24px;
}
.problem-main .ttl {
  display: flex;
  justify-content: flex-start;
  flex-direction: column;
}
.problem-main .ttl p {
  font-family: PingFang SC;
  font-size: 18px;
  font-weight: 600;
  line-height: normal;
  letter-spacing: 0em;

  /* 文字色/232323 */
  color: #232323;
}
.problem-main .ttr {
  display: flex;
}
.problem-main .ttr img {
  width: 60px;
  height: 60px;
}
.problem-main .bottom {
  font-family: PingFang SC;
  font-size: 14px;

  color: #999999;
  padding: 14px 24px 0 24px;
}

/* 处理 */
.deal-main {
  margin: 10px auto 0;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}
.deal-main .nav-wrapper {
  width: 1200px;
}

.deal-main .nav-wrapper-item {
  width: 120px;
  height: 130px;
  /* 自动布局 */
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  padding: 0px;
  gap: 8px;
  flex-grow: 1;
  align-self: stretch;
  position: relative;
}
.deal-main .nav-wrapper-item.active {
}
.deal-main .nav-wrapper-item img {
  width: 60px;
  height: 60px;
  opacity: 1;
}
.deal-main .nav-wrapper-item span {
  font-family: PingFang SC;
  font-size: 18px;
  font-weight: 500;
  line-height: normal;
  letter-spacing: 0em;
}
.deal-main .nav-wrapper-item.active span {
  color: #3975FB;
}
.deal-main .nav-wrapper-item.active .line {
  position: absolute;
  bottom: 0;
  left: 50%;
  margin-left: -60px;
  width: 120px;
  height: 2px;
  opacity: 1;

  /* 主题色/蓝色 */
  background: #3975FB;
}
.deal-main-content {
  width: 1440px;
  height: 400px;
  position: relative;
  display: flex;
  align-items: flex-end;
}
.deal-main-content-fll {
  position: absolute;
  left: 180px;
  top: 83px;
  display: flex;
  flex-direction: column;
  width: 50%;
}
.deal-main-content-fll .ttl {
  font-family: PingFang SC;
  font-size: 24px;
  font-weight: 600;

  /* 文字色/232323 */
  color: #232323;
}
.deal-main-content-fll .ct-list {
  padding-top: 8px;
}
.deal-main-content-fll .ct-list ul {
  display: flex;
  flex-direction: column;
  width: 100%;
}
.deal-main-content-fll .ct-list ul li {
  width: 100%;
  height: 50px;
  display: flex;
  align-items: center;
}
.deal-main-content-fll .ct-list ul .vector {
  padding-right: 5px;
}
.deal-main-content-fll .ct-list ul .vector img {
  width: 12px;
  height: 8.67px;
  display: inline-block;
}
.deal-main-content-fll .ct-list ul li span {
  font-family: PingFang SC;
  font-size: 14px;
  font-weight: normal;
  line-height: normal;
  letter-spacing: 0em;

  color: #4B5C76;
}
.deal-main-content-flr {
  position: absolute;
  right: 0;
  top: 0;
  opacity: 1;
}
.deal-main-content-flr img {
  width: 945.02px;
  height: 410px;
}

#math {

}
.math-container {
  padding: 33px 0 0;
  background: #E4E9F0;
}
.math-content {
  width: 1440px;
  height: 645px;
  margin: 0 auto;
  background: url("../assets/img/math_bg.png") no-repeat #E4E9F0;
  background-size: 100% 100%;
}
.dyh-main {
  background: linear-gradient(0deg, rgba(255, 255, 255, 0.6), rgba(255, 255, 255, 0.6)), url(../assets/img/image@3x.png);
}
.business-container {
  padding-top: 40px;
  opacity: 1;

  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}
.business-content {
  margin-top: 40px;
  margin-bottom: 70px;
  width: 1200px;
  display: flex;
  flex-direction: column;
  justify-content: center;
  padding: 0px;
  gap: 20px;
}
.business-content ul {
  display: flex;
  flex-direction: row;
  align-items: center;
  padding: 0px;
  gap: 20px;
}
.business-content ul li {
  width: 285px;
  height: 76px;
  /* 自动布局 */
  display: flex;
  flex-direction: row;
  align-items: center;
  padding: 0px 24px;
  gap: 4px;
  flex-grow: 1;
  align-self: stretch;

  background: #FFFFFF;
}
.business-content ul li img {
  width: 60px;
  height: 60px;
}
.business-content ul li span {
  font-family: PingFang SC;
  font-size: 18px;
  font-weight: 600;
  line-height: normal;
  letter-spacing: 0em;

  /* 文字色/232323 */
  color: #232323;
}

/* 快消 */
.food-container {
  padding: 33px 0 0;
}
.food-content {
  width: 1440px;
  height: 599px;
  margin: 0 auto;
  background: url("../assets/img/39@2x.png") no-repeat;
  background-size: 100% 100%;
}

.start-container {
  margin-top: 40.5px;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}
.start-content {
  width: 1240px;
  padding-top: 20.5px;
}
.start-content ul {
  display: flex;
  flex-direction: row;
  justify-content: center;
  align-items: center;
  padding: 20px;
  gap: 24px;
}
.start-content li {
   width: 384px;
  height: 350px;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;

  background: url("../assets/img/image@2x.png") no-repeat;
  background-size: 100% 100%;

  box-shadow: 0px 2px 14px 0px rgba(0, 0, 0, 0.1);
  flex-direction: column;
}
.start-content .title {
  font-family: PingFang SC;
  font-size: 20px;
  font-weight: 600;
  line-height: normal;
  letter-spacing: 0em;

  /* 文字色/232323 */
  color: #232323;
  padding-bottom: 26px;
}
.start-content .nr {

}
.start-content dt {
  font-family: PingFang SC;
  font-size: 14px;
  font-weight: normal;
  line-height: normal;
  letter-spacing: 0em;

  color: #4B5C76;
  padding: 5px 0;
}
.start-content .btn {
  width: 160px;
  height: 40px;
  opacity: 1;

  /* 自动布局 */
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  padding: 10px 24px;

  /* 主题色/蓝色 */
  background: #3975FB;

  font-family: PingFang SC;
  font-size: 16px;
  font-weight: normal;
  line-height: normal;
  letter-spacing: 0em;

  /* 文字色/#FFFFFF */
  color: #FFFFFF;
}

/* 上市 */
.shangshi-container {
  margin-top: 60px;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  padding-bottom: 30px;
}
.shangshi-content {
  width: 1240px;
  padding-top: 60px;
  display: flex;
  flex-direction: row;
  justify-content: center;
  align-items: center;
  padding: 40px 0 0;
  gap: 24px;
}
.shangshi-content .lfr {
  width: 384px;
  height: 350px;
  opacity: 1;

  display: flex;
  flex-direction: column;
  justify-content: flex-start;
  align-items: flex-start;
  padding: 12px 32px;

  box-shadow: 0px 2px 14px 0px rgba(0, 0, 0, 0.1);
  background: url("../assets/img/ig_bg.png") no-repeat;
  background-size: 100% 100%;
}
.shangshi-content .lfr .ttl {
  font-family: PingFang SC;
  font-size: 24px;
  font-weight: 600;

  /* 文字色/232323 */
  color: #232323;
}
.shangshi-content .lfr .desc {
  font-family: PingFang SC;
  font-size: 14px;
  font-weight: normal;
  line-height: normal;
  letter-spacing: 0em;
  padding-top: 8px;

  color: #4B5C76;
}
.shangshi-content .lfr .ct-list {
  padding-top: 8px;
}
.shangshi-content .lfr .ct-list ul {
  display: flex;
  flex-direction: column;
  width: 100%;
}
.shangshi-content .lfr .ct-list ul li {
  width: 100%;
  height: 50px;
  display: flex;
  align-items: center;
}
.shangshi-content .lfr .ct-list ul .vector {
  padding-right: 5px;
}
.shangshi-content .lfr .ct-list ul .vector img {
  width: 12px;
  height: 8.67px;
  display: inline-block;
}
.shangshi-content .lfr .ct-list ul li span {
  font-family: PingFang SC;
  font-size: 14px;
  font-weight: normal;
  line-height: normal;
  letter-spacing: 0em;

  color: #4B5C76;
}
.shangshi-content .lfr .btn-b {
  width: 120px;
  height: 32px;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  margin-top: 32px;

  /* 主题色/蓝色 */
  background: #3975FB;
  font-family: PingFang SC;
  font-size: 14px;
  font-weight: normal;
  line-height: normal;
  letter-spacing: 0em;

  /* 文字色/#FFFFFF */
  color: #FFFFFF;
}
.shangshi-content .lfc {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  padding: 0px;
  gap: 20px;
  align-self: stretch;
}
.shangshi-content .item {
  width: 384px;
  height: 165px;
  padding: 24px 32px;
  background-image: url("../assets/img/image@2x-1.png");
  background-size: cover;
  background-position: center;
  display: flex;
  flex-direction: column;
}
.shangshi-content .item .erp {
  font-family: PingFang SC;
  font-size: 20px;
  font-weight: 600;
  line-height: normal;
  letter-spacing: 0em;

  /* 文字色/232323 */
  color: #232323;
}
.shangshi-content .item .desc {
  font-family: PingFang SC;
  font-size: 14px;
  font-weight: normal;
  line-height: normal;
  letter-spacing: 0em;

  color: #4B5C76;
  padding-top: 10px;
}
.shangshi-content .item a {
  font-family: PingFang SC;
  font-size: 14px;
  font-weight: normal;
  line-height: normal;
  letter-spacing: 0em;

  /* 主题色/蓝色 */
  color: #3975FB;
  padding-top: 30px;
}
/* 经销商 */
.dealer-container {
  padding-top: 60px;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  background-color: #fff;
}
.dealer-content {
  width: 1240px;
  padding-top: 40px;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}
.nava1 {
  display: flex;
  flex-direction: row;
  justify-content: center;
  align-items: center;
  padding: 0px;
  gap: 4px;
  margin-bottom: 24px;
}
.nava1 li {
  width: 200px;
  height: 86px;
  border-radius: 7px;
  opacity: 1;
  box-sizing: border-box;
  display: flex;
  justify-content: center;
  align-items: center;
  background: url("../assets/img/jingx_bg.png") no-repeat;
  background-size: 100% 100%;
}
.nava1 li img {
  /* width: 80%;
  height: 80%; */
}

/* 资讯 */
#info {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  background-color: #F5F7FA;
  padding-bottom: 20px;
}
.info-main {
  width: 1200px;
  margin-top: 60px;
  display: flex;
}
.info-main .lfl {
  align-self: stretch;
}
.info-main .lfl .info-img {
  width: 520px;
  height: 320px;
}
.info-main .lfl .info-img img {
  width: 100%;
  height: 100%;
}
.info-main .lfl .lfr-ct {
  padding-top: 24px;
}
.info-main .lfl .ttl {
  font-family: PingFang SC;
  font-size: 16px;
  font-weight: 500;
  line-height: normal;
  letter-spacing: 0em;
  /* 文字色/232323 */
  color: #232323;
  padding-bottom: 8px;
}
.info-main .lfl .info-main .lfr span {
  font-family: PingFang SC;
  font-size: 14px;
  font-weight: normal;
  line-height: normal;
  letter-spacing: 0em;
  color: #666666;
}
.info-main .lfl .nr {
  font-family: PingFang SC;
  font-size: 14px;
  font-weight: normal;
  line-height: normal;
  letter-spacing: 0em;

  font-variation-settings: "opsz" auto;
  color: #666666;
  padding-top: 20px;
}

.info-main .lfr {
  display: flex;
  flex-direction: column;
  padding: 0px;
  flex-grow: 1;
}
.info-main .lfr li {
  width: 640px;
  height: 126px;
  display: flex;
  flex-direction: row;
  align-items: center;
  padding: 24px 16px;
  gap: 24px;
  align-self: stretch;
}
.info-main .lfr li.active {
  background: #FFFFFF;
}
.info-main .lfr .lf {
  width: 81px;
  height: 78px;
  display: flex;
  flex-direction: column;
  align-items: flex-end;
  padding: 10px 11px 10px 0;
  gap: 4px;

  box-sizing: border-box;
  border-width: 0px 1px 0px 0px;
  border-style: solid;
  border-color: #DADADA;
}
.info-main .lfr .lf .date {
  font-family: PingFang SC;
  font-size: 24px;
  font-weight: 500;
  line-height: normal;
  letter-spacing: 0em;

  font-variation-settings: "opsz" auto;
  /* 文字色/232323 */
  color: #232323;
}
.info-main .lfr .lf .year {
  font-family: PingFang SC;
  font-size: 14px;
  font-weight: normal;
  line-height: normal;
  letter-spacing: 0em;

  font-variation-settings: "opsz" auto;
  /* 文字色/232323 */
  color: #232323;
  width: 59px;
}
.info-main .lfr .lr {
  display: flex;
  flex-direction: column;
  padding: 0px;
  gap: 16px;
  flex-grow: 1;
}
.info-main .lfr .lr .ttl {
  font-family: PingFang SC;
  font-size: 16px;
  font-weight: 500;
  line-height: normal;
  letter-spacing: 0em;

  font-variation-settings: "opsz" auto;
  /* 文字色/232323 */
  color: #232323;
}
.info-main .lfr .lr .ct {
  font-family: PingFang SC;
  font-size: 14px;
  font-weight: normal;
  line-height: normal;
  letter-spacing: 0em;

  font-variation-settings: "opsz" auto;
  color: #666666;
  padding-top: 16px;
}

/* 合伙人 */
#partner {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  background-image: url("../assets/img/hehuoren_bg.png");
  background-size: cover;
  background-position: center;
}
.partner-container {
  padding-top: 30px;
}
.partner-main {
  width: 1240px;
  margin-top: 30px;
  display: flex;
}
.partner-main ul {
  width: 1240px;
  height: 270px;
  opacity: 1;

  /* 自动布局 */
  display: flex;
  flex-direction: row;
  justify-content: center;
  align-items: center;
  padding: 10px 20px;
  gap: 20px;
}
.partner-main ul li {
  width: 224px;
  height: 250px;
  /* 自动布局 */
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;

  border-radius: 12px;

  background: linear-gradient(222deg, #DEEEFF -2%, #F1F8FE 99%, #F1F8FE 99%);

  box-sizing: border-box;

  box-shadow: 0px 4px 10px 0px rgba(0, 0, 0, 0.08);

  z-index: 1;
}
.partner-main .parner-1 img {
  width: 68px;
  height: 61px;
}
.partner-main .parner-2 img {
  width: 68px;
  height: 71px;
}
.partner-main .parner-3 img {
  width: 63px;
  height: 60px;
}
.partner-main .parner-4 img {
  width: 60px;
  height: 56px;
}
.partner-main .parner-5 img {
  width: 61px;
  height: 60px;
}
.partner-main .ttl {
  font-family: PingFang SC;
  font-size: 20px;
  font-weight: 600;
  line-height: normal;
  letter-spacing: 0em;

  /* 文字色/232323 */
  color: #232323;
  padding-top: 20px;
}
.partner-main .ctr {
  display: flex;
  flex-direction: column;
  align-items: center;
  align-self: stretch;
  padding-top: 10px;
}
.partner-main p {
  font-family: PingFang SC;
  font-size: 14px;
  font-weight: normal;
  line-height: normal;
  text-align: center;
  letter-spacing: 0em;
  margin-bottom: 2px;

  color: #4B5C76;
}
</style>
