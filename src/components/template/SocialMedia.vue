<template>
    <div class="grid-reseaux">
        <template v-for="(item, index) in socialMedia">
            <div :key="index" class="reseau-icon">
                <a :href="item.link" class="icon-social">
                    <fa :icon="['fab', item.icon]" />
                </a>
            </div>
        </template>
    </div>
</template>

<script>
export default {
    name: 'SocialMedia',
    data() {
        return {
            socialMedia: [
                {
                    link: 'https://twitter.com/ReedifyFinance/',
                    icon: 'twitter'
                },
                {
                    link: 'https://t.me/ReedifyFinance/',
                    icon: 'telegram'
                },
                {
                    link: 'https://discord.gg/f3VXDfwKNb/',
                    icon: 'discord'
                },
                {
                    link: 'https://reedify.medium.com/',
                    icon: 'medium-m'
                }

            ]
        }
    }
}
</script>