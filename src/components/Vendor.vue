<template>
  <div class="vendor">
    <img alt="le bg" :src=creds.picture />
    <p>{{ creds.name }}</p>
    <p>{{ creds.phone }}</p>
  </div>
</template>

<script lang="ts">
import { Options, Vue } from 'vue-class-component';

export interface Seller {
  name: string,
  phone: string,
  picture: string,
}

@Options({
  props: {
    creds: Object as () => Seller,
  },
})

export default class Vendor extends Vue {
  creds!: Seller
}
</script>

<style scoped lang="scss">
.vendor {
  display: flex;
  flex-direction: column;
  align-items: center;
  padding-top: 20px;
  height: 300px;
  width: 300px;
  border: 1px solid #000;
  border-radius: 5%;
}

img {
  height: 200px;
  width: 200px;
  clip-path: circle(50% at 50% 50%);
}
</style>
