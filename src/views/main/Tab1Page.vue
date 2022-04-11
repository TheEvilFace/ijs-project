<template>
  <ion-page >
    <ion-content :fullscreen="true">
      <ion-header>
        <ion-toolbar class="new-toolbar-color" >
          <section name="head">
            <headerMain/>
          </section>
        </ion-toolbar>

      </ion-header>


      <section name="content" class="borderContent">

        <section name="history">
          <historyComponent />
        </section>

        <section class="paddingLeft" name="region">
          <div >
            <p class="regionText">Московская область</p>
          </div>
        </section>

        <section  name="category" >
          <ion-grid class="categoryClass">
            <ion-row class="categoryWidth">
              <ion-chip>
                <ion-label style="color: #4A687E">все — 250</ion-label>
              </ion-chip>

              <ion-chip outline>
                <ion-label color="medium" >вахверк — 36</ion-label>
              </ion-chip>

              <ion-chip outline>
                <ion-label color="medium">клееный брус — 52</ion-label>
              </ion-chip>

              <ion-chip outline>
                <ion-label color="medium">газобетон — 42</ion-label>
              </ion-chip>
            </ion-row>
          </ion-grid>
        </section>


        <section name="listAD">
          <ion-grid>
            <ion-row>
              <ion-col size="6" v-for="i in 8" :key="i">
                <ad-component name="Tab 1 page" />
              </ion-col>
            </ion-row>
          </ion-grid>
        </section>

      </section>

    </ion-content>
  </ion-page>
</template>

<script lang="ts">
import { defineComponent } from 'vue';
import {IonPage, IonContent} from '@ionic/vue';
import adComponent from '@/components/ad-component.vue'
import historyComponent from '@/components/History-component.vue'
import headerMain from '@/components/headerMain.vue'


export default  defineComponent({
  name: 'Tab1Page',
  components: {  IonContent, IonPage, headerMain, adComponent,historyComponent }
});
</script>

<style scoped>
  .paddingLeft{
    padding-left: 10px ;
  }
  .categoryWidth{
    width: max-content;
  }
  .categoryClass{
    overflow-x: scroll;
  }
  .categoryClass::-webkit-scrollbar {
    display: none;
  }
  ::-webkit-scrollbar {
    display:none !important;
  }
  .regionText{
    width: max-content;
    font-family: 'Mont';
    font-style: normal;
    font-weight: 800;
    font-size: 1.5rem;
    line-height: 23px;
    border-bottom: 1px dashed;
  }
  .borderContent{
    border-radius: 15px 15px 0px 0px;
  }
  .new-toolbar-color{
    --background: linear-gradient(239.67deg, #227164 0.34%, #278878 61.18%);
  }
</style>
