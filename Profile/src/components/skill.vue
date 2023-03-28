<template>
    <div class="skill-profile">
        <div class="profile-content">
            <h3>Expertise</h3>
            <div v-for="item in dataEpx">
                <span>{{ item.langguage }}</span>
                <div class="progress">
                    <div class="progress-bar" role="progressbar" :style="{ 'width': item.point + '%' }"
                        :class="{ 'bg-success': item.point > 25 }" :aria-valuenow="item.point" aria-valuemin="0"
                        aria-valuemax="100">{{ item.tier }}</div>
                </div>
            </div>

        </div>
    </div>
</template>

<script lang="js">
export default {
    data() {
        return {
            dataEpx: [{ langguage: "C++", point: 50, tier: "BASIC" }, { langguage: "C#", point: 25, tier: "BASIC" }, { langguage: "JAVA", point: 50, tier: "BASIC" }, { langguage: "PYTHON", point: 25, tier: "BASIC" }]
        }
    }
}
</script>