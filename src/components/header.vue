<template>
  <div id="header">
      <ul class="nav">
        <li>
            <a href="">
                세트 상품
            </a>
        </li>
        <li>
            개별 상품
            <ul>
                <li>
                    <a href="">동물</a>
                </li>
                <li>
                    <a href="">사람</a>
                </li>
                <li>
                    <a href="">건물</a>
                </li>
                <li>
                    <a href="">시리즈</a>
                </li>
            </ul>
        </li>
        <li>
            세일
        </li>
        <li>
            Collection
        </li>
      </ul>
      <div class="my-menu">
          <div :v-if="user.login === true" @click="goToLike">
              like
              <span>{{likeCnt}}</span>
          </div>
          <div :v-if="user.login === true" @click="goToCart">
              cart
              <span>{{cartCnt}}</span>
          </div>
          <div @click="goToMy">
              {{user.name}}
          </div>
      </div>
  </div>
</template>

<script>
export default {
    name:'comm-header',
    data(){
        return{
            user:{
                login:false,
                name:'로그인'
            },
            likeCnt:null,
            cartCnt:null
        }
    },
    methods:function(){
        goToLike = function(){

        },
        goToCart = function(){

        },
        goToMy = function(){
            // 로그인 상태일 때는 마이 페이지로 이동하고 아닐 땐 로그인 모달을 띄움
            if(this.user.login == true){

            }
        }
    }
}
</script>

<style>
    #header {
        width:100%;
        height:70px;
        border-bottom:1px solid #ddd;
        background-color:#fff;
        
    }
</style>