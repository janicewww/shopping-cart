<template>
  <div class="goods-container">
      <!-- 左側圖 -->
      <div class="thumb">
          <div class="custom-control custom-checkbox">
              <input type="checkbox" class="custom-control-input" id="cb1" :checked="true" />
              <label class="custom-control-label" for="cb1">
                  <img :src="pic" alt="" />
              </label>
          </div>
      </div>

      <!-- 右側信息 -->
      <div class="goods-info">
          <!-- 商品標題 -->
          <h6 class="goods-title"> {{title}} </h6>
          <div class="goods-info-bottom">
              <!-- 商品價格 -->
              <span class="goods-price">£{{price}} </span>
              <!-- 商品數量 -->
          </div>
      </div>
  </div>
</template>

<script>
export default {
    props: {
        title: {
            default: '',
            type: String
        },

        pic: {
            default: '',
            type: String
        },

        price: {
            default: '0',
            type: Number
        }

    },

}
</script>


<style lang="less" scoped>
.goods-container {
    + .goods-container {
        border-top: 1px solid #efefef;
    }
    padding: 10px;
    display: flex;
    .thumb {
        display: flex;
        align-items: center;
        img {
            width: 100px;
            height: 100px;
            margin: 0 10px;
        }
    }
}

</style>