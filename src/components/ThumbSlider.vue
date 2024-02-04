<script setup>
import { ref } from "vue";
const fullImg = ref(
  "https://cdn.pixabay.com/photo/2015/04/23/22/00/tree-736885_1280.jpg"
);

const Images = ref([
  {
    Thumb:
      "https://cdn.pixabay.com/photo/2015/04/23/22/00/tree-736885_1280.jpg",
    Full: "https://cdn.pixabay.com/photo/2015/04/23/22/00/tree-736885_1280.jpg",
  },
  {
    Thumb: "https://images.pexels.com/photos/414612/pexels-photo-414612.jpeg",
    Full: "https://images.pexels.com/photos/414612/pexels-photo-414612.jpeg",
  },
  {
    Thumb:
      "https://cdn.pixabay.com/photo/2014/02/27/16/10/flowers-276014_1280.jpg",
    Full: "https://cdn.pixabay.com/photo/2014/02/27/16/10/flowers-276014_1280.jpg",
  },
  {
    Thumb:
      "https://unblast.com/wp-content/uploads/2021/01/Space-Background-Images.jpg",
    Full: "https://unblast.com/wp-content/uploads/2021/01/Space-Background-Images.jpg",
  },
  {
    Thumb:
      "https://images.panda.org/assets/images/pages/welcome/orangutan_1600x1000_279157.jpg",
    Full: "https://images.panda.org/assets/images/pages/welcome/orangutan_1600x1000_279157.jpg",
  },
  {
    Thumb:
      "https://cdn.pixabay.com/photo/2018/01/12/10/19/fantasy-3077928_1280.jpg",
    Full: "https://cdn.pixabay.com/photo/2018/01/12/10/19/fantasy-3077928_1280.jpg",
  },
]);
const setImage = (img) => {
  fullImg.value = img.Full;
};
</script>
<template>
  <div class="w-full">
    <h3 class="text-center text-2xl text-info font-serif font-semibold mb-5">
      Custom Thumb Image Slider
    </h3>

    <div class="grid grid-cols-4 gap-3">
      <Transition type="animation" name="bounce">
        <img class="col-span-3 h-full w-full" :src="fullImg" alt="" />
      </Transition>
      <div class="">
        <img
          class="w-[200px] h-[150px] mb-3 border border-slate-400 rounded cursor-pointer"
          @click="setImage(img)"
          v-for="(img, index) in Images"
          :key="index"
          :src="img.Thumb"
          alt=""
        />
      </div>
    </div>
  </div>
</template>
<style scoped>
.bounce-enter-active {
  animation: bounce-in 0.5s;
}
.bounce-leave-active {
  animation: bounce-in 0.5s reverse;
}
@keyframes bounce-in {
  0% {
    transform: scale(0);
  }
  50% {
    transform: scale(1.25);
  }
  100% {
    transform: scale(1);
  }
}
</style>
