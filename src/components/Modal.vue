<template>
    <div class="backdrop" @click.self="closeModal">
        <div class="modal" :class="{sale: theme ==='sale'}">
         
        </div>
    </div>
</template>
<script>
export default {
    props: ['theme'],
    methods:{
        closeModal() {
            this.$emit('close')
        }
    }
}
</script>

<style>
.modal {
    width: 400px;
    padding: 200px;
    margin: 100px auto;
    background:white;
    border-radius: 10px;
}
.backdrop {
    top:0;
    position: fixed;
    background: rgba(0,0,0,0.5);
    width: 100%;
    height: 100%;
}
.modal.sale{
    background: crimson;
}
</style>