<template>
  <div>
    <h1>Participants list ({{ participants.length }})</h1>
    <ol>
        <li v-for="person in participants" :key="person">
            {{ person.name }} {{ person.surname }}
        </li>
    </ol>
    <h3>New participant</h3>
    <new-participant-form @added="addNewParticipant($event)"></new-participant-form>
  </div>
</template>

<script>
  import NewParticipantForm from "./NewParticipantForm.vue";

  export default {
    components: {NewParticipantForm},
    data() {
      return {
          participants: [],
      };
    },
    methods: {
      addNewParticipant(newParticipant) {
        this.participants.push(newParticipant);
      }
    }
  };
</script>
