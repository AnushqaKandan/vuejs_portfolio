<template>
    <div class="container">
      <div class="row">
          <h2 class="display-2">About</h2>
      </div>
      
       <div class="card">
        <div>
          <h3>This is me</h3>
        </div>
       <div class="col"> 
          <div id="details">
              <p v-if="about?.length">
                <span>{{ about[0].message }}</span>
              </p>
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
  const about = computed(() => store.state.about)
  
  
  onMounted(() => {
      store.dispatch('fetchAbout')
  })
  
  </script>
  
  <style>
  
  </style>