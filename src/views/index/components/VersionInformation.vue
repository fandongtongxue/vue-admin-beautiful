<template>
  <a-alert
    :message="
      '欢迎体验全网首个基于 vue ' +
      dependencies['vue'] +
      ' + ant-design-vue ' +
      dependencies['ant-design-vue'] +
      ' 开发的admin框架vue-admin-beautiful-antdv，vue3.0的流畅超乎了我们的想象，感谢尤雨溪、唐金州的开源项目我带来的灵感和帮助，vue-admin-beautiful-antdv同时支持电脑、平板、手机，希望实现一套代码即可帮助中小微企业快速实现项目落地，帮助前端小白快速入门vue前端框架搭建技术，迅速在工作中占据主导地位。'
    "
    type="success"
    show-icon
  />
</template>
<script>
  import { dependencies, devDependencies } from '*/package.json'

  export default {
    data() {
      return {
        updateTime: process.env.VUE_APP_UPDATE_TIME,
        dependencies: dependencies,
        devDependencies: devDependencies,
      }
    },
  }
</script>
<style lang="less" scoped>
  .version-information {
    margin-top: @vab-margin;
    &-table {
      width: 100%;
      overflow: scroll;
      table {
        width: 100%;
        color: #666;
        border-collapse: collapse;
        background-color: #fff;

        td {
          position: relative;
          padding: 9px 15px;
          font-size: 14px;
          line-height: 20px;
          border: 1px solid #e6e6e6;

          &:nth-child(odd) {
            width: 20%;
            text-align: right;
            background-color: #f7f7f7;
          }
        }
      }
    }
  }
</style>
