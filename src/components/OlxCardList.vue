<template>
    
        <div class="list-container">
                <olx-card
                    v-for="item in olxCardListData"
                    :key="item.id"
                    :img-src="item.imgSrc"
                    :available="item.available"
                    :title="item.title"
                    :city="item.city"
                    :price="item.price"
                    
                />
            </div>
    
</template>

<script >
import OlxCard from './OlxCard.vue'
export default {
    name: 'OlxCardList',
    components: {
    OlxCard,
  },

  props: {
    olxCardListData: {
      type: Array,
      default: () => [],
    },
  },
}
</script>

<style scoped>
.list-container{
  display: flex;
  justify-content: center;
}
</style>
