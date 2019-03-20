<template>
  <div>
    <detail-banner></detail-banner>
    <detail-header></detail-header>
    <div class="content">
      <detail-list :list="list"></detail-list>
    </div>
  </div>
</template>

<script>
  import DetailHeader from './components/header';
  import DetailBanner from './components/banner';
  import DetailList from './components/list';
  export default {
    name: 'Detail',
    components: {
      DetailBanner,
      DetailHeader,
      DetailList
    },
    data() {
      return {
        list: [{
          title: '成人票',
          children: [{
            title: '二级目录',
            children: [{
              title: '三级目录'
            }]
          }, {
            title: '二级目录'
          }]
        }, {
          title: '学生票'
        }, {
          title: '儿童票'
        }, {
          title: '特价票'
        }]
      };
    }
  };
</script>

<style lang="stylus" scoped>
  .content
    height: 50rem;
</style>
