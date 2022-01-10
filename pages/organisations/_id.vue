<template>
  <div>
    <div style="display: grid" class="content">
      <v-img
        class="content"
        src="https://lvdneng.rosselcdn.net/sites/default/files/dpistyles_v2/ena_16_9_extra_big/2020/09/24/node_869694/49073910/public/2020/09/24/B9724678734Z.1_20200924102506_000%2BG67GNLI5B.2-0.jpg?itok=du5lymEb1600935913"
        aspect-ratio="2"
        max-height="27rem"
      />
      <div class="overlay">
        <div>
          <div class="d-flex justify-center">
            <div class="ml-5 white--text">
              <div class="font-weight-bold text-h5">
                Association d'airsoft de Melun
              </div>
              <div class="font-weight-medium">
                89 Rue des anges 77490, Melun
              </div>
            </div>
          </div>

          <v-app-bar
            dense
            elevation="4"
            color="#efeae4"
          >
            <div
              style="margin-left: 10rem;"
            >
              <v-card>
                <v-img
                  max-height="20rem"
                  style="border: 1px solid black;
              box-shadow: rgb(0 0 0 / 24%) 0 3px 8px;"
                  max-width="13rem"
                  src="https://ae01.alicdn.com/kf/HTB1LACjKVXXXXcHXXXXq6xXFXXXw/202735408/HTB1LACjKVXXXXcHXXXXq6xXFXXXw.jpg?size=43867&height=800&width=800&hash=5cbf71b36d29fa40b943805cb345e35b"
                />
              </v-card>
            </div>
            <div class="ml-5">
              <span class="mr-10">
                Profile
              </span>
              <span class="mr-10">
                Parties
              </span>
              <span class="mr-10">
                La Team
              </span>
              <span class="mr-10">
                Rejoindre la Team
              </span>
            </div>
          </v-app-bar>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Id'
}
</script>

<style scoped>
:deep(.v-image__image) {
  box-shadow: inset 0 0 0 1000px rgb(0 0 0 / 32%) !important;
  background: red !important;
}

.content, .overlay {
  grid-area: 1 / 1;
  z-index: 999;
  align-items: end;
}
</style>
