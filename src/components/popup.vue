<template>
  <section>
    <button class="pointer" @click="$emit('togglePopup')">click me to open the popup</button>

    <section class="popup-container" :class="{ active: isActive }">
      <span class="close-btn" @click="$emit('togglePopup')">
        <img src="@/assets/popup_img/X.jpg" />
      </span>
      <span class="main-title">
        <img src="@/assets/popup_img/lemonade.png" alt="" />
        The Lemonade IPO takes place today
      </span>
      <span class="sub-title">Will we see a surge or a crash?</span>
      <span class="btn">
        <span class="desktop">Find out more</span><span class="mobile">Act now</span>
      </span>
    </section>

  </section>
</template>

<script>
export default {
  name: "popup",
  props: {
    isActive: {
      type: Boolean,
      default: false,
    },
  },
};
</script>
