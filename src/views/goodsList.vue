'<template>
  <div class="list">
      <!-- 상품 필터링 영역 -->
      <div>
      </div>
      <!-- 상품 리스트 영역 -->
      <div>
          <ul class="goods">
              <li v-for="goods in goodsList" :key="goods">
                  <img :src="goods.img" :name="goods.name">
                  <p>
                      <span>{{goods.name}}</span>
                      <span>{{goods.price}}</span>
                  </p>
              </li>
          </ul>
      </div>
  </div>
</template>

<script>
    export default {
        data(){
            return {
                // 상품 목록 (제품사진, 제품명, 가격)
                goodsList:{
                    img:null,
                    name:null,
                    price:null
                }
            }
        }
    }
</script>

<style>

</style>'