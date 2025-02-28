<template>
  <div class="nav-home">
    <div class='logo-container'>
      <img src="../assets/PublicImage/logo.png" alt="Logo" class="logo">
      <p class='text-logo'>SmartMath</p>
    </div>
    <div class="nav-text">
      <a href="#/about" class="text-start-chat">开始对话</a>
      <a href="#/about" class="text-open-api">API开放平台</a>
    </div>
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue';

export default defineComponent({
  name: 'NavHome',
});
</script>

<style scoped>
.nav-home {
  position: relative;
  display: flex;  
}

.logo-container {
  position: relative;
  left: 30px;
  top: 5px;
  width: 0px;
  height: 129.69px;
  opacity: 1;
  display: flex;
  align-items: center; /* Center vertically */
  justify-content: space-between;
}

.logo {
  width: 80px; 
  height: 80px; /* 让高度和宽度相等 */
  border-radius: 50%; /* 将容器的角半径设置为 50% 以形成圆形 */
  object-fit: cover; /* 确保图片覆盖整个圆形区域，避免变形 */
}

.text-logo {
  font-family: 'Kalam-Light';
  position: relative;
  color: rgba(121, 72, 234, 1);
  font-size: 28px;
  letter-spacing: 2px;
  left: 20px;
}

.nav-text {
  position: relative;
  display: flex;
  font-family: '得意黑';
  top: 70px;
  left: 1200px; /* Adjust the horizontal position */
  color: rgb(0, 0, 0);
  font-size: 25px;
  letter-spacing: 2px;
  text-decoration-line: underline;
}

.text-start-chat{
  position: relative;
  left: 320px;
  color: inherit; /* 继承父元素的颜色 */
  text-decoration: inherit; /* 继承父元素的文本装饰 */
}

.text-start-chat:active {
  color: inherit; /* 点击时颜色不变 */
  text-decoration: inherit; /* 点击时文本装饰不变 */
}

.text-open-api{
  position: relative;
  left: 380px;
  color: inherit; /* 继承父元素的颜色 */
  text-decoration: inherit; /* 继承父元素的文本装饰 */
}

.text-open-api:active {
  color: rgba(121, 72, 234, 1); /* 点击时颜色不变 */
  text-decoration: inherit; /* 点击时文本装饰不变 */
}
</style>