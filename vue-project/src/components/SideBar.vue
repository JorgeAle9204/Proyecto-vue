<template>
    <div class = "sidebar">
<h2 >Bienvenido</h2>
<h3>Nombre: {{ nombre }}</h3>
<h3>Email: {{ email }}</h3>

<ul>
    <li><router-link to = "/contador">Contador</router-link></li>
    <li><router-link to = "/lista-de-tareas">ListaDeTareas</router-link></li>
    <li><router-link to = "/registrar">Registrar</router-link></li>
</ul>
</div>

</template>

<script setup>
import { useRegistrarStore } from '@/modules/registro/stores/registarStore';
import {ref, watch} from 'vue';
const registarStore = useRegistrarStore();
const nombre = ref(registarStore.nombre.value);
const email  = ref(registarStore.email.value);

watch (() => registarStore.nombre, (newValue) => {
    nombre.value = newValue
});

watch (() => registarStore.email, (newValue) => {
    email.value = newValue
});

</script>

<style>
.sidebar {
width: 200px;
background-color: #f0f0f0;
padding: 20px;
}
</style>