<template>
    <div class="home-profile" :style="{
        display: useDatastore.statuspage == 'home' ? '' : 'none'
    }">
        <div class="profile-img">
            <img src="../picture/Profile Icon.jpg" alt="Profile">
        </div>
        <div class="profile-content">
            <h2>
                Hi!, My name is Ariyavas Phaipong
            </h2>
            <p>
                I'm looking for a back-end job, is anyone interested in viewing my portfolio?
            </p>
        </div>
    </div>
    <div>
        <skillVue />
    </div>
</template>

<script>
import { useCounterStore } from '../stores/counter';
import skillVue from '../components/skill.vue'
export default {
    data() {
        return {

        }
    },
    setup() {
        const useDatastore = useCounterStore()
        return { useDatastore }
    },
    methods: {
        test() {
            console.log(this.useDatastore.statuspage)
        }
    },
    components: {
        skillVue,
    }
}
</script>