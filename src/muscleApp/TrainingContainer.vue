<template>
    <v-list class="listStyle">
        <v-list-tile v-for="trainingPhase in trainingPhases" :key="trainingPhase.title">
            <v-tooltip right>
                <template v-slot:activator="{ on }"> -->
                    <v-btn fab small color="error">
                        <v-icon dark v-text="trainingPhase.icon"></v-icon>
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
        justify-content: flex-end;
        color: rebeccapurple;
        background-color: yellow;
    }
</style>


