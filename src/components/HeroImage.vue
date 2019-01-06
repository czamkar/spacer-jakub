<template>
<div class="heroImage" />
</template>

<script>
export default{
  name: 'HeroImage',
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss" scoped>
.heroImage{    
  position: fixed;
  width: 100%;
  height: 100vh;
  z-index: -1;
  background-image: url('../assets/heroimage.jpg');
  background-repeat:  no-repeat;
  background-size: cover;
  background-position: 30% 40%;
}
.heroImage::after{
    content: '';
    background: rgba(0,0,0,.1);
    position: absolute;
    top:0;
    left: 0;
    z-index: 1;
    width: 100%;
    height: 100vh;
} 
</style>
