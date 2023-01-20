<template>
  <!--  <div class="w-80 m-auto my-2">-->
  <!--    <Input label="用户名"></Input>-->
  <!--    <Input label="密码"></Input>-->
  <!--    <Button>登录</Button>-->
  <!--  </div>-->
  <div class="ml-56 mr-80 p-5 pt-16 h-screen">
    <FileList>
      <template #metadata="{ metadata }">
        <MetadataBar :data="metadata" />
      </template>
    </FileList>
  </div>
  <Uploader />
  <ToolBar />
  <Sidebar>
    <UserBar />
  </Sidebar>
</template>
<script>
import Input from "~/components/Input/Input.vue";
import Button from "~/components/Button/Button.vue";
import Sidebar from "~/components/Sidebar/Sidebar.vue";
import UserBar from "~/components/UserBar/UserBar.vue";
import ToolBar from "~/components/ToolBar/ToolBar.vue";
import FileList from "~/components/File/FileList.vue";
import Uploader from "~/components/File/Uploader.vue";
import MetadataBar from "~/components/Sidebar/MetadataBar.vue";
export default {
  meta: {
    title: "盐云",
  },
  components: {
    Uploader,
    Input,
    Button,
    Sidebar,
    UserBar,
    ToolBar,
    FileList,
    MetadataBar,
  },
};
</script>
<style>
body {
  overflow: hidden;
}
</style>
