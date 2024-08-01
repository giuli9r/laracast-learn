<script setup>
// import team from "@/team.json";
// import TeamHeader from "@/components/Teams/TeamHeader.vue";
import TeamMember from "@/components/TeamMember.vue";
// import TeamFooter from "@/components/Teams/TeamFooter.vue";
</script>

<template>
  <div id="wrapper">

    <header>
      <div>
        <button 
        class="ng-green-500 hover:bg-green-600 text-white px-4 rounded disabled:bg-gray-400"
        :disabled="true">Add MEMBER (0 Spots Left)
        </button>
      </div>
  
    <div>
      <h3>
        <img src="" alt=":)" class="mr-2 w-5 h-5">
        Smiley Team
        <div class="bg-green-400 w-5 h-5 text-xs text-white rounded-full flex justify-center items-center absolute -rigth-4 top-2">
          5
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
        <TeamMember name="John Dow" email="jonh@mail.com" status="Active"></TeamMember>
        <TeamMember name="Steven Doe" email="steven@doe.com" status="Active"></TeamMember>
        <TeamMember name="Sarah Doe" email="sarah@mail.com" status="Active"></TeamMember>
        <TeamMember name="Messi Doe" email="messi@doe.com" status="Active"></TeamMember>
      </tbody>

    </table>

    <p class="text-rigth text-gray-100 py-4 text-center">
      There are no remaining team sports. Upgrade to add more.
    </p>
  </div>

  <footer class="mt-12 bg-gray-100 py-4 text-center">
    <h5 class="font-semibold text-lg" > Smiley - 5 Member Team</h5>
  </footer>
  </div>

  <!-- <TeamHeader :team="team" /> -->

  <!-- <div class="place-self-center flex flex-col gap-y-3" style="width: 725px">
    <TeamMembers :team="team" />
  </div> -->

  <!-- <TeamFooter :team="team" /> -->
</template>