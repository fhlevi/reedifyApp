<template>
    <div class="section-info-generator">
        <template v-for="(item, index) in listGenerator">
            <div 
                :key="index" 
                :class="{
                    'container-section': checkPosition(item.position), 
                    'container-generator': !checkPosition(item.position)
                }">
                    <div :class="{
                        'content-title-left': checkPosition(item.position),
                        'content-title-right': !checkPosition(item.position)
                    }">
                        <img :src="require(`@/assets/img/icons/${item.image}`)" height="44" alt="logo generator" />
                        <h2 class="mt-1">{{ item.title }}</h2>
                    </div>
                    <p>{{ item.content }}</p>
            </div>
        </template>
    </div>
</template>

<script>
export default {
    data() {
        return {
            listGenerator: [
                {
                    image: 'infinity.png',
                    title: 'Yield Farm Generator',
                    position: 'left',
                    content: 'SPL projects will be able to connect their liquidity to the platform, set the total supply that will be allocated to farming, decide the weekly emission schedule, and launch their yield farm in a few clicks'
                },
                {
                    image: 'sun.png',
                    title: 'A place conceived, designed, and developed for farmers',
                    position: 'right',
                    content: "CropperFinance aims to provide best yields in the ecosystem. Made by farmers, for farmers."
                }
            ]
        }
    },
    methods: {
        checkPosition(position) {
            if(position === 'left') {
                return true
            }

            return false
        }
    }
}
</script>

<style>

</style>