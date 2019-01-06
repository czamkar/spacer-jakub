<template>
  <div :style="style" class="item" />
</template>

<script>
export default{
  name: 'Item',
  props: {
 item:{
    type: Object,
    required: true,
  },
  },
 
  data(){
    return{
      photo: this.item.links[0].href,
      title: this.item.data[0].title,

    };
  },
  computed:{
          style() {
        return `backgroundImage: url("${this.photo}")`;
      },
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss" scoped>
.item{
  width: 40vw;
  height: 250px;
  background-size: cover;
  background-repeat: none;
  background-position: 50%;
    @media(min-width: 768px){
     width: 25vw;
  }
}
</style>
