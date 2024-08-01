<template>
  <div class="list">
    <h2 class="list__title">Get up in the wait list</h2>
    <div v-for="list in waitList" :for="list.iconTitle" class="list__waitList">
      <div class="list__item">
        <img :src="list.icon" :alt="list.icon" />
        <div>
          <p class="list__iconTitle">{{ list.iconTitle }}</p>
          <p class="list__infoItem">
            {{ list.infoItem }}
            <img :src="list.infoImg" :alt="list.infoImg" />
            <span class="list__countDollars">{{ list.countDollars }}</span>
          </p>
        </div>
      </div>
      <img :src="rightArrow" :alt="rightArrow" />
    </div>
    <div class="list__waitList list__waitList-about">
      <div>About the project</div>
      <img :src="rightArrow" :alt="rightArrow" />
    </div>
  </div>
</template>

<script setup lang="ts">
import wishlist1 from "../assets/icons/wishlist1.png";
import wishlist2 from "../assets/icons/wishlist2.png";
import wishlist3 from "../assets/icons/wishlist3.svg";
import wishlist4 from "../assets/icons/wishlist4.svg";
import rightArrow from "../assets/icons/rightarrow.svg";
import dollar from "../assets/icons/dollar.svg";

const waitList = [
  {
    icon: wishlist1,
    iconTitle: "Invite your friends",
    infoItem: "up to",
    infoImg: dollar,
    countDollars: "25 000",
  },
  {
    icon: wishlist2,
    iconTitle: "Subscribe",
    infoImg: dollar,
    countDollars: "245",
  },
  {
    icon: wishlist3,
    iconTitle: "Watch the video",
    infoImg: dollar,
    countDollars: "245",
  },
  {
    icon: wishlist4,
    iconTitle: "Watch the video",
    infoImg: dollar,
    countDollars: "245",
  },
];
</script>

<style scoped lang="scss">
.list {
  display: flex;
  flex-direction: column;
  gap: 16px;
  &__title {
    margin: 0 24px;
    font-weight: 600;
    font-size: 28px;
  }
  &__waitList {
    display: flex;
    justify-content: space-between;
    border: 1px solid #b4b4b466;
    background: #1d1d1f80;
    padding: 12px;
    border-radius: 16px;
    margin-left: 24px;
    margin-right: 24px;
    font-size: 16px;
    font-weight: 500;
    &-about {
      padding: 26px 16px;
      margin: 32px 24px;
    }
  }
  &__item {
    display: flex;
    align-items: center;
    gap: 12px;
  }
  &__infoItem {
    color: #b4b4b4;
    display: flex;
    gap: 8px;
  }
  &__countDollars {
    color: #ffffff;
    font-weight: 600;
    font-size: 18px;
  }
}
</style>
