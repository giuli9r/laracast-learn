<script setup>
defineProps({
  team: Object
})
</script>

<template>
    
    <header class="flex space-between">
      <div>
        <button 
        class=":not(:hover):bg-green-200 hover:bg-green-600 text-black px-4 py-2 rounded" :disabled="team.members.length == team.spots"
        >Add MEMBER ( {{ team.spots - team.members.length }} Spots Left)
        </button>
      </div>
  
    <div>
      <h3 class="inline-flex items-center text-3xl relative">
        <img src="" alt=":)" class="mr-2 ">
        {{ team.name }} Team
        <div class="bg-green-400 w-5 h-5 text-xs text-white rounded-full flex justify-center items-center absolute rigth-4 top-2">
          {{ team.spots }}
        </div>
      </h3>
    </div>
  </header>

</template>