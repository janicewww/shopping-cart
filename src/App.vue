<template>
  <div class="app-container">
    <Header title="Shopping Cart"></Header>
    <Goods v-for="item in list" :key="item.id" :title="item.goods_name" :pic="item.goods_img" :price="item.goods_price"></Goods>
  </div>
</template>

<script>
import axios from 'axios'
import Header from '@/components/Header/Header.vue'
import Goods from '@/components/Goods/Goods.vue'

export default {

  data() {
    return {
      // 用來存 Shopping Cart 數據
      list: []
    }
  },

  created() {
    this.initCartList()
  },

  methods: {
    async initCartList() {
      const { data: res } = await axios.get('https://www.escook.cn/api/cart')
      if(res.status === 200) {
        this.list = res.list
      }
    }
  },

  components: {
    Header,
    Goods
  }

}
</script>

<style lang="less" scoped>
.app-container {
  padding-bottom: 55px;
}

</style>