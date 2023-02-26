<template>
    <div class="backdrop">
        <div class="modal" :class="{sale: theme === 'sale'}">
            <h1>{{ header }}</h1>
            <p>
                {{ text }}
            </p>
            <!-- How should we close it??? -->
            <button @click="closeModal">
                close modal
            </button>
        </div>
    </div>
</template>


<script>
export default {
    name: 'Modal',
    props: ['header', 'text', 'theme'],
    methods: {
        closeModal(){
            this.$emit('close');
        }
    }
}

</script>

<!-- means the style will be scoped -->
<!-- the css selector will select the data-attribute  -->
<style scoped>
    .modal {
        width: 400px;
        padding: 20px;
        margin: 100px auto;
        background: white;
        border-radius: 10px;
    }
    .backdrop {
        top: 0;
        position: fixed;
        background: rgba(0, 0, 0, 0.5);
        width: 100%;
        height: 100%;
    }
     h1 {
        color:lightblue;
     }

     /* Instead of using scoped , we can make the selector more specific */
     /* .modal h1 {
        color: red;
     } */

     .modal.sale {
            background:crimson;
            color:white
     }
</style>