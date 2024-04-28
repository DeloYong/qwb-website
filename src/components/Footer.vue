<template>
  <!-- footer -->
  <div id="footer" class="row">
    <div class="footer-container">
      <div class="footer-tips">
        <div class="item">
          <div class="icon">
            <img src="@/assets/img/footer/tips3.png" alt="">
          </div>
          <div class="txt">强大的技术支持</div>
        </div>
        <div class="item">
          <div class="icon">
            <img src="@/assets/img/footer/tips4.png" alt="">
          </div>
          <div class="txt">一对一线上培训</div>
        </div>
        <div class="item">
          <div class="icon">
            <img src="@/assets/img/footer/tips1.png" alt="">
          </div>
          <div class="txt">会员线上专线服务</div>
        </div>
        <div class="item">
          <div class="icon">
            <img src="@/assets/img/footer/tips2.png" alt="">
          </div>
          <div class="txt">全方位售后服务</div>
        </div>
      </div>
      <div class="footer-main">
        <div class="footer-content">
          <div class="footer-ct1">
            <div class="ct1-ttl">
              产品
            </div>
            <div class="ct1-nr">
              企微宝开单版
            </div>
            <div class="ct1-nr">
              企微宝开单版
            </div>
            <div class="ct1-nr">
              企微宝开单版
            </div>
            <div class="ct1-nr">
              企微宝开单版
            </div>
            <div class="ct1-nr">
              企微宝开单版
            </div>
            <div class="ct1-nr">
              企微宝开单版
            </div>
          </div>
          <div class="footer-ct1">
            <div class="ct1-ttl">
              功能模块
            </div>
            <div class="ct1-nr">
              智能ERP
            </div>
            <div class="ct1-nr">
              智能会计
            </div>
            <div class="ct1-nr">
              外勤管理
            </div>
            <div class="ct1-nr">
              商城管理
            </div>
            <div class="ct1-nr">
              物流管理
            </div>
          </div>
          <div class="footer-ct1">
            <div class="ct1-ttl">
              了解企微宝
            </div>
            <div class="ct1-nr">
              关于我们
            </div>
            <div class="ct1-nr">
              客户案例
            </div>
            <div class="ct1-nr">
              解决方案
            </div>
            <div class="ct1-nr">
              代理加盟
            </div>
          </div>
          <div class="footer-ct1">
            <div class="ct1-ttl">
              服务
            </div>
            <div class="ct1-nr">
              帮助中心
            </div>
            <div class="ct1-nr">
              下载软件
            </div>
          </div>
          <div class="footer-contact">
            <div class="ct1-ttl">
              关注或联系我们
            </div>
            <div class="ct1-nr">
              添加企微宝公众号、视频号、了解实时资讯
            </div>
            <div class="wx-tub">
              <div class="erweima">
                <img src="@/assets/img/footer/erweima.png" alt="">
              </div>
              <div class="erweima">
                <img src="@/assets/img/footer/erweima.png" alt="">
              </div>
              <div class="erweima">
                <img src="@/assets/img/footer/erweima.png" alt="">
              </div>
            </div>
            <div class="phone">
              <p><span>咨询热线：</span>400-000-000</p>
              <p><span>商务合作：</span>xucyyvol2k@aol.com</p>
              <p><span>业务合作：</span>xucyyvol2k@aol.com</p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  name: "Footer",
  data() {
    return {};
  }
};
</script>
<style scoped>
/* footer */
#footer {

  background: #F6F7FB;
}
.footer-container {
  width: 1440px;
  margin: 0 auto;
  display: flex;
  flex-direction: column;
  padding: 0px 120px;
  align-self: stretch;
}
.footer-tips {
  width: 1200px;
  height: 60px;
  opacity: 1;

  /* 自动布局 */
  display: flex;
  flex-direction: row;
  padding: 0px 20px;
  gap: 10px;
  align-self: stretch;

  box-sizing: border-box;
  border-width: 0px 0px 1px 0px;
  border-style: solid;
  border-color: #DCDCDC;
}
.footer-tips .item {
  display: flex;
  flex-direction: row;
  align-items: center;
  padding: 10px;
  gap: 8px;
  flex-grow: 1;
  align-self: stretch;
}
.footer-tips .item .icon img {
  width: 16px;
  height: 16px;
}
.footer-tips .item .txt {
  font-family: PingFang SC;
  font-size: 14px;
  font-weight: normal;
  line-height: normal;
  text-align: center;
  letter-spacing: 0em;

  color: #666666;
}
.footer-content {
  display: flex;
  flex-direction: row;
  padding: 0px;
  gap: 10px;
  flex-grow: 1;
  align-self: stretch;
}
.footer-content .footer-ct1 {
  width: 200px;
  height: 380px;
  display: flex;
  flex-direction: column;
  padding: 32px 20px;
  gap: 20px;
  align-self: stretch;
}
.footer-content .ct1-ttl {
  font-family: PingFang SC;
  font-size: 16px;
  font-weight: 500;
  line-height: normal;
  text-align: center;
  letter-spacing: 0em;

  /* 文字色/232323 */
  color: #232323;
}
.footer-content .ct1-nr {
  font-family: PingFang SC;
  font-size: 14px;
  font-weight: normal;
  line-height: normal;
  text-align: center;
  letter-spacing: 0em;

  color: #666666;
}
.footer-contact {
  width: 360px;
  height: 380px;
  display: flex;
  flex-direction: column;
  padding: 32px 0px;
  gap: 20px;
  flex-grow: 1;
  align-self: stretch;
  align-items: flex-start;
  justify-content: flex-start;
}
.footer-contact .wx-tub {
  display: flex;
  flex-direction: row;
  padding: 0px;
  gap: 15px;
  align-self: stretch;
}
.footer-contact .erweima {
  flex-grow: 1;
  align-self: stretch;
}
.footer-contact .erweima img {
  width: 110px;
  height: 110px;
}
.footer-contact .phone {
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  justify-content: flex-start;
  padding: 0px;
  gap: 10px;
}
.footer-contact .phone p {
  font-family: PingFang SC;
  font-size: 14px;
  font-weight: normal;
  line-height: normal;
  text-align: center;
  letter-spacing: 0em;
  color: #232323
}
.footer-contact .phone p span {
  color: #666666;
}
</style>

