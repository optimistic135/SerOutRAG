<template>
    <div class="man-in-work">
        <img src="../assets/HomeImage/WorkHardMan.png" alt="ManInHome" @click="showNextChat">
        <transition name="fade">
            <img v-if="currentChatIndex < 4 && currentChatIndex >= 0" src="../assets/HomeImage/chat1.png" alt="chat-green" class="chat-green-pos animated-chat">
        </transition>
        <transition name="fade">
            <img v-if="currentChatIndex < 4 && currentChatIndex >= 1" src="../assets/HomeImage/chat2.png" alt="chat-yellow" class="chat-yellow-pos animated-chat">
        </transition>
        <transition name="fade">
            <img v-if="currentChatIndex < 4 && currentChatIndex >= 2" src="../assets/HomeImage/chat3.png" alt="chat-blue" class="chat-dep-blue-pos animated-chat">
        </transition>
        <transition name="fade">
            <img v-if="currentChatIndex < 4 && currentChatIndex >= 3" src="../assets/HomeImage/chat4.png" alt="chat-blue" class="chat-blue-pos animated-chat">
        </transition>
        <transition name="fade">
            <img v-if="currentChatIndex >= 4" src="../assets/HomeImage/chat5.png" alt="chat-blue" class="chat-to-start animated-chat">
        </transition>
    </div>
</template>

<script lang="ts">
import { defineComponent, ref } from 'vue';

export default defineComponent({
    name: 'ManInHome',
    setup() {
        const currentChatIndex = ref(-1);

        const showNextChat = () => {
            if (currentChatIndex.value < 4) {
                currentChatIndex.value++;
            } else {
                currentChatIndex.value = 4;
                setTimeout(() => {
                    currentChatIndex.value = -1;
                }, 500); 
            }
        };

        return {
            currentChatIndex,
            showNextChat
        };
    }
});
</script>

<style scoped>
.man-in-work {
    position: relative;
    left: -100px;
    top: 42px;
    width: 1098.86px;
    height: 688.94px;
    opacity: 1;
}

.chat-green-pos {
    position: absolute;
    left: 700px;
    top: 270px;
    width: 253px;
    height: 166px;
    opacity: 1;
}

.chat-yellow-pos {
    position: absolute;
    left: 300px;
    top: -150px;
    width: 253px;
    height: 166px;
    opacity: 1;
}

.chat-dep-blue-pos {
    position: absolute;
    left: 850px;
    top: 50px;
    width: 250px;
    height: 200px;
    opacity: 1;
}

.chat-blue-pos {
    position: absolute;
    left: 670px;
    top: -100px;
    width: 200px;
    height: 160px;
    opacity: 1;
}

.chat-to-start {
    position: absolute;
    left: 700px;
    top: -80px;
    width: 400px;
    height: 320px;
    opacity: 1;
}

.animated-chat {
    animation: slide-up 1s ease-out;
}

@keyframes slide-up {
    from {
        transform: translateY(100%);
        opacity: 0;
    }
    to {
        transform: translateY(0);
        opacity: 1;
    }
}

.fade-enter-active,
.fade-leave-active {
    transition: opacity 0.5s;
}

.fade-enter,
.fade-leave-to {
    opacity: 0;
}
</style>