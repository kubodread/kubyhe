<template>

<div class="figt">
                <img :src="texto.imagen" :alt="texto.titulo">
                <div class="textf" >
                {{ texto.informacion }}
                </div>
</div>


</template>


<script>
export default {
    name: 'ImgText',
        props: {
         texto: {
            type: Object,
            required: true
        },
    },
};
</script>

<style scoped>
    .figt {
        display: flex;
        width: 280px;
        height: fit-content;
        justify-content: space-between;
        flex-direction: column;
        align-items: center;
        background-color: rgba(211, 211, 211, 0.466);
        border-radius: 15px;
        padding: 5px;
    }

    .textf {
        text-align: justify;
        font-size: 15px;
        padding: 0 10px;
    }

        .figt img {
        width: 70%;
        border-radius: .61em;
        mask-image: linear-gradient( #1f2937 40%, transparent );
        justify-content: center;
        border-radius: 15px;

    }
</style>
