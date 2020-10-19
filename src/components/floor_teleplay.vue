<template>
    <div class="floor">
        <el-row type="flex" justify="space-between" class="floor_hd">
            <el-col :span="14"><h4><a href="" name="teleplay">电视剧</a></h4></el-col>
            <el-col :span="10"><span><a href="">更多+</a></span></el-col>
        </el-row>
        <el-row class="floor_bd">
            <el-col :md="4" :sm="8" :xs="12" v-for="item in teleplayList" :key="item.id">
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
           teleplayList:[
                {
                    "type": "teleplay",
                    "id": 1,
                    "name": "孤单又灿烂的神：鬼怪",
                    "post_url": require("../../upload/index_teleplay/teleplay01.webp")
                },
                {
                    "type": "teleplay",
                    "id": 2,
                    "name": "请回答1988",
                    "post_url": require("../../upload/index_teleplay/teleplay02.webp")
                },
                {
                    "type": "teleplay",
                    "id": 3,
                    "name": "父母爱情",
                    "post_url": require("../../upload/index_teleplay/teleplay03.webp")
                },
                {
                    "type": "teleplay",
                    "id": 4,
                    "name": "异乡人Doctor",
                    "post_url": require("../../upload/index_teleplay/teleplay04.webp")
                },
                {
                    "type": "teleplay",
                    "id": 5,
                    "name": "当你沉睡时",
                    "post_url": require("../../upload/index_teleplay/teleplay05.webp")
                },
                {
                    "type": "teleplay",
                    "id": 6,
                    "name": "金秘书为何那样",
                    "post_url": require("../../upload/index_teleplay/teleplay06.webp")
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