<template>
    <div class="install">
        <div class="text">
            <div class="content">
            <h2>How to install vue.js to your computer</h2>
            <p>
                <ol>
                    <li>Open terminal whichever you prefer</li>
                    <li>use the command 'npm i vue@next' or 'npm i -g@vue/cli'</li>
                    <li>After that check if vue is installed in your computer by using the command 'vue --version'</li>
                </ol>
            </p>
            <button type="button" class="btn btn-primary" @click="$emit('next', next)" >Next</button>
        </div>
        </div>
    </div>
</template>

<script>
    export default {
        name: "installingVue",
        emits: ['next']
    }
</script>

<style scoped>
    .install{
        display: flex;
        align-items: center;
        justify-content: center;
        height: 100vh;
    }

    .text{
        width: 100%; /* Adjust the width as needed */
        max-width: 400px; /* Set a maximum width if necessary */
        border: 1px solid #ccc;
        border-radius: 8px;
        overflow: hidden;
        box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
    }

    .content {
        padding: 20px;
        text-align: center;
    }
</style>