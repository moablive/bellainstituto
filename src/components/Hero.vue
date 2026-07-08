<script setup>
</script>

<template>
  <!-- Fundo com a foto solicitada -->
  <section 
    id="hero" 
    class="position-relative d-flex align-items-center"
    style="
      min-height: 85vh; 
      background: url('https://www.dropbox.com/scl/fi/0eku2c1ajuy5jtxzply3t/AJUSTADO.jpeg?rlkey=21ojia7uzgo7u34dp5q5a6b3j&st=iliceuox&raw=1') no-repeat top center; 
      background-size: cover;
      margin-bottom: 80px; /* Espaço para a barra sobreposta */
    "
  >
    <!-- Overlay gradiente suave para garantir leitura do texto -->
    <div class="position-absolute top-0 start-0 w-100 h-100" style="background: linear-gradient(to right, rgba(255,255,255,0.9) 0%, rgba(255,255,255,0.6) 40%, transparent 100%);"></div>

    <div class="container position-relative z-2">
      <div class="row">
        <div class="col-lg-7" data-aos="fade-right">
          <p class="text-uppercase fw-bold text-muted mb-1" style="letter-spacing: 2px; font-size: 0.9rem;">
            O Salão de Beleza
          </p>
          <h1 class="display-3 fw-black text-primary-custom" style="font-weight: 900; line-height: 1;">
            SUA BELEZA EM <br/>
            <span class="text-outline-stroke" style="font-size: 1.15em;">DESTAQUE</span>
          </h1>
        </div>
      </div>
    </div>

    <!-- Barra de Informações Sobreposta (Bottom) -->
    <div class="position-absolute w-100 d-none d-md-block" style="bottom: -50px; z-index: 10;" data-aos="fade-up" data-aos-delay="300">
      <div class="container">
        <div class="row g-0 shadow-lg rounded overflow-hidden">
          
          <!-- Seção Rosa Forte (Contatos) -->
          <div class="col-md-9 bg-primary-custom text-white p-4 d-flex align-items-center justify-content-between">
            <div class="d-flex align-items-center gap-3 w-33">
              <i class="fas fa-map-marker-alt fs-4"></i>
              <div style="font-size: 0.85rem; line-height: 1.2;">
                R. Rubéns Rosa Guedes, 225<br/>Jardim Itu
              </div>
            </div>
            
            <div class="d-flex align-items-center gap-3 w-33 px-3" style="border-left: 1px solid rgba(255,255,255,0.2); border-right: 1px solid rgba(255,255,255,0.2);">
              <i class="far fa-clock fs-4"></i>
              <div style="font-size: 0.85rem; line-height: 1.2;">
                Segunda a Sexta das<br/>7:00h as 18:00h
              </div>
            </div>

            <div class="d-flex align-items-center gap-3 w-33 ps-3">
              <i class="fab fa-whatsapp fs-4"></i>
              <div class="fw-bold fs-5">
                (51) 98652-6924
              </div>
            </div>
          </div>

          <!-- Seção Rosa Claro (Agendar) -->
          <div class="col-md-3 bg-primary-light p-4 d-flex align-items-center justify-content-center cursor-pointer text-primary-custom fw-bold transition-all" style="cursor: pointer;" onclick="document.getElementById('contato').scrollIntoView({behavior: 'smooth'})">
            <div class="d-flex align-items-center gap-2">
              <i class="far fa-calendar-check fs-4"></i>
              AGENDAR HORÁRIO
            </div>
          </div>

        </div>
      </div>
    </div>
  </section>
</template>
