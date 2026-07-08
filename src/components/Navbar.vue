<script setup>
import { onMounted } from 'vue'

onMounted(() => {
  const navLinks = document.querySelectorAll('.nav-link')
  const menuToggle = document.getElementById('navbarNav')
  if (menuToggle && window.bootstrap) {
    const bsCollapse = new window.bootstrap.Collapse(menuToggle, { toggle: false })
    navLinks.forEach((l) => {
      l.addEventListener('click', () => {
        if (menuToggle.classList.contains('show')) {
          bsCollapse.toggle()
        }
      })
    })
  }
})
</script>

<template>
  <nav class="navbar navbar-expand-lg fixed-top shadow-sm">
    <div class="container d-flex justify-content-between align-items-center">
      
      <!-- Esquerda: Logo -->
      <a class="navbar-brand fw-bold d-flex align-items-center" href="#">
        <!-- Ícone simulando logo da referência -->
        <i class="fas fa-female text-primary-custom me-2" style="font-size: 2rem;"></i>
        <div class="d-flex flex-column" style="line-height: 1;">
          <span style="font-size: 1.5rem; letter-spacing: -1px;">Bella</span>
          <span class="text-muted" style="font-size: 0.75rem; font-weight: 500; letter-spacing: 1px;">BEAUTY SALON</span>
        </div>
      </a>

      <!-- Botão Hamburger (Mobile) -->
      <button
        class="navbar-toggler border-0"
        type="button"
        data-bs-toggle="collapse"
        data-bs-target="#navbarNav"
        aria-controls="navbarNav"
        aria-expanded="false"
        aria-label="Toggle navigation"
      >
        <span class="navbar-toggler-icon"></span>
      </button>

      <!-- Centro: Links -->
      <div class="collapse navbar-collapse justify-content-center" id="navbarNav">
        <ul class="navbar-nav fw-semibold">
          <li class="nav-item"><a class="nav-link text-primary-custom" href="#sobre">O Salão</a></li>
          <li class="nav-item"><a class="nav-link" href="#servicos">Serviços</a></li>
          <li class="nav-item"><a class="nav-link" href="#especialidades">Especialidades</a></li>
          <li class="nav-item"><a class="nav-link" href="#certificados">Certificados</a></li>
          <li class="nav-item"><a class="nav-link" href="#contato">Fale Conosco</a></li>
        </ul>
      </div>

      <!-- Direita: Botão Agendar -->
      <div class="d-none d-lg-block">
        <a href="#contato" class="btn btn-primary-custom rounded-pill shadow-sm">
          <i class="fas fa-clock me-2"></i> AGENDAR HORÁRIO
        </a>
      </div>

    </div>
  </nav>
</template>
