<template>
  <div id="app">
      <v-header />
      <div class="tab border-1px">
        <div class="tab-item">
          <router-link to="/goods">商品</router-link>
        </div>
        <div class="tab-item">
          <router-link to="/ratings">评价</router-link>
        </div>
        <div class="tab-item">
          <router-link to="/seller">商家</router-link>
        </div>     
      </div>
      <router-view/>
  </div>
</template>

<script>
import VHeader from '@/components/header/header.vue'
export default {
    components: {
      VHeader
    }
}
</script>
<style lang="scss" scoped>
@import "./common/mixin.scss";
    .tab{
      display: flex;
      @include border-1px(#ccc);
      .tab-item{
        flex: 1;
        height: .4rem;
        line-height:.4rem;
        
        text-align: center;
        font-size: .14rem;
        color: rgb(77, 85, 93);
        
        & > a{
            display: block;  //块

        }
        & > a.active{
           color: rgb(240,20,20);
        }
      }
    }
</style>
