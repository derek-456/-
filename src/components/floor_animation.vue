<template>
    <div class="floor">
        <el-row type="flex" justify="space-between" class="floor_hd">
            <el-col :span="10"><h4><a href="" name="animation">动漫</a></h4></el-col>
            <el-col :span="10"><span><a href="">更多+</a></span></el-col>
        </el-row>
        <el-row class="floor_bd">
            <el-col :md="4" :sm="8" :xs="12" v-for="item in animationList" :key="item.id">
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
            animationList:[
                {
                    "type": "animation",
                    "id": 1,
                    "name": "灌篮高手",
                    "post_url": require("../../upload/index_animation/animation01.webp")
                },
                {
                    "type": "animation",
                    "id": 2,
                    "name": "小林家的龙女仆",
                    "post_url": require("../../upload/index_animation/animation02.webp")
                },
                {
                    "type": "animation",
                    "id": 3,
                    "name": "俺物语",
                    "post_url": require("../../upload/index_animation/animation03.webp")
                },
                {
                    "type": "animation",
                    "id": 4,
                    "name": "擅长捉弄人的高木同学",
                    "post_url": require("../../upload/index_animation/animation04.webp")
                },
                {
                    "type": "animation",
                    "id": 5,
                    "name": "冰菓",
                    "post_url": require("../../upload/index_animation/animation05.webp")
                },
                {
                    "type": "animation",
                    "id": 6,
                    "name": "辉夜大小姐想让我告白",
                    "post_url": require("../../upload/index_animation/animation06.webp")
                },
            ]
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
    padding:0 5px;
    text-align: center;
    font-size: 18px;
    font-weight: 600;
    margin-bottom: 20px;

    overflow: hidden;
    white-space: nowrap;
    text-overflow: ellipsis;
}

</style>