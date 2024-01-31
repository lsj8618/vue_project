<template>
  <div class="header">
    <div @mouseover="isHover = false" v-if="isHover" class="header-class">
      <div class="logo">
        <img src="../assets/deuNavLogo.png" alt="132" />
      </div>
      <div class="header2-claas">
        <div class="header-sub-class" v-for="(text, i) in headerTexts" :key="i">
          <span class="header-text">{{ text }}</span>
        </div>
      </div>
    </div>
    <div @mouseleave="isHover = true" v-else class="header-class-2">
      <div
        class="header-sub-class-2"
        v-for="i in 6"
        :key="i"
        @mouseover="isActive = i"
      >
        <div class="header-text-2" :class="{ isActive: isActive === i }"></div>
        <div
          style="margin-top: 1rem; width: 100%"
          :class="{ isActive2: isActive === i }"
        >
          <div
            style="margin-top: 1rem"
            v-for="(subText, i) in subTexts"
            :key="i"
            class="header-sub-text"
            @click="$router.push({ path: '/about' })"
          >
            {{ subText }}
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
      headerTexts: [
        "사업단소개",
        "참여기업현황",
        "학과소개",
        "입학안내",
        "창의융합교육센터",
        "커뮤니티",
      ],
      subTexts: ["인사말1", "인사말2", "인사말3"],
    };
  },
};
</script>

<style scoped>
.header-class {
  width: 1540px;
  display: flex;
  justify-content: space-between;
  padding: 0.6rem 10rem;
  margin: 0 auto;
}
.header {
  width: 100%;
  background-color: rgba(0, 0, 0, 0.48);
}
.header-sub-class {
  padding: 0 15px;
  margin: 0 35px;
  min-width: max-content;
  font-size: 1.25rem;
}
.header2-claas {
  width: 65%;
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: center;
  margin-right: 40px;
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
  justify-content: flex-end;
  padding: 2rem 200px;
  background-color: white;
}

.header-sub-class-2 {
  padding: 20px 50px;
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
  margin: 0 auto;
  align-items: center; /* 세로 방향으로 가운데 정렬 */
}

.header-text {
  color: white;
}
</style>
