<template>
    <div class="entry-title d-flex justify-content-between p-2">
        <div>
            <span class="text-success fd-3 fw-bold">15</span>
            <span class="mx-1 fd-3">julio</span>
            <span class="mx-2 fs-4 fw-light">2021</span>
        </div>
        <div>
            <button class="btn btn-danger mx-2">
                borrar
                <i class="fa fa-trash-alt"></i>
            </button>

            <button class="btn btn-primary">
                subir foto
                <i class="fa fa-upload"></i>
            </button>
        </div>
    </div>

    <hr>
    <div class="d-flex flex-column px-3 h-75">
        <textarea placeholder="¿que paso hoy?">
        </textarea>
    </div>

    <Fab icon="fa-save"/>

    <img src="https://kinsta.com/wp-content/uploads/2020/08/tiger-jpg.jpg" alt="entry-picture" class="img-thumbnail">
</template>

<script>
import { defineAsyncComponent } from "vue";

export default {
    components: {
        Fab: defineAsyncComponent(() => import('../components/Fab.vue'))
    }
}
</script>

<style lang="scss" scoped>

    textarea {
        font-size: 20px;
        border: none;
        height: 100%;

        &:focus {
            outline: none;
        }
    }

    img {
        width: 200px;
        position: fixed;
        bottom: 150px;
        right: 20px;
        box-shadow: 0px 5px 10px rgba($color: #000000, $alpha: 0.2);
    }

</style>