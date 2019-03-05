<template>
    <div id="CompanyIntroduction">
        <div class="banner container-fuild text-center">关于我们</div>
        <div class="container">
            <div class="row CompanyIntroduction-container">
                <div class="col-xs-12 col-sm-12 col-md-6 wow zoomIn">
                    <img class="img-responsive center-block" src="@/assets/img/about_img.png">
                </div>
                <div class="col-xs-12 col-sm-12 col-md-6">
                    <h3>网站建设文化传播有限公司</h3>
                    <p class=".text-justify">有家软件公司, 是一家以高科技创意为核心的技术服务公司, 聚集了众多对软件开发和界面设计有独特创意的高端人才, 致力于为企业提供软件开发, 网站建设, 网页设计, IT外包, 手机应用开发, 互联网营销, 微信平台开发等解决方案。</p>
                    <p class=".text-justify">我们的客户包括集团上市公司, 酒店, IT科技, 教育, 服装, 贸易, 外贸, 时尚, 生物, 工业, 制造等众多行业, 并树立了良好的口碑, 积累了丰富的经验和成功案例. 我们提供权威专业的互联网品牌策划, 并实施高标准的设计方案, 创造真正意义上的品牌网站, 为互联网品牌在互动行销领域创造最大价值而不懈努力!</p>
                </div>
            </div>
        </div>
    </div>
</template>
<script>
import { WOW } from 'wowjs';
export default {
    name: 'CompanyIntroduction',
    data(){
        return{

        }
    },
    mounted(){
        var wow = new WOW();
        wow.init();
    }
}
</script>
<style scoped>
.banner{
    color: #fff;
    font-size: 30px;
    height: 150px;
    line-height: 150px;
    background-image: url('../assets/img/banner1.png');
    background-repeat: no-repeat;
    background-size: cover;
    background-attachment: scroll;
    background-position: center center;
}
.row{
    margin-right: 0;
    margin-left: 0;
}
.CompanyIntroduction-container{
    padding: 100px 0;
    color: #808080;
    transition: all ease 0.5s;
}
.CompanyIntroduction-container>div>p{
    font-size: 14px;
    line-height: 2.5rem;
}
@media screen and (max-width: 997px){
    .CompanyIntroduction-container{
    padding: 10px 0;
    color: #808080;
}
}
</style>

