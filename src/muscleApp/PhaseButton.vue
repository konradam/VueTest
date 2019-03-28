<template>
    <v-tooltip right>
        <template v-slot:activator="{on}">
            <v-btn fab small v-on="on" @click="showTrainingPhaseContainer(trainingPhases)">
                <v-icon style="color: red" v-text="icon"></v-icon>
            </v-btn>
        </template>
        <span v-text="tooltip"></span>
    </v-tooltip>
</template>

<script>
export default {
    props: {
        icon: {
            type: String
        },
        tooltip: {
            type: String
        }
    }
}
</script>
