<template>
  <div class="home-top">
    <h3>人气商品</h3>
    <div class="content">
      <van-card
        v-for="item in GoodsList"
        :key="item.id"
        :tag="item.tag"
        :price="item.retail_price"
        :origin-price="item.origin_price"
        :desc="item.goods_brief"
        :title="item.name"
        :thumb="item.list_pic_url"
      >
      </van-card>
    </div>
  </div>
</template>

<script setup>
const GoodsList = [
  {
    retail_price: '3699.00',
    origin_price: '4399.00',
    name: '华硕笔记本',
    goods_brief: '华硕无双(酷睿i5-12500H/16GB/512GB/120Hz/15.6寸)、高性能',
    list_pic_url: '/images/top1.jpg',
    tag: 'TOP1'
  },
  {
    retail_price: '9999.00',
    origin_price: '10098.00',
    name: 'iPad Pro2024',
    goods_brief: '全新 iPad Pro 采用轻薄新设计，配备突破性超精视网膜 XDR 显示屏，M4 芯片注入强悍性能和重量级 AI 实力，带来震撼飞跃',
    list_pic_url: '/images/top2.jpg',
    tag: 'TOP2'
  },
  {
    retail_price: '128.00',
    origin_price: '168.00',
    name: '休闲懒人沙发',
    goods_brief: '轻松看书、社交、办公、舒适放松',
    list_pic_url: '/images/top3.jpg',
    tag: 'TOP3'
  },
  {
    retail_price: '199.00',
    origin_price: '205.00',
    name: '儿童积木',
    goods_brief: '大颗粒 家长更放心 不易吞咽、安全性高',
    list_pic_url: '/images/top4.jpg',
    tag: 'TOP4'
  },
  {
    retail_price: '59.00',
    origin_price: '99.00',
    name: '大学生窗帘',
    goods_brief: '韩星U型双轨道床帘强遮光学生宿舍蚊帐一体式上铺寝室u形导轨支架',
    list_pic_url: '/images/top5.jpg',
    tag: 'TOP5'
  }
]
</script>

<style lang="less" scoped>
.home-top {
  h3 {
    font-size: 22px;
    line-height: 30px;
    text-align: center;
    margin: 0.5rem 0;
  }
  .content {
    --van-tag-primary-color: #FF8000;
    --van-card-font-size: 16px;
    --van-card-background: #f9f9f9;
    background: var(--van-card-background);
    :deep(.van-card) {
      margin-top: 0;
      .van-card__title {
        padding: 10px 0 5px;
      }
      .van-card__price-currency {
        font-size: var(--van-card-font-size);
      }
    }
  }
  &::after {
    content: '';
    display: block;
    height: 3rem;
  }
}
</style>