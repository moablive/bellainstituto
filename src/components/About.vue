<script setup>
</script>

<template>
  <section id="sobre" class="py-5 bg-white" style="margin-top: 60px;">
    <div class="container py-5">
      
      <!-- Título da Seção -->
      <div class="text-center mb-5" data-aos="fade-up">
        <p class="text-uppercase fw-bold text-muted mb-3" style="letter-spacing: 1px; font-size: 0.9rem;">
          Sobre
        </p>
        <h2 class="section-heading display-6 mb-4">
          O Salão de Beleza
        </h2>
      </div>

      <!-- Conteúdo Lado a Lado -->
      <div class="row align-items-center g-5 mt-2">
        
        <!-- Imagem -->
        <div class="col-lg-6" data-aos="fade-right">
          <div class="position-relative rounded overflow-hidden shadow-sm border border-light" style="padding: 10px; background: #fff;">
            <!-- Placeholder temporário de um procedimento de salão -->
            <img 
              src="https://images.unsplash.com/photo-1560066984-138dadb4c035?auto=format&fit=crop&q=80&w=800" 
              alt="Sobre o Salão" 
              class="img-fluid rounded w-100" 
              style="object-fit: cover; aspect-ratio: 4/3;"
            />
          </div>
        </div>

        <!-- Texto Descritivo -->
        <div class="col-lg-6" data-aos="fade-left" data-aos-delay="200">
          <p class="text-muted" style="line-height: 1.8; font-size: 1.05rem;">
            Seja muito bem-vinda ao seu novo espaço de autocuidado e transformação. 
            Nossa missão é realçar o que você tem de melhor, unindo técnicas avançadas, 
            produtos de alta qualidade e um atendimento acolhedor que faz toda a diferença.
          </p>
          <p class="text-muted" style="line-height: 1.8; font-size: 1.05rem;">
            Especialistas em terapia capilar, cortes, colorimetria e estética, 
            estamos sempre em busca de inovação para garantir resultados impecáveis. 
            Aqui, cada detalhe é pensado para proporcionar uma experiência relaxante 
            e elevar a sua autoestima.
          </p>
          <div class="mt-4">
            <a href="#servicos" class="btn btn-outline-dark rounded-pill px-4 py-2 fw-semibold">
              Conheça Nossos Serviços
            </a>
          </div>
        </div>
        
      </div>

    </div>
  </section>
</template>
