<script setup>
import { onMounted } from 'vue'

onMounted(() => {
  // Inicializa o script do Calendly dinamicamente para evitar problemas no Vue
  const script = document.createElement('script')
  script.setAttribute('src', 'https://assets.calendly.com/assets/external/widget.js')
  script.async = true
  document.head.appendChild(script)
})
</script>

<template>
  <section id="contato" class="py-5 bg-light-custom">
    <div class="container py-5">
      <h2 class="section-heading text-center mb-4">Agende seu Horário</h2>
      <p class="text-center text-muted mb-5">
        Escolha o melhor dia e horário para seu momento de autocuidado diretamente no calendário abaixo.
      </p>

      <div class="row justify-content-center">
        <div class="col-12 col-lg-10">
          <div 
            class="card shadow-sm border-0" 
            style="border-radius: 18px; overflow: hidden; background: rgba(255, 255, 255, 0.7); backdrop-filter: blur(10px);"
          >
            <div class="card-body p-0">
              <div 
                class="calendly-inline-widget" 
                data-url="https://calendly.com/leandrabrandeburskicapilar/30min?hide_event_type_details=1" 
                style="min-width:320px;height:700px;"
              ></div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>
