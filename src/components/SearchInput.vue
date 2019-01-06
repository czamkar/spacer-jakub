<template>

  <input name="search" id="search" :class="{dark}" :value="value" @input="handleChange"/>
 
</template>

<script>
export default{
  name: 'SearchInput',
  props:{
    value:{
      type: String,
      required: true,
    },
    dark:{
      type: Boolean,
      default: false,
    },
  },
  methods:{
    handleChange(e){
      this.$emit('input', e.target.value);
    }
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss" scoped>

  input{
    color: #ffffff;
    margin: 30px 0 0 0 ;
    text-align: center;
    font-size:  20px;
    height: 30px;
    font-weight: 300;
    border: 0;
    background: none;
    border-bottom: 1px solid #ffffff;
    transition: box-shadow .3s ease-out;

      @media(min-width: 1024px){
    font-weight:400;
  }
  }
  input:focus{
    outline: none;
    box-shadow: 0 10px 20px -8px rgba(255,255,255, .5);
  }
  .dark{
    color: #1e3d4a;
    border-bottom-color: #1e3d4a;
  }
  .dark:focus{
    box-shadow: 0 10px 20px -8px rgba(#1e3d4a,.5);
  }

</style>
