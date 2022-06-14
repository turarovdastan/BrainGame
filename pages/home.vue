<template>
  <div class="home">
    <div class="home-games">
      <div class="home-chees home-card">
        <div class="home-chees-title">Шахмат</div>
        <button class="home-chees-button">Play</button>
      </div>
      <div class="home-games-cnt">
        <div class="home-math home-card">
          <div class="home-math-title">Математика</div>
          <button class="home-math-button">Play</button>
        </div>
        <div class="home-flappy-bird home-card">
          <div class="home-flappy-title">Flappy Bird</div>
          <button class="home-flappy-button">Play</button>
        </div>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.home{
  width: 100%;
  padding: 2%;
  &-games{
    display: grid;
    grid-template-columns: 1fr 1fr;
    grid-gap: 10px;
    height: 40vh;
  }
  &-card{
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    div{
      padding: 20px;
      font-family: 'Montserrat';
      font-weight: 700;
      font-size: 16px;
      line-height: 16px;
      text-transform: uppercase;
      color: #fff;
      background: #00000050;
      border-radius: 10px 10px 0 0;
    }
    button{
      box-shadow: 0 2px 15px #000000;
      margin: 20px;
      background: #649fff;
      height: 45px;
      border: none;
      outline: none;
      border-radius: 4px;
      color: #fff;
      font-family: "Gamja Flower";
      font-size: 20px;
      transition: all .5s ease;
    }
    button:active{
      transform: scale(1.1);
    }
  }
  &-games-cnt{
    display: grid;
    grid-template-columns: 1fr;
    grid-gap: 10px;
    height: 100%;
  }
  &-chees{
    width: 100%;
    border-radius: 10px;
    background: url(../assets/img/chees.jpg);
    background-size: cover;
    background-repeat: no-repeat;
  }
  &-math{
    background: url(../assets/img/math.jpg);
    background-size: cover;
    background-repeat: no-repeat;
    background-position: center center;
    width: 100%;
    border-radius: 10px;
  }
  &-flappy-bird{
    background: url(../assets/img/flappy-bird.jpg);
    background-size: cover;
    background-repeat: no-repeat;
    background-position: center center;
    width: 100%;
    border-radius: 10px;
  }
}
</style>