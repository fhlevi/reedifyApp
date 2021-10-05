/*
 * Copyright (c) 2021 PT Telkom Indonesia Tbk
 * 
 * This software is licensed to PT Telkom Indonesia Tbk
 * 
 * All use of the material herein is restricted All rights are reserved
 * You may not use, copy, duplicate, modify, merge, publish, distribute, sublicense the Software without prior written agreement
 */
<template>
    <v-layout wrap class="main-token-section">
        <v-flex xs12 class="token-title">
            <div class="content-title-left">
                <img :src="require('@/assets/img/icons/reedify.png')" height="44" alt="reedify" />
                <h2 class="mt-1">CRP Token</h2>
            </div>
            <p>Solana Program Library (SPL)</p>

            <v-layout wrap class="card-grid">
                <template v-for="(item, index) in itemTokenCard">
                    <v-flex :key="index" xs6 class="px-3 pb-6">
                        <div class="grid-card-item">
                            <div class="card-content-item">
                                <div class="m-auto pt-3 font-600 text-20">
                                    {{ item.title }}
                                </div>
                                <div class="m-auto pa-3 text-13">
                                    {{ item.content }}
                                </div>
                            </div>
                        </div>
                    </v-flex>
                </template>
            </v-layout>
        </v-flex>
    </v-layout>
</template>

<script>
export default {
    name: 'InfoToken',
    data() {
        return {
            itemTokenCard: [
                {
                    title: 'Farm creation',
                    content: '$CRP will be essential for paying the fee to launch farms in USDC pairs.'
                },
                {
                    title: '$CRP Token',
                    content: "Our platform will be fuelled by CRP, it's native token."
                },
                {
                    title: 'Liquidity provision',
                    content: '$CRP will be required for providing liquidity to $CRP-[SPL-Token] pairs and getting additional yield.'
                },
                {
                    title: 'Fee collection',
                    content: 'Liquidity providers of the [CRP]-[USDC] farm will receive, in addition to the farming emissions, 50% of the fees collected.'
                }
            ]
        }
    }
}
</script>