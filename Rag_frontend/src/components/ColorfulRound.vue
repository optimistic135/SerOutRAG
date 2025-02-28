<template>
    <div class="image-container">
        <img alt="ColorfulRound" src="../assets/HomeImage/ColorfulRound.png" class="colorful-round">
        <p class='my-font'>SmartMath</p>
    </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue';

export default defineComponent({
    name: 'ColorfulRound',
});
</script>

<style scoped>
.my-font {
    font-family: 'Kalam';
    font-size: 72px;
    letter-spacing: 10px;
    color: rgba(121, 72, 234, 1);
}

.image-container {
    position: relative;
    top: -30px;
    left: 70px;
    width: 670px; 
    height: 670px; 
    display: flex;
    justify-content: center;
    align-items: center;
    border-radius: 50%; 
    overflow: hidden; 
}

.colorful-round {
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%); /* 调整为居中对齐 */
    transform-origin: center;
    width: 0;
    height: 0;
    opacity: 0;
    animation: slow-rotate 8s linear infinite, scale-up 1.25s ease-out forwards;
}

@keyframes slow-rotate {
    from {
        transform: translate(-50%, -50%) rotate(0deg);
    }
    to {
        transform: translate(-50%, -50%) rotate(360deg);
    }
}

@keyframes scale-up {
    from {
        width: 0;
        height: 0;
        opacity: 0;
    }
    to {
        width: 900px; /* 适当增大图片最终大小 */
        height: 900px; 
        opacity: 1;
    }
}
</style>