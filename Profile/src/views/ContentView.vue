<template>
  <div
    class="portfolio"
    :style="{
      display: useDatastore.statuspage ? 'none' : ''
    }"
  >
    <a href="https://ibb.co/q0rjYV2">
      <img src="https://i.ibb.co/s5VR9zX/Blue-and-Black-Modern-Resume.png" alt="" />
    </a>
  </div>
  <div
    class="home-profile"
    :style="{
      display: useDatastore.statuspage == 'home' ? '' : 'none'
    }"
  >
    <div class="profile-img">
      <img
        src="https://st2.depositphotos.com/1104517/11967/v/950/depositphotos_119675554-stock-illustration-male-avatar-profile-picture-vector.jpg"
        alt=""
      />
    </div>
    <div class="profile-content">
      <h2>Hi!, My name is Ariyavas Phaipong</h2>
      <p>I'm looking for a back-end job, is anyone interested in viewing my portfolio?</p>
    </div>
  </div>
  <div
    :style="{
      display: useDatastore.statuspage == 'skill' ? '' : 'none'
    }"
  >
    <skillVue />
  </div>
  <div
    :style="{
      display: useDatastore.statuspage == 'about' ? '' : 'none'
    }"
  >
    <aboutVue />
  </div>
  <div
    :style="{
      display: useDatastore.statuspage == 'project' ? '' : 'none'
    }"
  >
    <projectVue />
  </div>
</template>

<script>
import { useCounterStore } from '../stores/counter'
import skillVue from '../components/skill.vue'
import aboutVue from '../components/about.vue'
import projectVue from '../components/project.vue'
export default {
  data() {
    return {}
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
    aboutVue,
    projectVue
  }
}
</script>
