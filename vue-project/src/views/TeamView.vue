<script setup>
// import team from "@/team.json";
import team from "./../team.json"
// import TeamHeader from "@/components/Teams/TeamHeader.vue";
import TeamMember from "@/components/TeamMember.vue";
// import TeamFooter from "@/components/Teams/TeamFooter.vue";
console.log(team);
</script>

<template>
  <div id="wrapper">

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

  <div class="place-self-center flex flex-col gap-y-3" style="width: 725px">
    <table class="table-fixed border-spacing-2 border-separate">
      <thead>
        <th class="text-left px-6 py-2"> Name </th>
        <th class="text-left px-6 py-2"> Email </th>
        <th class="text-left px-6 py-2"> Status </th>
      </thead>

      <tbody>
        <TeamMember v-for="(m) in team.members" :name="m.name" :email="m.email" :status="m.status" :key="m.id" ></TeamMember>
      </tbody>
    </table>

    <p class="text-rigth text-gray-500 py-4 text-center" v-show="team.spots <= team.members.length">
      There are no remaining team sports. Upgrade to add more.
    </p>
  </div>

  <footer class="mt-12 bg-gray-100 py-4 text-center">
    <h5 class="font-semibold text-lg" >  {{ team.name }} -  {{ team.spots }} Member Team</h5>
  </footer>

  </div>

  <!-- <TeamHeader :team="team" /> -->

  <!-- <div class="place-self-center flex flex-col gap-y-3" style="width: 725px">
    <TeamMembers :team="team" />
  </div> -->

  <!-- <TeamFooter :team="team" /> -->
</template>