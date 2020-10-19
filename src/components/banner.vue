<template>
    <el-carousel height="600px" trigger="click">
      <el-carousel-item v-for="item in bannerList" :key="item.name">
        <h3><img :src="item.post_url" alt=""></h3>
    </el-carousel-item>
    </el-carousel>
</template>

<script>
export default {
    data(){
        return{
            bannerList:[
                {"type":"movie","id": 1,"name": "时空恋旅人","post_url": require("../../upload/index_banner/banner01.webp")},
                {"type": "animation","id": 1,"name": "擅长捉弄的高木同学","post_url": require("../../upload/index_banner/banner02.png")},
                {"type": "teleplay","id": 1,"name": "孤单又灿烂的神-鬼怪","post_url": require("../../upload/index_banner/banner03.webp")},
                {"type": "book","id": 1,"name": "围城","post_url": require("../../upload/index_banner/banner04.jpg")}
            ]
        }
    }
}
</script>

<style lang="less" scoped>
.el-carousel__item h3 {
    line-height: 300px;
    margin: 0;
}

.el-carousel__item h3 img{
    width: 100%;
    height: 600px;
}
  

</style>