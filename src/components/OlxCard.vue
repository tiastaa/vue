<template>
  <div class="card-box parrent">
    
    <div class="card-img ">
      <img :src="imgSrc" />
    </div>
    <div class="card-delivery-img child">
      <button   v-show="available">
        <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRIdPygjewcn5hP7hZn8VjAWCIygVCnKEakuw&usqp=CAU" alt="">
      </button>
    </div>
    <div class="card-title child">
      {{ title }}
    </div>
    <div class="card-city">
      {{ city }}
    </div>
    <div class="card-price child">
      {{ price }} грн
    </div>
    <div class="card-like-button child">
      <button >
        <img src="https://www.seekpng.com/png/small/869-8698119_grey-heart-clip-art-at-clker-gray-heart.png" alt="">
      </button>
    </div>
  </div>
</template>

<script>
export default {
  name: "OlxCard",
  props: {
    imgSrc: {
      type: String,
      default:
        "https://res.cloudinary.com/woodland/image/upload/ar_1,c_crop/f_auto,h_800,q_auto,w_800/d_ni.png/v1/craftcuts_media/media/catalog/product/d/i/dimensional_animals_cats_cat_paw.jpg",
    }, 
    available: {
      type: Boolean,
      default: false,
    },
    title: {
      type: String,
      default: ". . .",
    },
    city: {
      type: String,
      default: ". . ."
    },
    price: {
      type: Number,
      default: 0,
    },
   
  },
};
</script>

<style scoped>
.card-box {
  position: relative;
  border: 0px solid rgb(101, 144, 119);
  border-radius: 3px;
  margin: 9px;
  padding: 10px;
  background-color: white;
  height: 230px;
  width: 220px;
}


.card-delivery-img button{
  position: absolute;
  top: 125px;
  right: 20px;
  border: 0px solid bisque;
  border-radius:90px ;
  padding: 5px;
  background-color: white;
  width: 25px;
  height: 25px;

}
.card-delivery-img img{
width: 15px;
height: 15px;
  

}
.card-like-button button{
    width: 20px;
    height: 20px;
    margin-bottom: 10px;
    padding: 3px;
    cursor: pointer;
    background-color: rgb(255, 255, 255);
    border: 0px solid rgb(255, 255, 255);

    position: absolute;
    bottom: 0px;
    right: 10px;
    
}

.card-like-button img{
    width: 100%;

}

.card-img img {
  width: 220px;
  height: 150px;
  
}

.card-city{
  color: rgb(96, 96, 96);
  font-size: x-small;
  position: absolute;
  bottom: 35px;
}
.card-price{
  position: absolute;
  bottom: 10px;
}

</style>
