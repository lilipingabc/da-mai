<template>
    <div class="footer">
        <ul>
            <router-link :to="item.path" tag="li" v-for="(item,index) in tabbar" :key="item.id">
                <i class="iconfont" v-html="item.icon"></i>
                <span>{{item.title}}</span>
            </router-link>
        </ul>
    </div>
</template>
<script>
export default {
    name:"tabbar",
    data(){
        return{
            tabbar:[
                {
                    title:"电影",
                    path:"/movie",
                    icon:"&#xe6af;"
                },
                {
                    title:"影院",
                    path:"/cinema",
                    icon:"&#xe61d;"
                },
                {
                    title:"我的",
                    path:"/mine",
                    icon:"&#xe629;"
                }
            ]
        }
    }
}
</script>
<style lang="scss" scoped>
$sc:25;
$color:#e54847;
.footer{
  width:100%;
  height: 50/$sc+rem;
  position: fixed;
  bottom: 0;
  left:0;
  border-top:1px solid rgb(214, 214, 214);
  ul{
      width:100%;
      height:100%;
      display: flex;
      margin-top:5/$sc+rem;
    //   justify-content: space-between;
    //   align-items: center;
      li{
          width: 100%;
          height:100%;
          display: flex;
          flex-direction: column;
          text-align: center;
          font-size:12px;
          color:rgb(70, 69, 69);
          .iconfont{
              font-size: 20px;
          }
      }
  }
}
.footer>ul>.router-link-active{
    color: $color;
}
</style>