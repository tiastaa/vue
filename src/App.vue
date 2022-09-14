<template>
  <div>
    <olx-card-list :olx-card-list-data="listData" />
  </div>
</template>

<script>
import OlxCardList from "@/components/OlxCardList.vue";

export default {
  name: "App",

  components: {
    OlxCardList,
  },

  data() {
    return {
      listData: [
        {
          id: 1,
          imgSrc: "https://ireland.apollo.olxcdn.com/v1/files/2pksj2jufax73-UA/image;s=1156x868", 
          available: true,
          title: "Термокомбінзон для дівчинки",
          city: "Межова",
          price: 500,
         
        },
        {
          id: 2,
          imgSrc: "https://ireland.apollo.olxcdn.com/v1/files/x457pxcgvmz92-UA/image;s=1000x750", 
          available: false,
          title: "Кузов Бочина Четверть ",
          city: "Рівне",
          price: 150 ,
        },
        {
          id: 3,
          imgSrc: "https://ireland.apollo.olxcdn.com/v1/files/gxkgy9w5w6zl-UA/image;s=1600x1200", 
          available: true,
          title: "Спортивне харчування",
          city: "Київ, Шевченківський",
          price: 300,
        },

      ],
    };
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
