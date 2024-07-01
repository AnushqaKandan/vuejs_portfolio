<template>
  <div class="container">
      <div class="row">
          <h2 class="display-2">Skills</h2>
      </div>


   <div class="col cardSkills"> 
     <div class="card text-white">
      <div id="details">
        <div v-if="skills?.length">
            <img src="https://anushqakandan.github.io/All-images/vue/HTML.png " alt="skills" class="img-skills" loading="lazy">
            <p class="Skills-Name">{{ skills[0].name }}</p>
            <p class="Skills-Level">{{ skills[0].level }}</p>
        </div>
        <Spinner v-else/>
     </div> 
    </div>

    <div class="card text-white">
     <div id="details">
        <div v-if="skills?.length">
            <img src="https://anushqakandan.github.io/All-images/vue/CSS.png " alt="skills" class="img-skills" loading="lazy">
            <p class="Skills-Name">{{ skills[1].name }}</p>
            <p class="Skills-Level">{{ skills[1].level }}</p>
        </div>
        <Spinner v-else/>
     </div> 
    </div>
    
    <div class="card text-white">
     <div id="details">
        <div v-if="skills?.length">
            <img src="https://anushqakandan.github.io/All-images/vue/Bootstrap.png " alt="skills" class="img-skills" loading="lazy">
            <p class="Skills-Name">{{ skills[2].name }}</p>
            <p class="Skills-Level">{{ skills[2].level }}</p>
        </div>
        <Spinner v-else/>
     </div> 
    </div>

    <div class="card text-white">
     <div id="details">
        <div v-if="skills?.length">
            <img src="https://anushqakandan.github.io/All-images/vue/ " alt="skills" class="img-skills" loading="lazy">
            <p class="Skills-Name">{{ skills[3].name }}</p>
            <p class="Skills-Level">{{ skills[3].level }}</p>
        </div>
        <Spinner v-else/>
     </div> 
    </div>

    <div class="card text-white">
     <div id="details">
        <div v-if="skills?.length">
            <img src="https://anushqakandan.github.io/All-images/vue/ " alt="skills" class="img-skills" loading="lazy">
            <p class="Skills-Name">{{ skills[4].name }}</p>
            <p class="Skills-Level">{{ skills[4].level }}</p>
        </div>
        <Spinner v-else/>
     </div> 
    </div>

    <div class="card text-white">
     <div id="details">
        <div v-if="skills?.length">
            <img src="https://anushqakandan.github.io/All-images/vue/ " alt="skills" class="img-skills" loading="lazy">
            <p class="Skills-Name">{{ skills[5].name }}</p>
            <p class="Skills-Level">{{ skills[5].level }}</p>
        </div>
        <Spinner v-else/>
     </div> 
    </div>

    <div class="card text-white">
     <div id="details">
        <div v-if="skills?.length">
            <img src="https://anushqakandan.github.io/All-images/vue/ " alt="skills" class="img-skills" loading="lazy">
            <p class="Skills-Name">{{ skills[6].name }}</p>
            <p class="Skills-Level">{{ skills[6].level }}</p>
        </div>
        <Spinner v-else/>
     </div> 
    </div>

    <div class="card text-white">
     <div id="details">
        <div v-if="skills?.length">
            <img src="https://anushqakandan.github.io/All-images/vue/ " alt="skills" class="img-skills" loading="lazy">
            <p class="Skills-Name">{{ skills[7].name }}</p>
            <p class="Skills-Level">{{ skills[7].level }}</p>
        </div>
        <Spinner v-else/>
     </div> 
    </div>

    <div class="card text-white">
     <div id="details">
        <div v-if="resume?.length">
            <img src="https://anushqakandan.github.io/All-images/vue/ " alt="skills" class="img-skills" loading="lazy">
            <p class="Skills-Name">{{ skills[8].name }}</p>
            <p class="Skills-Level">{{ skills[8].level }}</p>
        </div>
        <Spinner v-else/>
     </div> 
    </div>
 </div>
</div>

</template>

<script setup>
import { computed, onMounted } from 'vue'
  import { useStore } from 'vuex'
  const store = useStore()
  const skills = computed(() => store.state.skills)
  
  
  onMounted(() => {
      store.dispatch('fetchSkills')
  })
</script>

