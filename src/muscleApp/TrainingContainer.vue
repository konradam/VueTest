<template >
    <div class="listStyle">
        <phaseButton v-for="trainingPhase in trainingPhases" :key="trainingPhase.title" :icon="trainingPhase.icon" :tooltip="trainingPhase.title"></phaseButton>
    </div>
</template>

<script>
import PhaseButton from './PhaseButton.vue'
export default {
    props: {
        trainingPhases: {
            type: Array
        },
        currentPhase: {
        }
    },
    components: {
        'phaseButton': PhaseButton
    },
    methods: {
        showTrainingPhaseContainer: function(phase){
            this.currentPhase = phase;
        }
    }
}
</script>

<style scoped>
    .listStyle {
        display: flex;
        flex-direction: column;
        align-items: flex-start;
        justify-content: center;
        color: rebeccapurple;
        background-color: yellow;
    }
</style>


