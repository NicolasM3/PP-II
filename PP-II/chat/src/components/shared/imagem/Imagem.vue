<template>
   <img :src="'imagens/' + ra + '.jpg'" />
</template>

<script>
export default {
  props: ["ra"],
  data() { 
      return { 
          visivel: true 
        }
    }
};
</script>