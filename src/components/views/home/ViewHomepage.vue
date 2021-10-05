<template>
    <div>
        <app-banner></app-banner>
            <v-crp-token></v-crp-token>
            <info-generator></info-generator>
            <builder-info></builder-info>
            <team-info></team-info>
        <info-powered></info-powered>
    </div>
</template>

<script>
export default {
  name: 'ViewHomepage',
  components: {
    'app-banner': () => import('@/components/template/Banner.vue'),
    'v-crp-token': () => import('@/components/views/home/InfoToken.vue'),
    'info-generator': () => import('@/components/views/home/InfoGenerator.vue'),
    'builder-info': () => import('@/components/views/home/InfoBuilder.vue'),
    'team-info': () => import('@/components/views/home/InfoTeam.vue'),
    'info-powered': () => import('@/components/views/home/InfoPowered.vue')
  }
}
</script>