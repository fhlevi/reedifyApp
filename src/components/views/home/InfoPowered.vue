<template>
    <div class="large-section">
        <div class="large-secion-container">
            <div class="large-section-title">
                <img :src="require('@/assets/img/icons/powered.png')" alt="powered by">
                <span>Powered by</span>
            </div>
            <div class="reedify-grid-partenaires">
                <template v-for="(item, index) in imageList">
                    <div :key="index" class="reedify-item-grid">
                        <img :src="require(`@/assets/img/icons/${item.name}.png`)" :alt="item.img">
                    </div>
                </template>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'InfoPowered',
    data() {
        return {
            imageList: [
                {name: 'solana'}
            ]
        }
    }
}
</script>