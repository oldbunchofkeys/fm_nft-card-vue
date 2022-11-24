<template>
  <div class="card-wrapper">
    <div class="card">
      <div class="nft-img-wrapper">
        <img width="279" class="nft-image" src="../assets/images/image-equilibrium.jpg" alt="image of the nft">
        <img class="icon-view" src="../assets/images/icon-view.svg" alt="eyeball icon">
      </div>
      <a href="#"><h1>{{ heading }}</h1></a>
      <p class="main-copy">{{ body }}</p>
      <div class="details-wrapper">
        <div class="value-wrapper">
          <img src="../assets/images/icon-ethereum.svg" alt="image of the ethereum icon">
          <p class="value-copy">{{ price }} ETH</p>
        </div>
        <div class="time-wrapper">
          <img src="../assets/images/icon-clock.svg" alt="icon of a clock">
          <p class="time-copy">{{ time }} days left</p>
        </div>
      </div>
      <div class="author-wrapper">
        <img class="author-avatar" src="../assets/images/image-avatar.png" alt="profile avatar">
        <p class="author-copy">Creation of <a href=""><span class="author-name">{{ author }}</span></a></p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'NftCard',
  props: ['heading', 'body', 'price', 'time', 'author']
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  @import url('https://fonts.googleapis.com/css2?family=Outfit:wght@300;400;600&family=Overpass:wght@400;700&display=swap');
  
  * {
    font-family: 'Outfit';
  }
  .card-wrapper {
    display: flex;
    justify-content: center;
    align-items: center;
    background-color:#0D192C;
    height: 100vh;
  }
  a {
    text-decoration: none;
  }
  span:hover, h1:hover {
    color: #00FFF8;
  }
  .card {
    width: 327px;
    background: #15263F;
    padding: 24px;
    box-shadow: 0px 25px 50px rgba(0, 0, 0, 0.0952917);
    border-radius: 15px;
  }
  .nft-img-wrapper {
    border-radius: 8px;
    display: flex;
    justify-content: center;
    align-items: center;
    position: relative;
  }
  .nft-img-wrapper:hover {
    background-color: #00FFF8;
    cursor: pointer;
  }
  .nft-image {
    height: auto;
    border-radius: 8px;
    display: block;
    z-index: 1;
  }
  .nft-image:hover {
    z-index: 0;
    opacity: 50%;
  }
  .icon-view {
    position: absolute;
  }
  h1 {
    font-style: normal;
    font-weight: 600;
    font-size: 22px;
    line-height: 28px;
    color: #fff;
    margin-top: 24px;
  }
  .main-copy {
    font-weight: 300;
    font-size: 18px;
    line-height: 26px;
    color: #8BACD9;
    margin-top: 12px;
  }
  .details-wrapper, .value-wrapper, .time-wrapper, .author-wrapper {
    display: flex;
  }
  .details-wrapper {
    justify-content: space-between;
    margin: 1rem 0;
  }
  .value-copy {
    font-weight: 600;
    font-size: 16px;
    line-height: 20px;
    color: #00FFF8;
    padding-left: 6.5px;
  }
  .time-wrapper {
    width: 93px;
  }
  .time-copy {
    font-weight: 400;
    font-size: 15px;
    line-height: 19px;
    color: #8BACD9;
    margin-left: 7.7px;
    min-width: 68px;
  }
  .author-wrapper {
    padding-top: 16px;
    border-top: 1px solid #2E405A;
    align-items: center;
  }
  .author-avatar {
    width: 33px;
    height: 33px;
    border: 1px solid #FFF;
    border-radius: 50%;
  }
  .author-copy {
    font-weight: 400;
    font-size: 15px;
    line-height: 20px;
    color: #8BACD9;
    margin-left: 1rem;
  }
  .author-name {
    color: #fff;
  }

  @media screen and (min-width: 740px) {
    .card {
      width: 350px;
    }
    .details-wrapper {
      margin: 24px 0;
    }
    .main-copy {
      margin-top: 1rem;
    }
    .author-copy {
      font-size: 1rem;
    }

  }
</style>
