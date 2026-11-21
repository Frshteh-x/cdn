
<template>
  <div class="container">
    <div class="counter-card">
      <span class="title">COUNTER</span>

      <div class="number">{{ count }}</div>

      <div class="buttons">
        <button class="btn minus" @click="count--">−</button>
        <button class="btn plus" @click="count++">+</button>
      </div>

      <button class="reset" @click="count = 0">
        RESET
      </button>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      count: 0
    }
  }
}
</script>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  background: #080b12;
  font-family: Arial, sans-serif;
}

.container {
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  background: radial-gradient(circle, #101d35, #080b12 70%);
}

.counter-card {
  background: #0c1220;
  border: 1px solid #1e90ff;
  box-shadow: 0 0 25px #007bff30;
  border-radius: 20px;
  padding: 40px;
  width: 320px;
  text-align: center;
}

.title {
  color: #60aaff;
  letter-spacing: 5px;
  font-size: 14px;
}

.number {
  color: #ffffff;
  font-size: 80px;
  font-weight: bold;
  margin: 30px 0;
  text-shadow: 0 0 20px #007bff80;
}

.buttons {
  display: flex;
  justify-content: center;
  gap: 20px;
}

.btn {
  width: 65px;
  height: 65px;
  border-radius: 50%;
  font-size: 30px;
  cursor: pointer;
  border: 1px solid #1688ff;
  transition: 0.3s;
}

.plus {
  background: #1688ff;
  color: white;
}

.minus {
  background: transparent;
  color: #1688ff;
}

.btn:hover {
  box-shadow: 0 0 20px #1688ff;
  transform: scale(1.08);
}

.reset {
  margin-top: 25px;
  width: 100%;
  padding: 12px;
  background: transparent;
  color: #60aaff;
  border: 1px solid #243b60;
  border-radius: 10px;
  letter-spacing: 3px;
  cursor: pointer;
  transition: 0.3s;
}

.reset:hover {
  background: #1688ff;
  color: white;
  border-color: #1688ff;
}
</style>
