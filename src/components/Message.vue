<script setup>
    import { ref } from 'vue';
    defineProps(['open']);
</script>

<template>
    <article class="message is-success is-medium" v-if="open">
        <div class="message-header">
            <p>Message</p>
            <button class="delete" @click="$emit('close')"></button>
        </div>
        <slot></slot>
    </article>
</template>