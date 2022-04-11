<template>
  <div>
    <ion-grid class="historyClass">
      <ion-row class="historyWidth">
        <ion-col>
          <div class="borderHistory paddingHistory">
            <div class="container ">
              <img class="imgClass" src="../../resources/history1.png" height="95" width="95"/>
              <p class="text-center-bottom styledText">Экспертиза работ</p>
            </div>
          </div>
        </ion-col>

        <ion-col>
          <div class="borderHistory paddingHistory">
            <div class="container">
              <img class="imgClass" src="../../resources/history2.png" height="95" width="95"/>
              <p class="text-center-bottom styledText">Дом BLYSKÄR</p>
            </div>
          </div>
        </ion-col>

        <ion-col>
          <div >
            <div class="container">
              <img class="imgClass" src="../../resources/history3.png"/>
              <p class="text-center-bottom styledText">Нас не просили, но мы сделали</p>
            </div>
          </div >

        </ion-col>

        <ion-col>
          <div>
            <div class="container">
              <img class="imgClass " src="../../resources/history4.png"/>
              <p class="text-center-bottom styledText">Инстаграмная лестница</p>
            </div>
          </div>

        </ion-col>


      </ion-row>
    </ion-grid>
  </div>
</template>

<script>
export default {
  name: "History-component"
}
</script>

<style scoped>
.historyWidth {
  width: max-content;
}

.historyClass {
  overflow-x: scroll;
}

.historyClass::-webkit-scrollbar {
  display: none;
}

.container {
  position: relative;
  text-align: center;
  color: white;
  height: 95px;
  width: 95px;
}
.imgClass{
  border-radius: 12px;
}
.borderHistory{
  position:relative;
}
.borderHistory::before {
  content:"";
  position:absolute;
  top:-1px;
  left:-1px;
  right:-1px;
  bottom:-1px;
  border-radius:12px;
  padding:1.5px;
  background:linear-gradient(135.55deg, #A7A6CB -5.43%, #8989BA 107.62%);
  -webkit-mask:
      linear-gradient(#fff 0 0) content-box,
      linear-gradient(#fff 0 0);
  -webkit-mask-composite: xor;
  mask-composite: exclude;
}



.text-center-bottom {
  position: absolute;
  bottom: 10%;
  left: 7.5%;
}

.styledText {
  text-align: left;
  font-family: 'Mont';
  font-style: normal;
  font-weight: 500;
  font-size: 0.65rem;
  line-height: 115%;
  margin: 0;
  letter-spacing: 0.05rem
}
.paddingHistory{
  padding: 2px;
}
</style>