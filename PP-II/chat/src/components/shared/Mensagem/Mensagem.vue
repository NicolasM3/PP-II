<template>
    <input id = "message" type = "text" :src = "''" + message>
</template>

<script>
export default 
{
  props: ["message"]
};
</script>