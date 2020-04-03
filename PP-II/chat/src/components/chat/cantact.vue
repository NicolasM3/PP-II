<template>
    <div class="wrap">
        <span class="status"></span>
        <img src="image" alt="" />
        <div class="meta">
        <p class="name">{{name}}</p>
        </div>
    </div>
</template>

<script>
export default {
    props: ["status", "name", "image"],
    data() { 
        return { 
            visivel: true 
        }
    }
};
</script>