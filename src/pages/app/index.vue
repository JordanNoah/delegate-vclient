<template>
    <router-view />
</template>

<script>

export default {
    name: 'App',
    components: {
        AppBar: () => import('@/components/AppBar.vue'),
        NavigationDrawer: () => import('@/components/NavigationDrawer.vue'),
    },
};
</script>