<template>
  <v-row>
    <v-col cols="12" sm="6">
      <v-toolbar class="mt-n5" flat color="transparent">
        <v-toolbar-title class="white--text">All Payment</v-toolbar-title>
        <v-chip class="ml-2" color="green" text-color="white">2</v-chip>
      </v-toolbar>
      <v-row>
        <v-col cols="12" sm="6">
          <v-card class="rounded-lg mx-2 pa-2 mt-n3" flat color="#242426">
            <span class="caption grey--text mt-n6">Credit Card</span><br />
            <h6 class="white--text mt-4">Balance</h6>
            <h4 class="white--text">$767.50</h4>
            <v-card-text class="pt-0">
              <v-icon class="mr-2" color="grey">fab fa-cc-mastercard</v-icon>
              <span class="text-caption grey--text font-weight-light"
                >**6774</span
              >
            </v-card-text>
          </v-card>
        </v-col>
        <v-col cols="12" sm="6">
          <v-card class="rounded-lg mx-2 pa-2 mt-n3" color="#242426" flat>
            <span class="caption grey--text mt-n6">Credit Card</span><br />
            <h6 class="white--text mt-4">Balance</h6>
            <h4 class="white--text">$328.85</h4>
            <v-card-text class="pt-0">
              <v-icon class="mr-2" color="grey">fab fa-cc-visa</v-icon>
              <span class="text-caption grey--text font-weight-light"
                >**6774</span
              >
            </v-card-text>
          </v-card>
        </v-col>
      </v-row>
    </v-col>
    <v-col cols="12" sm="6">
      <v-toolbar class="mt-n5" flat color="transparent">
        <v-toolbar-title class="white--text">All Transactions</v-toolbar-title>
        <v-chip class="ml-2" color="green" text-color="white">12</v-chip>
      </v-toolbar>
      <v-card class="rounded-lg mr-2 mt-n3" color="#242426" flat>
        <h5 class="white--text ml-2 pt-2">Recent Experience</h5>
        <v-list class="mt-n2" color="transparent" dense>
          <v-list-item
            v-for="experience in experiences"
            :key="experience.title"
          >
            <v-list-item-avatar>
              <v-img :src="experience.img" />
            </v-list-item-avatar>

            <v-list-item-content>
              <v-list-item-title
                class="white--text"
                v-text="experience.title"
              ></v-list-item-title>
              <v-list-item-subtitle
                class="grey--text"
                v-text="experience.subtitle"
              ></v-list-item-subtitle>
            </v-list-item-content>
            <v-list-item-action>
              <h5 class="white--text">{{ experience.price }}</h5>
            </v-list-item-action>
          </v-list-item>
        </v-list>
      </v-card>
    </v-col>
  </v-row>
</template>

<script>
export default {
  data: () => ({
    experiences: [
      {
        img: "spotify.png",
        subtitle: "Premium 1 Month Service",
        title: "Spotify",
        price: "-$52.42",
      },
      {
        img: "netflix.png",
        subtitle: "Premium 1 Month Service",
        title: "Netflix",
        price: "-$106.42",
      },
    ],
  }),
};
</script>

<style></style>
