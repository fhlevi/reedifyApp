<template>
  <div>
    <view-homepages></view-homepages>
  </div>
</template>

<script>
export default {
  name: 'Index',
  components: {
    'view-homepages': () => import('@/components/views/home/ViewHomepage.vue')
  }
}
</script>