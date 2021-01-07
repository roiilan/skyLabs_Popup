<template>
  <div class="home">
    <div @click="isActive = false" class="backdrop" :class="{ active: isActive }"></div>
    <popup class="popup" :isActive="isActive" @togglePopup="isActive = !isActive" />
  </div>
</template>

<script>
// @ is an alias to /src
import popup from "@/components/popup.vue";

export default {
  name: "Home",
  components: {
    popup,
  },
  data() {
    return {
      isActive: true,
    };
  },
};
</script>
