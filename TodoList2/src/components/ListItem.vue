<script setup lang="ts">
    defineProps<{
        isChecked?: boolean;
    }>();
</script>

<template>
    <label :class="{'checked': isChecked}">
      <input type="checkbox" :ischeck="isChecked" />
      <slot></slot>

    </label>
</template>

<style scoped>
    Label {
        cursor: pointer;
    }
    .checked {
        text-decoration: line-through;
    }
</style>