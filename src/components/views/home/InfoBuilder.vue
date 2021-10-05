<template>
    <div class="reedify-builder-secion">
        <div class="container-builder">
            <div class="content-title-left">
                <img :src="require('@/assets/img/icons/reedify.png')" height="44" alt="reedify" />
                <h2 class="mt-1">Made for Solana builders</h2>
            </div>
            <p>Friction-less process</p>

            <v-layout class="card-grid">
                <template v-for="(item, index) in itemBuilderCard">
                    <v-flex :key="index" xs6 class="px-3 pb-6">
                        <div class="grid-card-item">
                            <div class="card-content-item">
                                <div class="m-auto pt-3 font-600 text-20">
                                    {{ item.title }}
                                </div>
                                <div class="m-auto pa-3 text-15">
                                    {{ item.content }}
                                </div>
                            </div>
                        </div>
                    </v-flex>
                </template>
            </v-layout>
        </div>
    </div>
</template>

<script>
export default {
    name: 'InfoBuilder',
    data() {
        return {
            itemBuilderCard: [
                {
                    title: 'Launch',
                    content: 'Open your farms in a few clicks and onboard thousands of farmers tomorrow.'
                },
                {
                    title: 'Stabilize',
                    content: "Stabilize your SPL token and offer a good farming experience."
                },
                {
                    title: 'Bring value',
                    content: 'Generate rewards to your holders through different farming features.'
                }
            ]
        }
    }
}
</script>

<style>

</style>