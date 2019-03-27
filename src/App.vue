<template>
    <v-layout align-end row style="background: green">
      <v-flex md>
          <v-list>
            <v-list-tile v-for="training in trainings" :key="training">
                <v-list-tile-content>
                    <v-list-tile-title v-text="training"></v-list-tile-title>
                </v-list-tile-content>
            </v-list-tile>
          </v-list>
        </v-flex>
        <v-flex md>
          <trainingContainer :trainingPhases="trainingPhases"></trainingContainer>
        </v-flex>
        
    </v-layout>
</template>

<script>
import TrainingContainer from './muscleApp/TrainingContainer.vue'

export default {
  props: {
    trainingPhases: {
      default: [
        {title: 'Warm up', icon:'fas fa-search'},
        {title: 'Stretich', icon:'fa-list'},
        {title: 'Workout', icon:'fa-lock'},
        {title: 'Cardio', icon:'fa-edit'},
        {title: 'Cardiooo', icon:'fa-search'}
      ]
    },
    trainings: {
      default: ['Trainign2', 'Trainign3', 'Trainign4', 'Trainign5']
    }
  },
  components: {
    'trainingContainer': TrainingContainer
  }
}
</script>

<style scoped>
.listTrainingStyle {
        display: flex;
        flex-direction: row;
        color: rebeccapurple;
    }
</style>