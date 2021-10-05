<template>
    <div>
        <div class="banner-vector">
            <img :src="require('Assets/img/banner/reedify_banner.png')" alt="">
        </div>
        <div class="section-banner">
            <div class="container-banner">
                <div class="text-title-section">The first permissionless yield</div> 
                <div class="text-title-section">farming protocol on Solana.</div>
                <div class="text-sub-title">Bringing Yield Farming to the next level.</div>
                <div class="main-banner button">
                    <v-btn class="btn-LA">
                        Launch App
                    </v-btn>
                    <a href="https://docs.reedify.finance/" target="_blank">
                        <v-btn class="btn-RM">
                            Read More
                        </v-btn>
                    </a>
                </div>
                <div class="float-left">
                    <social-media-item></social-media-item>
                </div>
                <div class="banner--powered">
                    <p>Powered by</p>
                    <img :src="require('Assets/img/solana.png')" alt="">
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'Banner',
    components: {
        'social-media-item': () => import('Components/template/SocialMedia.vue')
    }
}
</script>