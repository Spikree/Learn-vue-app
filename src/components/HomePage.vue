<template>
    <div class="homepage">
        <div class="intro">
            <div class="content">
            <h2>Learn vue</h2>
            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Ut accusamus natus reiciendis tempora asperiores nihil iure provident, distinctio obcaecati! Eveniet pariatur cupiditate at labore similique incidunt reiciendis consequuntur iste illum! Lorem ipsum dolor sit amet consectetur adipisicing elit. Veritatis incidunt quam minima adipisci iusto dignissimos laboriosam dolorem molestiae, et consectetur numquam ipsam, natus necessitatibus dolorum atque, quidem porro? Optio, aliquam?</p>
            <button type="button" class="btn btn-primary" @click="$emit('close', name)">Lets start</button>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        name: "HomePage",
        emits: {
            close: (name) => {
                if(!name) {
                    return false
                } else{
                    return true
                }
            }
        },
        data() {
            return {
                name : '',
            }
        }
    }
</script>

<style scoped>

    .homepage{
    display: flex;
    align-items: center;
    justify-content: center;
    height: 100vh;
    }
    .intro {
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