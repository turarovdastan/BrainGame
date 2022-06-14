<template>
  <div class="profile">
    <div class="profile-avatar">
      <img src="../assets/img/avatar.jpg" alt="">
      <div @click="info = !info" class="profile-info">
        <div class="profile-username">@dastan</div>
        <svg :class="[info && 'rotate']" width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
        <path d="M7 10L12 15L17 10H7Z" fill="#5F6368"/>
        </svg>
      </div>
      <transition name="fade">
        <div v-if="info" class="profile-email">
          turaaa555@gmail.com
        </div>
      </transition>
    </div>
    <div class="profile-balance">
      <div>
        <img src="../assets/img/coin.svg" alt=""/>
        <div>Balance</div>
      </div>
      <div>
        70 сом
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data: () => ({
    info: false
  })
}
</script>

<style lang="scss" scoped>
.profile{
  padding: 40px 20px;
  display: flex;
  flex-direction: column;
  gap: 20px;
  &-avatar{
    display: flex;
    align-items: center;
    justify-content: center;
    flex-direction: column;
    gap: 20px;
    padding-bottom: 30px;
    border-bottom: 1px solid #ccc;
    .rotate{
      transform: rotate(180deg);
    }
    svg{
      transition: all 1s ease-in;
    }
    img{
      width: 120px;
      height: 120px;
      border-radius: 50%;
      padding: 6px;
      box-shadow: 1px 1px 18px 3px #00000060
    }
  }
  &-username{
    font-family: 'Roboto';
  }
  &-email{
    width: 100%;
    font-family: 'Roboto';
  }
  &-balance{
    display: flex;
    align-items: center;
    justify-content: space-between;
    & > div{
      font-family: 'Montserrat';
      display: flex;
      gap: 10px;
      align-items: center;
    }
  }
  &-info{
    width: 100%;
    display: flex;
    align-items: center;
    justify-content: space-between;
  }
}

.fade-enter-active,
.fade-leave-active {
  transition: opacity 0.5s ease;
}

.fade-enter-from,
.fade-leave-to {
  opacity: 0;
}
</style>