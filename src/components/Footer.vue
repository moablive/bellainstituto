<script setup>
import { computed } from 'vue'

const currentYear = computed(() => new Date().getFullYear())
</script>

<template>
  <footer class="footer text-center py-4 mt-auto">
    <div class="container">
      <p class="mb-0 text-muted">
        &copy; {{ currentYear }} <span class="fw-semibold text-dark">Bella Instituto</span>.
        Todos os direitos reservados.
      </p>
    </div>
  </footer>
</template>
