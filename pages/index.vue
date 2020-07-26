<template>
  <v-container>
    <v-row>
      <v-col cols="12" class="headline text-center mb-4">
        Linking to a Specific Tab
      </v-col>
    </v-row>
    <v-row>
      <v-col cols="12" md="6" offset-md="3">
        <v-card>
          <v-tabs v-model="tab" background-color="grey lighten-4">
            <v-tab>
              One
            </v-tab>
            <v-tab>
              Two
            </v-tab>
            <v-tab-item>
              <v-card-text>
                This is ONE!<br>
                1111111111
              </v-card-text>
            </v-tab-item>
            <v-tab-item>
              <v-card-text>
                This is TWO!<br>
                2222222222
              </v-card-text>
            </v-tab-item>
          </v-tabs>
        </v-card>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  data: () => ({
    tab: null
  })
}
</script>
