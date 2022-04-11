<template>
  <div class="textColorWhite">
    <h6 class="headerText headerOffset">Добро пожаловать <br>в ИЖС Маркет!</h6>
    <ion-grid>
      <ion-row>
        <ion-col>
          <div class="blockOne">
            <p class="text-bottom">
              Выберите проект дома, а разные застройщики предложат цены
            </p>
          </div>
        </ion-col>
        <ion-col>
          <div class="blockTwo">
            <p class="text-bottom">
              Стройте с <span style="font-weight: bold">ИЖС Genius</span> без убытков и потери личного времени
            </p>
            <ion-icon class="questIcon" :icon="quest" />
          </div>
        </ion-col>
      </ion-row>
    </ion-grid>


  </div>

</template>

<script>
import quest from '@/icons/Question.svg'
import {IonIcon} from "@ionic/vue";

export default {
  name: "headerMain",
  components: {IonIcon},
  setup() {
    return{
      quest
    }
  }
}
</script>

<style scoped>
.headerOffset {
  padding-top: 50px;
  padding-left: 10px;
}

.textColorWhite {
  color: white;
}

.headerText {
  font-family: 'Mont';
  font-style: normal;
  font-weight: 800;
  font-size: 24px;
  line-height: 31px;
  margin: 0;
}

.blockOne {
  background: linear-gradient(135.55deg, #A7A6CB -5.43%, #8989BA 107.62%);
  border-radius: 10px;
  width: 175px;
  height: 104px;
  position: relative;
}

.blockTwo {
  background: linear-gradient(134.43deg, #C79081 26.26%, #DFA579 105.21%);
  border-radius: 10px;
  width: 175px;
  height: 104px;
  position: relative;
}

.text-bottom {
  position: absolute;
  margin: 0;
  bottom: 13px;
  left: 10px;
  font-family: 'Mont';
  font-style: normal;
  font-weight: 500;
  font-size: 0.8rem;
  line-height: 13px;
}
.questIcon{
  position: absolute;
  right: 10px;
  top: 10px;
}
</style>