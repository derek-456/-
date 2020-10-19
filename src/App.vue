<template>
  <div id="app">
    <!-- shortcut -->
    <el-row type="flex" justify="center" class="header">
      <el-col :span="15" class="header">
        <el-row class="shortcut">
          <el-col :md="7" :sm="24"><div class="fl">闲暇时光网欢迎您!</div></el-col>
          <el-col :md="1" class="hidden-sm-and-down"></el-col>
          <el-col :md="16" :sm="24"><div class="fr">推我所爱，与您共度美好的闲暇时光。</div></el-col>
        </el-row>
      </el-col>
    </el-row>
    <!-- nav -->
    <el-row  type="flex" justify="center">
      <el-col :lg="15" :md="24">
        <el-row  class="nav">
          <el-col :md="7" :sm="20" :xs="20">
            <div class="logo">
              <h1>
                <a href="">闲暇时光网</a>
              </h1>
            </div>
          </el-col>
          <el-col :md="2" :sm="4" :xs="4"><img class="hidden-md-and-up" src="../public/manu.png" alt=""></el-col>
          <el-col :md="14" class="hidden-sm-and-down">
            <el-row type="flex" justify="space-between">
              <el-col class="menuItem">电影</el-col>
              <el-col class="menuItem">动漫</el-col>
              <el-col class="menuItem">电视剧</el-col>
              <el-col class="menuItem">读书</el-col>
            </el-row>
          </el-col>
          <!-- <el-col :md="1" :sm="1" class="hidden-sm-and-up"><img src="../public/manu.png" alt=""></el-col> -->
        </el-row>
      </el-col>
    </el-row>
    <!-- banner -->
    <el-row  type="flex" justify="center" class="banner">
      <el-col :lg="15" :md="24">
        <banner></banner>
      </el-col>
    </el-row>

    <!-- floor -->
    <el-row  type="flex" justify="center">
      <el-col :lg="15" :md="24">
        <floorMovie></floorMovie>
      </el-col>
    </el-row>
    <el-row  type="flex" justify="center">
      <el-col :lg="15" :md="24">
        <floorAnimation></floorAnimation>
      </el-col>
    </el-row>
    <el-row  type="flex" justify="center">
      <el-col :lg="15" :md="24">
        <floorTeleplay></floorTeleplay>
      </el-col>
    </el-row>
    <el-row  type="flex" justify="center">
      <el-col :lg="15" :md="24">
        <floorBook></floorBook>
      </el-col>
    </el-row>


    <!-- footer -->
    <el-row type="flex" justify="center">
      <el-col :span="15" style="text-align:center">
        <hr>
      </el-col>
    </el-row>
    <el-row type="flex" justify="center">
      <el-col :span="15" style="text-align:center">
        网站所有资源排名仅代表本人个人意见，萝卜青菜各有所爱！
      </el-col>
    </el-row>
    <el-row type="flex" justify="center">
      <el-col :span="15" style="text-align:center">
        网站所有图片资源部分来自个人截图，大部分收集于 豆瓣 若本站收录的节目无意侵犯了贵司版权，请给网页底部邮箱地址来信，我们会及时处理和回复，谢谢
      </el-col>
    </el-row>
    <el-row type="flex" justify="center">
      <el-col :span="15" style="text-align:center">
        Copyright©2020 闲暇时光
      </el-col>
    </el-row>
    

  </div>
</template>

<script>
import 'element-ui/lib/theme-chalk/display.css';
import banner from './components/banner.vue'
import floorMovie from './components/floor_movies.vue'
import floorAnimation from './components/floor_animation.vue'
import floorTeleplay from './components/floor_teleplay.vue'
import floorBook from './components/floor_book.vue'
export default {
  name: 'app',
  data(){
    return{
    }
  },
  components: {
    "banner": banner,
    "floorMovie": floorMovie,
    "floorAnimation":floorAnimation,
    "floorTeleplay":floorTeleplay,
    "floorBook":floorBook
  }
}
</script>

<style>
*{
  padding: 0;
  margin: 0;
  box-sizing: border-box;
}

#app .header{
  background-color: rgb(227,228,229);
}

/* shortcut */
.shortcut{
  height:35px;
}
.shortcut>div{
  height: 100%;
}
.shortcut .fl,.fr{
  height: 100%;
  line-height: 35px;
  text-align: center;
  color: #999;
}
.shortcut .fl{
  font-size: 18px;
  letter-spacing: 2px;
}
.shortcut .fr{
  font-size: 23px;
  font-style: italic;
  font-weight: 500;
}

/* nav */
.nav{
  height: 80px;
  line-height: 80px;
  background-color:rgb(41,54,122);
  margin-bottom: 20px;
}
.nav>div{
  height: 100%;
}
.nav .logo{
  text-align: center;
  text-indent: -999px;
  overflow: hidden;
  background: url(../public/vacantTimeLogo.png) no-repeat center center ;
  background-size: 70% 70%;
}
.nav .menuItem{
  font-size: 27px;
  font-weight: 600;
  text-align: center;
  cursor: pointer;
}
.nav .el-col-md-2{
  text-align: center;
}
.nav .el-col-md-2 img{
  width: 50px;
  height: 50px;
  vertical-align: middle;
  text-align: center;
}

/* banner */
.banner{
  margin-bottom: 150px;
}

/* floor */
.floor{
  padding-bottom: 50px;
}



</style>
