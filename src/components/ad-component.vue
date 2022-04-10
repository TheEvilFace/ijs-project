<template>
  <div class="adBoxStyle border-rounded" >
    <img class="border-rounded-img" src="../../resources/dom.jpg" style="width: 100%" />
    <ion-icon class="dotsClass" :src="dots" />
    <div class="text-block" >
      <ion-icon class="badge-M" :src="M" />

      <p class="titleText">Название проекта</p>
      <p class="descriptionText " >180 м2 | 6-8,9 млн ₽</p>
    </div>

  </div>
</template>

<script>
import {IonIcon} from '@ionic/vue';
import dots from '@/icons/dots.svg';
import M from '@/icons/badgeM.svg';


export default {
  name: "ad-component",
  components: { IonIcon },
  setup(){
    return{
      dots,
      M
    }
  }

}
</script>

<style scoped>
  .adBoxStyle {
    background: #FFFFFF;
    box-shadow: 4px 4px 10px #F0EFF1;
    padding: 0 0 10px 0;
    border-radius: 10px;
  }
  .border-rounded-img{
    border-radius: 10px 10px 0 0;
  }
  .dotsClass{
    position: absolute;
    right: 3%;
    top: 5%;
    width: 15%;
    height: 15%;
  }
  .marginY{
    margin: 10px 0;
  }

  .titleText{
    font-family: 'Mont';
    font-style: normal;
    margin-top: 4px;
    margin-bottom: 3px;
    font-weight: 600;
    font-size: 12px;
    line-height: 15px;
  }
  .descriptionText{
    font-family: 'Mont';
    font-style: normal;
    font-size: 12px;
    font-weight: 400;

    margin-top: 0;
    margin-bottom: 3px;
    line-height: 15px;
  }
  .badge-M{
    right: 3px;
    top: -15px;
    width: 56px;
    z-index: 9;
    position: absolute;
  }
  .text-block{
    position: relative;
    padding: 0 10px;
  }
</style>