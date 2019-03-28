<template>
    <v-layout row style="background: green; height: 100%">
      <v-flex>
          <v-list>
            <v-list-tile v-for="training in trainings" :key="training">
                <v-list-tile-content>
                    <v-list-tile-title v-text="training"></v-list-tile-title>
                </v-list-tile-content>
            </v-list-tile>
          </v-list>
        </v-flex>
        <v-flex>
          <trainingContainer :trainingPhases="trainingPhases" style="height: 100%"></trainingContainer>
        </v-flex>
    </v-layout>
</template>

<script>
import TrainingContainer from './muscleApp/TrainingContainer.vue'

export default {
  props: {
    trainingPhases: {
      default: [
        {title: 'Warm up', icon:'alarm'},
        {title: 'Stretich', icon:'list'},
        {title: 'Workout', icon:'lock'},
        {title: 'Cardio', icon:'edit'},
        {title: 'Cardiooo', icon:'search'}
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