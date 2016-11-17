<template>
    <article id="app">
      <div class="hello_img">
        <img src="./assets/imgs/wife_head_2.png">
      </div>
      <p class="msg_class">{{msg}}</p>
      <div class="clock_box">
        <div class="clock_content">
          <p class="clock_number">{{clockNumber}}</p>
        </div>
      </div>
    </article>

</template>

<script>
export default {
  name: 'app',
  data () {
    return {
      msg: '欢迎您的到访，@辛雯雯',
      countDown: true,
      imgShow: false,
      clockNumber: 10
    }
  },
  mounted () {
    this.timeCountDown();
  },
  methods: {
    timeCountDown: function () {
      let me = this;
      this.intervalTimeId = setInterval(function () {

          if(me.clockNumber != 0) {
            me.clockNumber --;
          }else {

          }
      }, 1000);
    }
  }
}
</script>

<style>
  html{
    width: 100%;
    height: 100%;
    min-height: 100%;
    font-size: 50px;
  }
  body{
    width: 100%;
    height: 100%;
    min-height: 100%;
    background: #eee;
    margin: 0;
  }
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  width: 100%;
  height: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
}
  #app img{
    width: 100%;
    height: 100%;
  }
  #app p{
    width: 100%;
  }
  .msg_class{
    width: 100%;
    height: 1rem;
    line-height: 1rem;
    font-size: 0.32rem;
  }
  .hello_img{
      width: 6rem;
  }
  .hello_img_big{
      width: 3rem;
  }
  .hello_img img{
    border-radius: 50%;
  }
  .clock_box{
    width: 3rem;
    height: 3rem;
    background: #dec93a;
    border-radius: 50%;
    display: flex;
    justify-content: center;
    align-items: center;
  }
  .clock_content{
    width: 2rem;
    height: 2rem;
    background: #de6c3a;
    border-radius: 50%;
    display: flex;
    justify-content: center;
    align-items: center;
  }
</style>
