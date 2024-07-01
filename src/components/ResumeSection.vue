<template>
    <div class="container">
      <div class="row">
          <h2 class="display-2">Resume</h2>
      </div>
       
     
       <div class="col cardResume">  
        <div class="card text-white">
          <div id="details">
              <div v-if="resume?.length">
                  <p class="Resume-Title">{{ resume[0].place }}</p>
                <p class="Resume-Description">{{ resume[0].description }}</p>
              </div>
              <Spinner v-else/>
          </div> 
        </div>
        <div class="card text-white">
          <div id="details">
              <div v-if="resume?.length">
                  <p class="Resume-Title">{{ resume[1].place }}</p>
                <p class="Resume-Description">{{ resume[1].description }}</p>
              </div>
              <Spinner v-else/>
          </div> 
        </div>
  
        <div class="card text-white">
          <div id="details">
              <div v-if="resume?.length">
                  <p class="Resume-Title">{{ resume[2].place }}</p>
                <p class="Resume-Description">{{ resume[2].description }}</p>
              </div>
              <Spinner v-else/>
          </div> 
        </div>
  
        <div class="card text-white">
          <div id="details">
              <div v-if="resume?.length">
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
  
  <style>
  
  </style>