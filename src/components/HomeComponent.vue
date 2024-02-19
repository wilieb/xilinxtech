<template>
    <v-container>
        <v-row justify="center">
            <v-col cols="12" md="8">
                <div ref="stageContainer">
                    Lets get it done with, already!
                </div>
            </v-col>
        </v-row>
    </v-container>
</template>

<script>
import Konva from 'konva';

export default {
    mounted() {
        this.initKonva();
    },
    methods: {
        initKonva() {
            const stage = new Konva.Stage({
                container: this.$refs.stageContainer,
                width: 500,
                height: 500,
            });

            const layer = new Konva.Layer();
            const circle = new Konva.Circle({
                x: stage.width() / 2,
                y: stage.height() / 2,
                radius: 50,
                fill: 'red',
            });

            layer.add(circle);
            stage.add(layer);
        },
    },
};
</script>

<style scoped>

</style>