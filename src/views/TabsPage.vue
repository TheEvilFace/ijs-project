<template>
  <ion-page>
    <ion-tabs>
      <ion-router-outlet></ion-router-outlet>
      <ion-tab-bar slot="bottom">

        <ion-tab-button color="medium" tab="tab1" href="/tabs/tab1">
          <ion-icon    :src="main" />
          <ion-label>Главная</ion-label>
        </ion-tab-button>

        <ion-tab-button tab="tab2" href="/tabs/tab2">
          <ion-icon :icon="service" />
          <ion-label>Сервисы</ion-label>
        </ion-tab-button>

        <ion-tab-button tab="tab3" href="/tabs/tab3">
          <ion-icon :icon="myProject" />
          <ion-label>Мой проект</ion-label>
        </ion-tab-button>

        <ion-tab-button tab="tab4" href="/tabs/tab4">
          <ion-icon :icon="favorite" />
          <ion-label>Избранное</ion-label>
        </ion-tab-button>

        <ion-tab-button tab="tab5" href="/tabs/tab5">
          <ion-icon :icon="profile" />
          <ion-label>Меню</ion-label>
        </ion-tab-button>
      </ion-tab-bar>
    </ion-tabs>
  </ion-page>
</template>

<script type="ts">
import { defineComponent } from 'vue';
import { IonTabBar, IonTabButton, IonTabs, IonLabel, IonIcon, IonPage, IonRouterOutlet } from '@ionic/vue';

// иконки
import main from '../icons/main.svg';
import favorite from '../icons/favorite.svg';
import myProject from '../icons/myproject.svg';
import profile from '../icons/profile.svg';
import service from '../icons/service.svg';

export default defineComponent({
  name: 'TabsPage',
  components: { IonLabel, IonTabs, IonTabBar, IonTabButton, IonIcon, IonPage, IonRouterOutlet },
  setup() {
    return {
      main,
      favorite,
      myProject,
      profile,
      service
    }
  }
});
</script>

<style scoped>
  ion-tab-button{
      --color: #A9B7C5 ;
  }
</style>