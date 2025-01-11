<script setup lang="ts">
    import ListItem from './ListItem.vue';
    type Item = {
        tittle: string;
        checked?: boolean;
    }
const GroupsItems: Item[] = [
    { tittle: 'Leer un libro al mes' },
    { tittle: 'Hacer ejercicio' },
    { tittle: 'Aprender algo nuevo' },
    ];
</script>

<template>
    <ul>
        <li :key="index" v-for="(item, index) in GroupsItems">
            <ListItem :isChecked="item.checked">
                {{ item.tittle }}
            </ListItem>

        </li>
    </ul>
</template>

<style scoped>
    ul {
        list-style: none;
        padding: 0;
    }
    li {
       margin: 0.5rem 0;
    }
  
</style>