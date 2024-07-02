<template>
  <div class="container">
    <div class="row">
        <h2 class="display-2">About</h2>
    </div>
    
     <div class="card cardAbout">
     <div class="col"> 
        <div id="details">
            <div v-if="about?.length">
              <p class="card-text">{{ about[0].message }}</p>
              <p class="card-text1"> Full name: {{ about[0].name }}</p>
              <p class="card-text1"> Location: {{ about[0].location }}</p>
             <p class="card-text1"> Email: {{ about[0].email }}</p>  
            </div>
            <Spinner v-else/>
        </div> 
      </div>
    </div>

  </div>
  
</template>

<script setup>
import Spinner from './Spinner.vue'
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