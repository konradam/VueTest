<template>
    <v-list class="listStyle">
        <v-list-tile v-for="trainingPhase in trainingPhases" :key="trainingPhase.title">
            <v-tooltip right>
                <template v-slot:activator="{ on }">
                    <v-btn fab small>
                        <v-icon style="color: red" v-text="trainingPhase.icon"></v-icon>
                    </v-btn>
                </template>
                <span v-text="trainingPhase.title"></span>
            </v-tooltip>
        </v-list-tile>
    </v-list>
</template>

<script>
export default {
    props: {
        trainingPhases: {
            type: Array
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


