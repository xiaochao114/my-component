<template>
  <div class="centent">
    <div class="led led-blue"></div>
    <div class="led led-red"></div>
  </div>
</template>

<script>
export default {

}
</script>

<style scoped>
.centent {
  height: 100vh;
  width: 100vw;
  display: flex;
  align-items: center;
  justify-content: center;
  margin: 0;
  gap: 40px;
  background: rgb(220, 220, 220);
}

.led {
  width: 80px;
  height: 80px;
  border-radius: 100%;
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.4), 0 2px 1px rgba(0, 0, 0, 0.08);
  cursor: pointer;
}

.led:after {
  display: block;
  content: "";
  width: 60px;
  height: 48px;
  border-radius: 100%;
  margin: 4px auto;
  background: rgb(255, 255, 255);
  background: linear-gradient(0deg,
      rgba(255, 255, 255, 0.2) 0%,
      rgba(255, 255, 255, 0.8) 100%);
}

.led-blue {
  background: rgb(0, 103, 175);
  background: linear-gradient(0deg,
      rgba(225, 243, 255, 1) 0%,
      rgba(0, 103, 175, 1) 100%);
}

.led-blue.on {
  background: radial-gradient(circle,
      rgba(255, 255, 255, 1) 0%,
      rgba(255, 255, 255, 1) 50%,
      rgba(0, 103, 175, 1) 100%);
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.4), 0 2px 1px rgba(0, 0, 0, 0.08),
    0 0 30px rgba(0, 103, 175, 1), 0 0 5px 5px rgba(255, 255, 255, 1);
}

.led-red {
  background: rgb(175, 20, 0);
  background: linear-gradient(0deg,
      rgba(255, 225, 225, 1) 0%,
      rgba(175, 20, 0, 1) 100%);
}

.led-red.on {
  background: radial-gradient(circle,
      rgba(255, 255, 255, 1) 0%,
      rgba(255, 255, 255, 1) 50%,
      rgba(175, 20, 0, 1) 100%);
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.4), 0 2px 1px rgba(0, 0, 0, 0.08),
    0 0 30px rgba(175, 20, 0, 1), 0 0 5px 5px rgba(255, 255, 255, 1);
}
</style>