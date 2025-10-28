<template>
    <v-container fluid>
      <v-row >
        <v-col
          v-for="car in cars"
          :key="car.model"
          cols="3"
        >
        <Car :model="car.model" :photo="car.src" :price="car.price"/>
                  </v-col>
      </v-row>
    </v-container>
</template>
<script setup>
  const cars = [
    { model: 'Corola', src: 'https://tmna.aemassets.toyota.com/is/image/toyota/toyota/jellies/max/2026/corolla/xse/1866/1k3/36/5.png?fmt=png-alpha&wid=930&hei=328&qlt=90', price: 10.00},
    { model: 'G-Wagon', src: 'https://p7.hiclipart.com/preview/263/320/1000/2018-mercedes-benz-g-class-car-sport-utility-vehicle-mercedes-benz-g-wagon.jpg', price: 15.00},
    { model: 'Supra ', src: 'https://di-sitebuilder-assets.dealerinspire.com/Toyota/models/2024/gr-supra/3.0_grsupra.png', price: 20.00},
    { model: 'G-Wagon', src: 'https://p7.hiclipart.com/preview/263/320/1000/2018-mercedes-benz-g-class-car-sport-utility-vehicle-mercedes-benz-g-wagon.jpg', price: 30.00},
    { model: 'Corola', src: 'https://tmna.aemassets.toyota.com/is/image/toyota/toyota/jellies/max/2026/corolla/xse/1866/1k3/36/5.png?fmt=png-alpha&wid=930&hei=328&qlt=90', price: 50.00},
    { model: 'G-Wagon', src: 'https://p7.hiclipart.com/preview/263/320/1000/2018-mercedes-benz-g-class-car-sport-utility-vehicle-mercedes-benz-g-wagon.jpg', price: 60.00},
    { model: 'Supra ', src: 'https://di-sitebuilder-assets.dealerinspire.com/Toyota/models/2024/gr-supra/3.0_grsupra.png', price: 80.00},
    { model: 'Corola', src: 'https://tmna.aemassets.toyota.com/is/image/toyota/toyota/jellies/max/2026/corolla/xse/1866/1k3/36/5.png?fmt=png-alpha&wid=930&hei=328&qlt=90', price: 100.00},
    { model: 'G-Wagon', src: 'https://p7.hiclipart.com/preview/263/320/1000/2018-mercedes-benz-g-class-car-sport-utility-vehicle-mercedes-benz-g-wagon.jpg', price: 40.00},
    { model: 'Supra ', src: 'https://di-sitebuilder-assets.dealerinspire.com/Toyota/models/2024/gr-supra/3.0_grsupra.png', price: 30.00},
  ]
</script>
