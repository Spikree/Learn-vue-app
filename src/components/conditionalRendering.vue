<template>
    <div>
        <div>
            <div>
                <h2>we're going to see 4 conditional rendering operators</h2>
                <h3>These are</h3>
                <ol>
                    <li>v-if</li>
                    <li>v-else</li>
                    <li>v-else-if</li>
                    <li>v-show</li>
                </ol>
                <button type="button" class="btn btn-primary" @click="$emit('next2', next2)" >Next</button>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        name : 'conditionalRendering',
        emits: [next2]
    }
</script>

<style scoped>

</style>