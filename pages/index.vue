<template>
  <v-container>
    <v-row class="mb-4">
      <v-col cols="12" class="headline text-center">
        Linking to a Specific Tab
      </v-col>
    </v-row>
    <v-row class="mb-4">
      <v-col cols="12" md="6" offset-md="3">
        <v-card>
          <v-tabs v-model="tab" background-color="grey lighten-4">
            <v-tab href="#one">
              One
            </v-tab>
            <v-tab href="#two">
              Two
            </v-tab>
          </v-tabs>

          <v-tabs-items :value="tab">
            <v-tab-item value="one">
              <v-card-text>
                This is ONE!<br>
                1111111111
              </v-card-text>
            </v-tab-item>
            <v-tab-item value="two">
              <v-card-text>
                This is TWO!<br>
                2222222222
              </v-card-text>
            </v-tab-item>
          </v-tabs-items>
        </v-card>
      </v-col>
    </v-row>
    <v-row>
      <v-col cols="12" class="text-center">
        Go to:
        <v-btn to="/?tab=one" class="ml-4">
          Tab One
        </v-btn>
        <v-btn to="/?tab=two" class="ml-4">
          Tab Two
        </v-btn>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  computed: {
    tab: {
      set (tab) {
        this.$router.replace({ query: { ...this.$route.query, tab } })
      },
      get () {
        return this.$route.query.tab
      }
    }
  }
}
</script>
