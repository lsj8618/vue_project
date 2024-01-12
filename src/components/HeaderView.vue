<template>
  <div style="min-width: 100%">
    <div @mouseover="isHover = false" v-if="isHover" class="header-class">
      <div class="logo">
        <img src="../assets/deuNavLogo.png" alt="132" />
      </div>
      <div class="header-sub-class" v-for="i in 6" :key="i">
        <span class="header-text">사업단 소개</span>
      </div>
    </div>
    <div @mouseleave="isHover = true" v-else class="header-class-2">
      <div
        class="header-sub-class-2"
        v-for="i in 6"
        :key="i"
        @mouseover="isActive = i"
      >
        <div class="header-text-2" :class="{ isActive: isActive === i }">
          사업단 소개
        </div>
        <div
          style="margin-top: 1rem; width: 100%"
          :class="{ isActive2: isActive === i }"
        >
          <div
            style="margin-top: 1rem"
            v-for="i in 3"
            :key="i"
            class="header-sub-text"
            @click="$router.push({ path: '/about' })"
          >
            인사말{{ i }}
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      isHover: false,
      isActive: -1,
    };
  },
};
</script>
<style scoped>
.header-class {
  display: flex;
  justify-content: center;
  padding: 2rem 10rem;
  background-color: rgb(224, 211, 211);
}
.header-sub-class {
  padding: 0 30px;
  min-width: max-content;
  font-size: 1.25rem;
}
.header-text:hover {
  color: blue;
}
.isActive {
  position: relative;
  border-bottom: 1px solid #aaa;
}

.header-class-2 {
  display: flex;
  justify-content: center;
  padding: 2rem 10rem;
  background-color: white;
}
.header-sub-class-2 {
  padding: 0 30px;
  min-width: max-content;
  font-size: 1.25rem;
}
.header-text-2:hover {
  color: blue;
}
.header-sub-text:hover {
  color: blue;
}
.isActive2 {
  background-color: rgb(234, 229, 229);
}
.logo > img {
  width: 293px;
  height: 63px;
}
</style>
