<template>
  <div id='app'>
    <components></components>
  </div>
</template>
<script>
  import components from 'components/components'

  export default {
    name: 'app',
    components: {
      components
    }
  }

</script>
<style>
  body, html {
    height: 100%;
  }

  body {
    background: rgb(255, 255, 255);
  }

  #ranking {
    background: rgb(244, 244, 244);
  }

  #recomment {
    background: rgb(244, 244, 244);
  }

  .left {
    float: left;
  }

  .right {
    float: right;
  }

  .clear:after {
    content: "";
    display: block;
    clear: both;
  }

  .mint-spinner-triple-bounce > div, .mint-spinner-double-bounce > div {
    background: #31c27c !important;
  }

  .mint-spinner-double-bounce {
    margin: 0px auto;
  }

  .loading_con {
    padding: 20px;
    text-align: center;
  }
</style>
<!-- <template>
    <div class="rules">
        <p class="drop-down" v-if="dropDown">松手刷新数据...</p>
        <div class="bscroll" ref="bscroll">
            <ul>
               <li>1</li><li>1</li><li>1</li>
               <li>1</li><li>1</li><li>1</li>
               <li>1</li><li>1</li><li>1</li>
               <li>1</li><li>1</li><li>1</li>
               <li>1</li><li>1</li><li>1</li>
               <li>1</li><li>1</li><li>1</li>
               <li>1</li><li>1</li><li>1</li>
               <li>1</li><li>1</li><li>1</li>
               <li>1</li><li>1</li><li>1</li>
               <li>1</li><li>1</li><li>1</li>
               <li>1</li><li>1</li><li>1</li>
               <li>1</li><li>1</li><li>1</li>
               <li>1</li><li>1</li><li>1</li>
               <li>1</li><li>1</li><li>1</li>
               <li>1</li><li>1</li><li>1</li>
               <li>1</li><li>1</li><li>1</li>
               <li>1</li><li>1</li><li>1</li>
               <li>1</li><li>1</li><li>1</li>
               <li>1</li><li>1</li><li>1</li>
               <li>1</li><li>1</li><li>1</li>
               <li>1</li><li>1</li><li>1</li>
               <li>1</li><li>1</li><li>1</li>
               <li>1</li><li>1</li><li>1</li>
               <li>1</li><li>1</li><li>1</li>
               <li>1</li><li>1</li><li>1</li>
               <li>1</li><li>1</li><li>1</li>
               <li>1</li><li>1</li><li>1</li>
               <li>1</li><li>1</li><li>1</li>
               <li>1</li><li>1</li><li>1</li>
               <li>1</li><li>1</li><li>1</li>
               <li>1</li><li>1</li><li>1</li>
               <li>1</li><li>1</li><li>1</li>
               <li>1</li><li>1</li><li>1</li>
               <li>1</li><li>1</li><li>1</li>
               <li>1</li><li>1</li><li>1</li>
               <li>1</li><li>1</li><li>1</li>
               <li>1</li><li>1</li><li>1</li>
               <li>1</li><li>1</li><li>1</li>
               <li>1</li><li>1</li><li>1</li>
               <li>1</li><li>1</li><li>1</li>
               <li>1</li><li>1</li><li>1</li>
               <li>1</li><li>1</li><li>1</li>
               <li>1</li><li>1</li><li>1</li>
               <li>1</li><li>1</li><li>1</li>
               <li>1</li><li>1</li><li>1</li>
               <li>1</li><li>1</li><li>1</li>
               <li>1</li><li>1</li><li>1</li>
               <li>1</li><li>1</li><li>1</li>
               <li>1</li><li>1</li><li>1</li>
               <li>1</li><li>1</li><li>1</li>
               <li>1</li><li>1</li><li>1</li>
               <li>1</li><li>1</li><li>1</li>
               <li>1</li><li>1</li><li>1</li>
               <li>1</li><li>1</li><li>1</li>
               <li>1</li><li>1</li><li>1</li>
               <li>1</li><li>1</li><li>1</li>
               <li>1</li><li>1</li><li>1</li>
               <li>1</li><li>1</li><li>1</li>
               <li>1</li><li>1</li><li>1</li>
               <li>1</li><li>1</li><li>1</li>
               <li>1</li><li>1</li><li>1</li>
               <li>1</li><li>1</li><li>1</li>
               <li>1</li><li>1</li><li>1</li>
               <li>1</li><li>1</li><li>1</li>
               <li>1</li><li>1</li><li>1</li>
               <li>1</li><li>1</li><li>1</li>
               <li>1</li><li>1</li><li>1</li>
               <li>1</li><li>1</li><li>1</li>
               <li>1</li><li>1</li><li>1</li>
               <li>1</li><li>1</li><li>1</li>
            </ul>
        </div>
        <!-- <p class="x">加载更多...</p>
    </div>
</template>

<script>
import BScroll from 'better-scroll'
export default {
    data(){
        return{
            dropDown:false
        }
    },
    mounted(){
        this.scrollFn()
    },
    methods:{
        scrollFn(){
            this.$nextTick(() => {
                if (!this.scroll) {
                    this.scroll = new BScroll(this.$refs.bscroll, {
                        click: true,
                        scrollY: true,
                        probeType: 3
                    });
                }else{
                    this.scroll.refresh();
                }
                this.scroll.on('scroll', (pos) => {
                    console.log(pos.y,this.dropDown)
                    //如果下拉超过50px 就显示下拉刷新的文字
                    if(pos.y>50){
                        this.dropDown = true
                    }else{
                        this.dropDown = false
                    }
                })
                // //touchEnd（手指离开以后触发） 通过这个方法来监听下拉刷新
                // this.scroll.on('touchEnd', (pos) => {
                //     // 下拉动作
                //     if(pos.y > 50){
                //         console.log("下拉刷新成功")
                //         this.dropDown = false
                //     }
                //     //上拉加载 总高度>下拉的高度+10 触发加载更多
                //     if(this.scroll.maxScrollY>pos.y+10){
                //         console.log("加载更多")
                //         //使用refresh 方法 来更新scroll  解决无法滚动的问题
                //         this.scroll.refresh()
                //     }
                //     console.log(this.scroll.maxScrollY+"总距离----下拉的距离"+pos.y)
                // })
                // console.log(this.scroll.maxScrollY)
            });
        }
    }
}
</script>


<style scoped>
.bscroll{
    width: 100%;
    height:500px;
    overflow: hidden;
    background: #ff0000;
}
/*.bscroll-container{
}*/
.drop-down{
    position: absolute;
    top:0px;
    lefT:0px;
    width: 100%;
    height: 50px;
    line-height:50px;
    text-align: center;
    font-size:0.8rem;
    color:#red;
}
</style>
  -->
