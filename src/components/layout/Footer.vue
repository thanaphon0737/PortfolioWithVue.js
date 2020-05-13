<template>
  <div id="footer">
      <span class="footer">{{title}}</span>
  </div>
</template>

<script>
export default {
    name: "Footer",
    props:[
        "title",
    ]
}
</script>

<style scoped>
.footer{
    font-size: 12px;
    color: gray;
}

</style>