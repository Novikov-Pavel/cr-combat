<template>
  <div class="position">
    <div class="position__title">
      <h2 class="position__name">Hi, Michael</h2>
      <div class="position__coins"><img :src="dollar" :alt="dollar" /> 100</div>
    </div>
    <div class="position__my_position">
      <div class="position__block">
        <p class="position__text">Your position</p>
        <p class="position__I">11 451</p>
        <p class="position__users">of 1452 users</p>
      </div>
      <div class="position__earn">
        <div class="position__earn_info">
          <p>You earn</p>
          <img :src="dollar" :alt="dollar" />
          <p>1</p>
        </div>
        <div>for 1 people after you</div>
        <button type="button" class="position__reward">Get Daily reward</button>
      </div>
    </div>
  </div>
</template>

<script setup lang="ts">
import dollar from "../assets/icons/dollar.svg";
</script>

<style scoped lang="scss">
.position {
  &__my_position {
    background-color: #811fff;
    border-radius: 20px;
    position: relative;
  }
  &__earn {
    background-color: #5e00d6;
    margin: 8px 11px;
    border-radius: 20px;
    position: relative;
    bottom: 11px;
    display: flex;
    flex-direction: column;
    gap: 10px;
    padding: 16px;
    &_info {
      display: flex;
      align-items: center;
      gap: 10px;
      font-size: 20px;
      font-weight: 600;
    }
  }
  &__reward {
    color: #811fff;
    padding: 16px 70px;
    font-size: 16px;
    font-weight: 600;
    border-radius: 16px;
  }
  &__block {
    display: flex;
    flex-direction: column;
    padding: 28px 24px;
    &::after {
      content: url("../assets/icons/fox.png");
      position: absolute;
      right: 0;
      top: 0;
    }
  }
  &__text {
    font-weight: 600;
    font-size: 24px;
  }
  &__I {
    font-weight: 600;
    font-size: 54px;
  }
  &__users {
    font-weight: 400;
    font-size: 16px;
  }
  margin: 0 24px;
  &__title {
    display: flex;
    justify-content: space-between;
    align-items: center;
  }
  &__name,
  &__coins {
    font-size: 24px;
    font-weight: 600;
  }
  &__coins {
    display: flex;
    justify-content: space-between;
    align-items: center;
    gap: 8px;
  }
}
</style>
