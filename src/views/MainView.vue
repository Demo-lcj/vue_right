<template>
  <div class="mainview">
    <el-container>
      <el-header>
        <header-view></header-view>
      </el-header>
      <el-container>
        <el-aside>
          <tree-view></tree-view>
        </el-aside>
        <el-container>
          <el-main>
            <role></role>
          </el-main>
          <el-footer>Footer</el-footer>
        </el-container>
      </el-container>
    </el-container>
  </div>
</template>
<script>
import HeaderView from "../components/HeaderView";
import TreeView from "../components/TreeView";
import Role from "../components/role";
export default {
  name: "mainview",
  data() {
    return {};
  },
  components: {
    "header-view": HeaderView,
    "tree-view": TreeView,
    role: Role
  }
};
</script>
<style scoped lang="scss">
.mainview {
  height: 100%;
}
.mainview > .el-container {
  width: 100%;
  height: 100%;
  display: flex;
  flex-direction: column;
  justify-content: start;
  .el-header {
    flex: 0 0 60px;
    width: 100%;
    background-color: #b3c0d1;
    line-height: 60px;
  }
  .el-container {
    flex: 1;
    width: 100%;
    display: flex;
    flex-direction: row;
    justify-content: flex-start;
    .el-aside {
      flex: 0 0 250px;
      height: 100%;
      background-color: #fff;
      color: #333;
      text-align: center;
      line-height: 160px;
    }
    .el-container {
      flex: 1;
      height: 100%;
      display: flex;
      flex-direction: column;
      justify-content: start;
      .el-main {
        //可以解决这个table撑得过大的bug
        flex: 1 1 500px;
        width: 100%;
        background-color: #e9eef3;
        color: #333;
        text-align: center;
        line-height: 160px;
      }
      .el-footer {
        flex: 0 0 60px;
        width: 100%;
        background-color: #b3c0d1;
        color: #333;
        text-align: center;
        line-height: 60px;
      }
    }
  }
}
</style>

<style lang="scss">
//没有scoped则说明是设置全局的样式
html,
body,
#app {
  height: 100%;
  width: 100%;
}
</style>
