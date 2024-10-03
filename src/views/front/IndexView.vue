<template>
  <SwiperHeader />
  <SwiperAd class="ms-sm-5" id="breakpoint" />
  <MenuModel />
  <Advantage />
  <Vedio />
  <Feeback />
</template>

<script>
import SwiperHeader from '@/components/index/SwiperBgModel.vue';
import SwiperAd from '@/components/index/SwiperAdModel.vue';
import MenuModel from '@/components/index/MenuModel.vue';
import Advantage from '@/components/index/AdvantageModel.vue';
import Vedio from '@/components/index/VedioModel.vue';
import Feeback from '@/components/index/FeedbackModel.vue';

export default {
  components: {
    SwiperHeader,
    SwiperAd,
    MenuModel,
    Advantage,
    Vedio,
    Feeback,
  },
};
</script>
