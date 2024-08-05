<script setup>
import team from "./../team.json"
import TeamHeader from "../components/TeamHeader.vue";
import TeamMembersList from "../components/TeamMembersList.vue";
import TeamFooter from "../components/TeamFooter.vue";
// console.log(team);

</script>

<template>
  <div id="wrapper">

    <TeamHeader :team="team" />
    <TeamMembersList :team="team" ></TeamMembersList>
    <TeamFooter :team="team"></TeamFooter>
    
  </div>
</template>