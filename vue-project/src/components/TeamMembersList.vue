<script setup>
import TeamMember from './TeamMember.vue';
defineProps({
    team: Object
})
</script>

<template>
    
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

</template>