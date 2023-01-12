<script>
export default {
    props:{
        comic: Object,
    }
}
</script>

<template lang="">
    <div class="card">
        <div class="card-image">
            <img :src="comic.thumb" alt="">
        </div>
        <div class="card-name">
            {{ comic.series }}
        </div>
    </div>
</template>

<style lang="scss">
    .card{
        width: calc(100% / 6 - 40px);
        text-align: center;
    }
</style>