<template>
  <div class="list">
    <div v-for="item in listData"
         class="list-item">
      <span class="icon">
        <svg :fill="item.iconColor">
          <use :xlink:href="item.icon"></use>
        </svg>
      </span>
      <div class="info"><span>{{item.info}}</span></div>
    </div>
  </div>
</template>

<script>
  export default {
    name: "ListView",
    props: {
      listData: {
        type: Array,
        default() {
          return [];
        },
      },
    },
  }
</script>

<style scoped>
  .list {
    background-color: #fff;
  }
  .list .list-item {
    height: 36px;
  }
  .list .list-item .icon {
    position: absolute;
    left: 16px;

    margin-top: 4px;
  }
  .list .list-item .icon svg {
    width: 14px;
    height: 14px;
  }
  .list .list-item .info {
    margin-left: 60px;
    font-size: 14px;
    line-height: 36px;

    border-bottom: 1px solid rgba(100, 100, 100, .1);
  }
</style>
