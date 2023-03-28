<template>
    <div class="profile">
        <header>
            <navbarVue />
        </header>
        <ContentView />
    </div>
</template>

<script>
import navbarVue from '../components/navbar.vue';
import ContentView from './ContentView.vue'
export default {
    components: {
        navbarVue,
        ContentView
    }
}
</script>