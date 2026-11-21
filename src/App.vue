
<script setup>
import { ref } from 'vue'

const count = ref(0)

function increase() {
  count.value++
}

function decrease() {
  if (count.value > 0) {
    count.value--
  }
}

function reset() {
  count.value = 0
}
</script>

<template>
  <div class="page" dir="rtl">
    <div class="counter-box">

      <div class="icon">✦</div>

      <p class="small-title">MY COUNTER</p>

      <h1>شمارنده من</h1>

      <p class="description">
        هر قدم کوچک، یک پیشرفت بزرگ است.
      </p>

      <div class="number">
        {{ count }}
      </div>

      <p class="count-text">تعداد شمارش</p>

      <div class="buttons">
        <button class="plus" @click="increase">+</button>
        <button class="minus" @click="decrease">−</button>
      </div>

      <button class="reset" @click="reset">
        بازنشانی شمارنده
      </button>

      <div class="footer-text">
        Keep Growing ✿
      </div>

    </div>
  </div>
</template>

<style scoped>
* {
  box-sizing: border-box;
}

.page {
  min-height: 100vh;
  background-color: #e9eadf;
  display: flex;
  justify-content: center;
  align-items: center;
  padding: 20px;
  font-family: Tahoma, sans-serif;
}

.counter-box {
  background-color: #faf9f4;
  width: 100%;
  max-width: 400px;
  padding: 40px 30px;
  border-radius: 25px;
  text-align: center;
  box-shadow: 0 10px 30px rgba(53, 67, 43, 0.12);
}

.icon {
  color: #89966a;
  font-size: 35px;
}

.small-title {
  color: #89966a;
  letter-spacing: 4px;
  font-size: 12px;
  margin-top: 10px;
}

h1 {
  color: #35432b;
  font-size: 30px;
  margin: 15px 0;
}

.description {
  color: #777d6b;
  font-size: 14px;
}

.number {
  background-color: #e9eadf;
  color: #35432b;
  font-size: 65px;
  font-weight: bold;
  padding: 20px;
  margin-top: 30px;
  border-radius: 18px;
}

.count-text {
  color: #89966a;
  font-size: 13px;
  margin-bottom: 25px;
}

.buttons {
  display: flex;
  justify-content: center;
  gap: 20px;
}

button {
  cursor: pointer;
  border: none;
  font-family: inherit;
}

.plus,
.minus {
  width: 65px;
  height: 55px;
  border-radius: 14px;
  font-size: 30px;
  color: white;
  background-color: #89966a;
}

.plus:hover,
.minus:hover {
  background-color: #35432b;
}

.reset {
  background-color: #35432b;
  color: white;
  padding: 12px 25px;
  border-radius: 10px;
  margin-top: 25px;
  font-size: 13px;
}

.reset:hover {
  background-color: #89966a;
}

.footer-text {
  color: #89966a;
  font-size: 12px;
  margin-top: 30px;
  letter-spacing: 2px;
}
</style>
