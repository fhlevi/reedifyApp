<template>
    <div class="large-section">
        <div class="large-secion-container">
            <div class="large-section-title">
                <img :src="require('@/assets/img/icons/profile.png')" alt="profile team">
                <span>The Team</span>
            </div>
            <div class="grid-storie">
                <v-layout>
                    <v-flex xs11>
                        <v-expansion-panels inset>
                            <v-expansion-panel
                                v-for="(item,i) in listTeam"
                                :key="i"
                            >
                                <v-expansion-panel-header>{{ item.title }}</v-expansion-panel-header>
                                <v-expansion-panel-content>
                                    {{ item.content }}
                                </v-expansion-panel-content>
                            </v-expansion-panel>
                        </v-expansion-panels>
                    </v-flex>
                </v-layout>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'InfoTeam',
    data() {
        return {
            listTeam: [
                {
                    image: '',
                    sosmed: [
                        { telegram: '' },
                        { twiiter: '' }
                    ],
                    title: 'Lorem',
                    content: 'Open your farms in a few clicks and onboard thousands of farmers tomorrow.'
                },
                {
                    image: '',
                    sosmed: [
                        { telegram: '' },
                        { twiiter: '' }
                    ],
                    title: 'Lorem',
                    content: 'Open your farms in a few clicks and onboard thousands of farmers tomorrow.'
                }
            ]
        }
    }
}
</script>

<style>

</style>