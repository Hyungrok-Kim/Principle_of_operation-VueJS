<template>
  <main>
      <product-title :isShow="isShow" :title="title"></product-title>
      <custom-button>전역 버튼</custom-button>
      <product-list></product-list>
      <!-- 
        Vue에서 자식 컴포넌트에 props 넘기는 방법 
        :posts는 prop명, "posts"는 실제 넘기고자하는 변수명  
      -->
  </main>
</template>


<script>
import ProductTitle from './product-title.vue';
import ProductList from './product-list.vue';
import CustomButton from '@/global-components/CustomButton.vue';

export default {
  name: 'ProductMain',
  components: {
    // HelloWorld,
    ProductTitle,
    ProductList,
    CustomButton,
  },

  data() {
    return {
        isShow: true,
        title: '상품 목록',
    };
  }
}
</script>

<style>

</style>