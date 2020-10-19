<template>
    <div class="floor">
        <el-row type="flex" justify="space-between" class="floor_hd">
            <el-col :span="10"><h4><a href="" name="movie">电影</a></h4></el-col>
            <el-col :span="10"><span><a href="">更多+</a></span></el-col>
        </el-row>
        <el-row class="floor_bd">
            <el-col :md="4" :sm="8" :xs="12" v-for="item in movieList" :key="item.id">
                <img :src="item.post_url" alt="">
                <div class="title">{{item.name}}</div>
            </el-col>
        </el-row>
    </div>
</template>

<script>
export default {
    data(){
        return{
            movieList:[
        {
          "type": "movie",
          "id": 1,
          "name": "时空恋旅人",
          "post_url": require("../../upload/index_movie/movie01.webp")
        },
        {
          "type": "movie",
          "id": 2,
          "name": "当幸福来敲门",
          "post_url": require("../../upload/index_movie/movie02.webp")
        },
        {
          "type": "movie",
          "id": 3,
          "name": "肖申克的救赎",
          "post_url": require("../../upload/index_movie/movie03.webp")
        },
        {
          "type": "movie",
          "id": 4,
          "name": "触不可及",
          "post_url": require("../../upload/index_movie/movie04.webp")
        },
        {
          "type": "movie",
          "id": 5,
          "name": "阳光姐妹淘",
          "post_url": require("../../upload/index_movie/movie05.webp")
        },
        {
          "type": "movie",
          "id": 6,
          "name": "放牛班的春天",
          "post_url": require("../../upload/index_movie/movie06.webp")
        },
      ],
        }
    },
}
</script>

<style lang="less" scoped>
a{
    text-decoration: none;
    color: black;
}
.floor .floor_hd{
    margin-bottom: 10px;
    padding: 0 40px;
}
.floor h4 a{
    font-size: 30px;
    letter-spacing: 10px;
    font-weight: 600;
}
.floor span{
    display: block;
    width: 100%;
    text-align: right;

}
.floor span a{
    line-height: 39px;
}
.floor_bd {
    height: 220px;
}
.floor_bd>div{
    height: 100%;
}
.floor_bd img{
    display: block;
    width: 140px;
    margin: 0 auto;
    height: 80%;
    padding:0 10px;
}

.floor_bd .title{
    padding: 0 5px;
    text-align: center;
    font-size: 18px;
    font-weight: 600;
    margin-bottom: 20px;

    overflow: hidden;
    white-space: nowrap;
    text-overflow: ellipsis;
}

</style>