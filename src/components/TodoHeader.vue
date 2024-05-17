<script>
import { RouterLink } from 'vue-router';
</script>

<template>
  <header>
    <nav class="container">
        <div class="branding">
            <img src="../assets/elephant-48545_640.png" width="100px" alt="elephant"/>
            <h1>Ellie Todos</h1>
        </div>
        <ul class="nav-routes">
            <RouterLink to="/">Home</RouterLink>
            <RouterLink to="/about">About</RouterLink>
        </ul>
    </nav>
  </header>
</template>
