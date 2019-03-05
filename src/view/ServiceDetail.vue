<template>
  <div id="ServiceDetail">
    <div class="banner container-fuild text-center">相关服务</div>
    <div class="container">
      <div class="row">
        <div class="col-xs-12 col-sm-12 col-md-3" id="myScrollspy">
          <ul class="nav nav-tabs nav-stacked center-block" id="myNav">
            <p>特色服务</p>
            <li
              :class="item.id==id?'active':''"
              v-for="(item,index) in serviceNavList"
              :key="index"
            >
              <a :href="'#'+item.id">{{item.title}}</a>
            </li>
          </ul>
        </div>
        <div class="col-xs-12 col-sm-12 col-md-9 content  wow zoomIn">
          <div class="content-block" v-for="(item,index) in serviceContentList" :key="index">
            <h2 :id="item.id">
              {{item.title}}
              <small>/ {{item.eng_title}}</small>
            </h2>
            <div v-html="item.content"></div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
import { WOW } from "wowjs";
export default {
  name: "ServiceDetail",
  data() {
    return {
      id: "section-1",
      serviceNavList: [
        {
          id: "section-1",
          title: "软件定制开发"
        },
        {
          id: "section-2",
          title: "IT外包服务"
        },
        {
          id: "section-3",
          title: "网上商城建设"
        },
        {
          id: "section-4",
          title: "iOS应用定制开发"
        }
      ],
      serviceContentList: [
        {
          id: "section-1",
          title: "软件定制开发",
          eng_title: "Customize App",
          content:
            "<h3>这是标题1</h3><p>这里是内容，请根据实际需要修改。这里是内容，请根据实际需要修改。这里是内容，请根据实际需要修改。这里是内容，请根据实际需要修改。这里是内容，请根据实际需要修改。这里是内容，请根据实际需要修改。这里是内容，请根据实际需要修改。这里是内容，请根据实际需要修改。这里是内容，请根据实际需要修改。这里是内容，请根据实际需要修改。</p><h3>这是标题2</h3><p>这里是内容，请根据实际需要修改。这里是内容，请根据实际需要修改。这里是内容，请根据实际需要修改。这里是内容，请根据实际需要修改。这里是内容，请根据实际需要修改。这里是内容，请根据实际需要修改。这里是内容，请根据实际需要修改。这里是内容，请根据实际需要修改。这里是内容，请根据实际需要修改。这里是内容，请根据实际需要修改。</p>"
        },
        {
          id: "section-2",
          title: "IT外包服务",
          eng_title: "Outsourcing",
          content:
            "<h3>这是标题1</h3><p>这里是内容，请根据实际需要修改。这里是内容，请根据实际需要修改。这里是内容，请根据实际需要修改。这里是内容，请根据实际需要修改。这里是内容，请根据实际需要修改。这里是内容，请根据实际需要修改。这里是内容，请根据实际需要修改。这里是内容，请根据实际需要修改。这里是内容，请根据实际需要修改。这里是内容，请根据实际需要修改。</p><h3>这是标题2</h3><p>这里是内容，请根据实际需要修改。这里是内容，请根据实际需要修改。这里是内容，请根据实际需要修改。这里是内容，请根据实际需要修改。这里是内容，请根据实际需要修改。这里是内容，请根据实际需要修改。这里是内容，请根据实际需要修改。这里是内容，请根据实际需要修改。这里是内容，请根据实际需要修改。这里是内容，请根据实际需要修改。</p>"
        },
        {
          id: "section-3",
          title: "网上商城建设",
          eng_title: "eCommerce Site",
          content:
            "<h3>这是标题1</h3><p>这里是内容，请根据实际需要修改。这里是内容，请根据实际需要修改。这里是内容，请根据实际需要修改。这里是内容，请根据实际需要修改。这里是内容，请根据实际需要修改。这里是内容，请根据实际需要修改。这里是内容，请根据实际需要修改。这里是内容，请根据实际需要修改。这里是内容，请根据实际需要修改。这里是内容，请根据实际需要修改。</p><h3>这是标题2</h3><p>这里是内容，请根据实际需要修改。这里是内容，请根据实际需要修改。这里是内容，请根据实际需要修改。这里是内容，请根据实际需要修改。这里是内容，请根据实际需要修改。这里是内容，请根据实际需要修改。这里是内容，请根据实际需要修改。这里是内容，请根据实际需要修改。这里是内容，请根据实际需要修改。这里是内容，请根据实际需要修改。</p>"
        },
        {
          id: "section-4",
          title: "iOS应用定制开发",
          eng_title: "iOS App Dev",
          content:
            "<h3>这是标题1</h3><p>这里是内容，请根据实际需要修改。这里是内容，请根据实际需要修改。这里是内容，请根据实际需要修改。这里是内容，请根据实际需要修改。这里是内容，请根据实际需要修改。这里是内容，请根据实际需要修改。这里是内容，请根据实际需要修改。这里是内容，请根据实际需要修改。这里是内容，请根据实际需要修改。这里是内容，请根据实际需要修改。</p><h3>这是标题2</h3><p>这里是内容，请根据实际需要修改。这里是内容，请根据实际需要修改。这里是内容，请根据实际需要修改。这里是内容，请根据实际需要修改。这里是内容，请根据实际需要修改。这里是内容，请根据实际需要修改。这里是内容，请根据实际需要修改。这里是内容，请根据实际需要修改。这里是内容，请根据实际需要修改。这里是内容，请根据实际需要修改。</p>"
        }
      ]
    };
  },
  mounted() {
    this.id = this.$route.params.id;
    var top = document.getElementById(this.id).offsetTop;
    $(window).scrollTop(top + 300);
    $("#myNav").affix({
      offset: {
        top: 300
      }
    });
    var wow = new WOW();
    wow.init();
  }
};
</script>
<style scoped>
.banner {
  color: #fff;
  font-size: 30px;
  height: 150px;
  line-height: 150px;
  background-image: url("../assets/img/banner_2.jpg");
  background-repeat: no-repeat;
  background-size: cover;
  background-attachment: scroll;
  background-position: center center;
}
ul.nav-tabs {
  width: 200px;
  margin-top: 40px;
  border-radius: 4px;
  background: #fff;
  z-index: 99999;
  border: 1px solid #474747;
  box-shadow: 0 1px 4px rgba(0, 0, 0, 0.067);
}
ul.nav-tabs li {
  text-align: center;
  margin: 0;
  border-top: 1px solid #474747;
}
ul.nav-tabs p {
  color: #fff;
  font-size: 18px;
  font-weight: bold;
  text-align: center;
  background: #474747;
  margin: 0;
  padding: 10px 0;
}
ul.nav-tabs li:first-child {
  border-top: none;
}
ul.nav-tabs li a {
  margin: 0;
  padding: 8px 16px;
  border-radius: 0;
}
ul.nav-tabs li.active a,
ul.nav-tabs li.active a:hover {
  color: #fff;
  background: #474747;
  border: 1px solid #474747;
}
ul.nav-tabs li:first-child a {
  border-radius: 4px 4px 0 0;
}
ul.nav-tabs li:last-child a {
  border-radius: 0 0 4px 4px;
}
ul.nav-tabs.affix {
  top: 30px;
}
.content-block {
  margin: 50px 0;
}
.content-block > h2 {
  padding: 20px 0;
  border-bottom: 1px solid #ccc;
}
</style>
