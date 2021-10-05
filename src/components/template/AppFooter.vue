<template>
    <div class="main-footer">
        <div class="footer-line"></div>
        <div class="footer-content">
            <div class="footer-logo">
                <img :src="require('Assets/img/icons/reedify.png')" alt="logo footer" />
                <span class="footer-info text-21">ReedifyFinance</span>
            </div>
            <div class="footer-copyright text-13">
                <span>Decentralized 2021</span>
            </div>
            <div class="footer-social-media">
                <social-media-item></social-media-item>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'AppFooter',
    components: {
        'social-media-item': () => import('@/components/template/SocialMedia.vue')
    }
}
</script>