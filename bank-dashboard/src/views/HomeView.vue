<template>
  <v-app
    id="inspire"
    :style="{ background: $vuetify.theme.themes.dark.background }"
  >
    <SideBar />
    <v-container>
      <NavBar />
      <v-row>
        <v-col cols="12" sm="8">
          <v-row>
            <v-col cols="12" sm="12">
              <OverviewCom />
            </v-col>
            <v-col cols="12" sm="12">
              <MoneyCom />
            </v-col>
            <v-col cols="12" sm="12">
              <PaymentCom />
            </v-col>
          </v-row>
        </v-col>

        <v-col cols="12" sm="4">
          <CardCom />
        </v-col>
      </v-row>
    </v-container>
  </v-app>
</template>

<script>
import CardCom from "@/components/CardCom.vue";
import MoneyCom from "@/components/MoneyCom.vue";
import OverviewCom from "@/components/OverviewCom.vue";
import PaymentCom from "@/components/PaymentCom.vue";
import SideBar from "@/components/SideBar.vue";
import NavBar from "@/components/NavBar.vue";

export default {
  name: "HomeView",
  components: {
    CardCom,
    MoneyCom,
    OverviewCom,
    PaymentCom,
    SideBar,
    NavBar,
  },
};
</script>

<style>
.v-btn.withoutuppercase {
  text-transform: none !important;
}

.v-btn:not(.v-btn--round).v-size--small {
  min-width: 30px !important;
  padding: 0 5px !important;
}
</style>
