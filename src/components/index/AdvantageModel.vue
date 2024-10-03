<template>
  <section class="card border-0 rounded-0 bg-white overflow-hidden pe-sm-5">
    <div
      class="text-white pt-5 ps-sm-5 advantageSit"
      :style="{
        'background-image':
          'url(' + require('@/assets/images/advantageBg.jpg') + ')',
        'border-radius': '0 24px 0 0',
      }"
    >
      <h4 class="mb-2">卷民wrrrry的四大優勢</h4>
      <h2 class="mb-5 d-flex">
        <i
          class="fas fa-exclamation me-3"
          style="animation-delay: calc(1s * 0.1)"
          data-aos="animate__rotateInDownLeft"
        ></i>
        <span
          style="animation-delay: calc(1s * 0.2)"
          data-aos="animate__rotateInDownLeft"
          >爲</span
        >
        <span
          style="animation-delay: calc(1s * 0.3)"
          data-aos="animate__rotateInDownLeft"
          >何</span
        >
        <span
          style="animation-delay: calc(1s * 0.4)"
          data-aos="animate__rotateInDownLeft"
          >選</span
        >
        <span
          style="animation-delay: calc(1s * 0.5)"
          data-aos="animate__rotateInDownLeft"
          >擇</span
        >
        <span
          style="animation-delay: calc(1s * 0.6)"
          data-aos="animate__rotateInDownLeft"
          >捲</span
        >
        <span
          style="animation-delay: calc(1s * 0.7)"
          data-aos="animate__rotateInDownLeft"
          >民</span
        >
        <span
          style="animation-delay: calc(1s * 0.8)"
          data-aos="animate__rotateInDownLeft"
          >W</span
        >
        <span
          style="animation-delay: calc(1s * 0.9)"
          data-aos="animate__rotateInDownLeft"
          >r</span
        >
        <span
          style="animation-delay: calc(1s * 1)"
          data-aos="animate__rotateInDownLeft"
          >rrrry</span
        >
      </h2>
      <div>
        <!-- 1 -->
        <template v-for="(item, index) in advantageList" :key="index">
          <div class="py-8 d-block text-dark text-decoration-none advantageBox">
            <div
              class="px-5 py-4 shadow-lg col-12 col-sm-5"
              :class="`marginLeft-${index}`"
            >
              <h2 class="mb-2">#{{ index + 1 }}</h2>
              <h3 class="mb-0 text-black-50">
                {{ item.title }}
              </h3>
            </div>
          </div>
        </template>
      </div>
    </div>
  </section>
</template>

<style scoped>
.marginLeft-0 {
  margin-left: 0%;
  background: hsla(0, 0%, 100%, 0.5);
}
.marginLeft-1 {
  margin-left: 10%;
  background: hsla(0, 0%, 100%, 0.6);
}
.marginLeft-2 {
  margin-left: 0%;
  background: hsla(0, 0%, 100%, 0.7);
}
.marginLeft-3 {
  margin-left: 10%;
  background: hsla(0, 0%, 100%, 0.8);
}
.advantageSit {
  background-repeat: no-repeat;
  background-position: center center;
  background-size: cover;
}
.advantageBox {
  border: 10px solid #fff;
  border-bottom: 0px;
}
@media (max-width: 576px) {
  .marginLeft-1 {
    margin-left: 0%;
  }
  .marginLeft-3 {
    margin-left: 0%;
    border-bottom:10px solid #fff;
  }
}
</style>

<script>
export default {
  data() {
    return {
      advantageList: [
        { title: '涵蓋必考跨版本精選文章，融物理學常識於課程中' },
        { title: '鞭辟入裡解說物理段考進度不錯過，陪孩子超前部署' },
        { title: '講義搭配試題以及無力實驗詳解解構題目破解知識點' },
        { title: '晦澀難懂的物理知識在俊民老師講述下生動有趣' },
      ],
    };
  },
};
</script>
