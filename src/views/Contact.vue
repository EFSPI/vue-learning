<template>
  <div class="contact">
    <h1>Contact</h1>
    <p>voici les meilleurs vendeurs de l'année:</p>
    <ul>
      <li v-for="seller in sellers" :key=seller.name>
        <Vendor :creds=seller />
      </li>
    </ul>
  </div>
</template>

<script lang="ts">
import { Options, Vue } from 'vue-class-component';
import Vendor from '@/components/Vendor.vue';

@Options({
  components: {
    Vendor,
  },
})

export default class Contact extends Vue {
  public sellers = [
    {
      name: 'Jéméry',
      phone: '07 83 31 43 89',
      picture: 'https://www.shareicon.net/data/2016/05/24/770124_man_512x512.png',
    },
    {
      name: 'Turbo',
      phone: '514 914 5169',
      picture: 'https://www.ascensiongamedev.com/uploads/monthly_2017_04/self_portrait.thumb.png.300bff792217d8b8c72fa9bab783abf2.png',
    },
    {
      name: 'Cuite',
      phone: '69 69 69 69',
      picture: 'https://the7thcontinent.seriouspoulp.com/images/users/805f6c609970c565ec08652318325bc3.png',
    },
  ];
}
</script>

<style scoped lang="scss">
ul {
  list-style-type: none;
  padding: 0;
}

li {
  display: inline-block;
  margin: 0 10px;
}

</style>
