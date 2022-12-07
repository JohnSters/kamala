<template>
  <div>
    <v-parallax
      src="/images/HomeHeader.png"
      height="500"
    >
      <v-container fluid>
        <v-row
          align="center"
          justify="center"
          no-gutters
        >
          <v-col cols="12" class="pl-15">
            <div class="pl-8">
              <h1 class="pb-8">Karoo Retreat</h1>
              <p>Kamala House Karoo Retreat is the vision <br /> and dream of Terry de Vries, Known <br /> internationally for her labyrinth work.</p>
            </div>
          </v-col>
        </v-row>
      </v-container>
    </v-parallax>
    <v-card color="#E2EAEC" flat>
      <v-row>
        <v-col cols="12" sm="4">
          <v-parallax src="/images/Be.png">
            <v-card class="ma-auto text-center transparent white--text">
              <p class="display-3">BE</p>
              <v-btn class="blue rounded-0 lighten-2" height="50" dark>View More</v-btn>
            </v-card>
          </v-parallax>
        </v-col>
        <v-col cols="12" sm="4">
          <v-parallax src="/images/Grow.png">
            <v-card class="ma-auto text-center transparent white--text">
              <p class="display-3">GROW</p>
              <v-btn class="blue rounded-0 lighten-2" height="50" dark>View More</v-btn>
            </v-card>
          </v-parallax>
        </v-col>
        <v-col cols="12" sm="4">
          <v-parallax src="/images/Learn.png">
            <v-card class="ma-auto text-center transparent white--text">
              <p class="display-3">LEARN</p>
              <v-btn class="blue rounded-0 lighten-2" height="50" dark>View More</v-btn>
            </v-card>
          </v-parallax>
        </v-col>
      </v-row>
    </v-card>
    <v-card class="pa-3 mt-8" flat>
      <v-row>
        <v-col cols="12" sm="6">
          <v-img src="/images/IntimateRetreats.png" max-height="428px" contain></v-img>
        </v-col>
      </v-row>
    </v-card>
  </div>
</template>

<script>
export default {
  name: 'IndexPage'
}
</script>
