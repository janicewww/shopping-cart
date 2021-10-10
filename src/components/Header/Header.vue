<template>
  <div class="header-container"> {{title}} </div>
</template>

<script>
export default {
    props: {
        title: {
            default: '',
            type: String
        }
    }

}
</script>

<style lang="less" scoped>
.header-container {
    text-size: 12px;
    text-align: center;
    height: 45px;
    width: 100%;
    color: white;
    background: lightseagreen;
}

</style>