<template>
  <ion-page>
    <ion-header class="ion-no-border">
      <ion-toolbar>
        <ion-buttons slot="start">
          <ion-button color="primary">
            <ion-icon slot="icon-only" :icon="arrowBack"></ion-icon>
          </ion-button>
        </ion-buttons>
        <ion-buttons slot="end">
          <router-link to="/signup">
            <ion-button color="primary">Sign Up</ion-button>
          </router-link>
        </ion-buttons>

      </ion-toolbar>
    </ion-header>

    <ion-content>
      <div id="header">
        <img src="../assets/logo.jpeg" alt="">
      </div>

      <form action="" id="form">
        <h1 class="text-center">Login</h1>
        <Input placeholder="Email"></Input>
        <Input placeholder="password" type="password"></Input>
        <ion-button expand="block" shape="round">Login</ion-button>
      </form>
    </ion-content>
  </ion-page>
</template>

<script>
import {IonButton, IonButtons, IonHeader, IonIcon, IonPage, IonToolbar} from "@ionic/vue";
import {arrowBack, personCircle, search} from 'ionicons/icons';
import Input from "@/components/Auth/Input";

export default {
  name: "Login Page",
  components: {
    Input,
    IonHeader,
    IonButtons,
    IonButton,
    IonIcon,
    IonToolbar,
    IonPage,
  },
  setup() {
    const clickedStar = () => {
      console.log('Star clicked!');
    }
    return { personCircle, search, arrowBack, clickedStar };
  }
}
</script>

<style scoped>
  ion-toolbar{
    --background: #f7f7f7;
  }

  ion-toolbar ion-button{
    text-transform: initial;
    font-size: 17px;
  }

  ion-content{
    --background: #f7f7f7;
  }

  #header{
    display: flex;
    flex-direction: column;
    align-items: center;
  }

  #header h1 {
    font-weight: 700;
    font-size: 26px;
    color: #010100;
    margin-bottom: 15%;
  }

  img{
    width: 125px;
    height: 125px;
    border-radius: 50%;
    border: 10px solid #ffffff;
  }

  #form {
    margin-top: 15%;
    padding-left: 30px;
    padding-right: 30px;
  }

  #form ion-button{
    margin-top: 35px;
    height: 48px;
    font-size: 18px;
    text-transform: initial;
    border-radius: 50px;
    box-shadow: 1px 8px 8px 0px rgba(0, 0, 0, 0.05);
    --box-shadow: none;
  }
</style>