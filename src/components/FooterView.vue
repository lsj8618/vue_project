<template>
  <div class="Footer">
    <div class="container">
      <div class="content has-text-centered">
        <p><strong>Your Company</strong> © 2024. All rights reserved.</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "FooterView",
};
</script>

<style scoped>
.footer {
  background-color: #f5f5f5;
  padding: 20px 0;
  position: absolute;
  left: 0;
  bottom: 0;
  width: 100%;
}

.container {
  display: flex;
  justify-content: center;
}

.content {
  flex: 1;
  max-width: 1200px;
  padding: 0 20px;
}

p {
  margin-bottom: 0;
}
</style>
