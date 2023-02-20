<template>
    <div class="backdrop">
        <div class="modal">
            <h1>Modal Title</h1>
            <p>
                modal content
            </p>
            <!-- How should we close it??? -->
            <button>
                close modal
            </button>
        </div>
    </div>
</template>

<script>
export default {
    name: 'Modal',
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
        color:red;
     }

     /* Instead of using scoped , we can make the selector more specific */
     /* .modal h1 {
        color: red;
     } */
</style>