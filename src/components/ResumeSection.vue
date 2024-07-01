<template>
    <div class="container">
      <div class="row">
          <h2 class="display-2">Resume</h2>
      </div>
       
     
       <div class="col cardResume">  
        <div class="card text-white">
          <div id="details">
              <div v-if="resume?.length">
                <img src="https://anushqakandan.github.io/All-images/vue/SpineRoad2.png " alt="resume" class="img-resume1" loading="lazy">
                  <p class="Resume-Title">{{ resume[0].place }}</p>
                <p class="Resume-Description">{{ resume[0].description }}</p>
              </div>
              <Spinner v-else/>
          </div> 
        </div>
        <div class="card text-white">
          <div id="details">
              <div v-if="resume?.length">
                <img src="https://anushqakandan.github.io/All-images/vue/UWC1.png " alt="resume" class="img-resume2" loading="lazy">
                  <p class="Resume-Title">{{ resume[1].place }}</p>
                <p class="Resume-Description">{{ resume[1].description }}</p>
              </div>
              <Spinner v-else/>
          </div> 
        </div>
  
        <div class="card text-white">
          <div id="details">
              <div v-if="resume?.length">
                <img src="https://anushqakandan.github.io/All-images/vue/Sigma2.png " alt="resume" class="img-resume3" loading="lazy">
                  <p class="Resume-Title">{{ resume[2].place }}</p>
                <p class="Resume-Description">{{ resume[2].description }}</p>
              </div>
              <Spinner v-else/>
          </div> 
        </div>
  
        <div class="card text-white">
          <div id="details">
              <div v-if="resume?.length">
                <img src="https://anushqakandan.github.io/All-images/vue/LifeChoices.png " alt="resume" class="img-resume4" loading="lazy">
                  <p class="Resume-Title">{{ resume[3].place }}</p>
                <p class="Resume-Description">{{ resume[3].description }}</p>
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
  const resume = computed(() => store.state.resume)
  
  
  onMounted(() => {
      store.dispatch('fetchResume')
  })
  
  </script>
  
