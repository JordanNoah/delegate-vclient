<template>
    <v-navigation-drawer expand-on-hover rail app>
        <v-list nav>
            <v-list-item 
                v-for="navigationItem in navigationItems" 
                :key="navigationItem.path"
                :prepend-icon="navigationItem.icon"
                :title="navigationItem.title"
                :to="navigationItem.path"
            />
        </v-list>
    </v-navigation-drawer>
</template>

<script lang="ts">
export default {
    data: () => ({
        navigationItems: [
            {
                icon:'mdi-home-outline',
                path:'/app/external',
                title:'Inicio'
            },
            {
                icon:'mdi-account-multiple-outline',
                path:'/app/delegates',
                title:'Docentes'
            },
            {
                icon:'mdi-bell-outline',
                path:'/app/notifications',
                title:'Notificaciones'
            },
            {
                icon:'mdi-account-cog-outline',
                path:'/app/permissions',
                title:'Permisos'
            },
            {
                icon:'mdi-account-multiple-check-outline',
                path:'/app/assignments',
                title:'Asignaciones'
            },
            {
                icon:'mdi-account-arrow-down-outline',
                path:'/app/drops',
                title:'Bajas'
            },
            {
                icon:'mdi-application-cog-outline',
                path:'/app/settings',
                title:'Configuraciones'
            }
        ]
    })
}
</script>