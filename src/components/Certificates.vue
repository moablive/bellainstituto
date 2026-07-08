<script setup>
const certificates = [
  {
    title: 'Workshop Esteticistas Empreendedoras - Nível Intermediário',
    desc: 'Participação em 2018 com carga de 8h, realizado pela Faccialle e Faculdade Monteiro Lobato.',
    url: 'https://www.dropbox.com/scl/fi/0d80id27rtnjg16zfcvzp/Workshop-Esteticistas-Empreendedoras-N-vel-Intermedi-rio.pdf?rlkey=1i4xuyescw9e3d4489rgddqzb&st=5k071b3i&dl=0',
    icon: 'fas fa-certificate'
  },
  {
    title: 'Certificação de Espaço Homologado ABRATTEC',
    desc: 'Selo digital atestando que o estabelecimento cumpre os padrões da ABRATTEC (Associação Brasileira de Tricologia e Terapia Capilar).',
    url: 'https://www.dropbox.com/scl/fi/hzqsxfunfp8speij03tvz/ABRATTEC-Associa-o-Brasileira-de-Tricologia-e-Terapia-Capilar.pdf?rlkey=a90kukfcv288slogtzjx5hb03&st=tlqlpkht&dl=0',
    icon: 'fas fa-award'
  },
  {
    title: 'Curso Profissionalizante de Terapia Capilar',
    desc: 'Habilitação para serviços no couro cabeludo e haste capilar, realizado de 25/08 a 29/08/2025 com carga de 40h (DNA Vital/ABRATTEC).',
    url: 'https://www.dropbox.com/scl/fi/1uv328dbyudcorirhu9o9/Terapia-Capilar-Avan-ada.pdf?rlkey=183uhft6hr2ru84r54ycagwkq&st=fj9ayefk&dl=0',
    icon: 'fas fa-user-graduate'
  },
  {
    title: 'Grade Curricular de Terapia Capilar',
    desc: 'Documento listando 11 módulos de ensino do curso da DNA Vital, incluindo avaliação clínica, tricoscopia e cosmecêuticos.',
    url: 'https://www.dropbox.com/scl/fi/6sxw2j8s0obdtt118x3ac/DNA-Academy-DNA-Vital.pdf?rlkey=bvk1w6u5q3ulspil9f5ski2rm&st=29s1l8qb&dl=0',
    icon: 'fas fa-book-open'
  },
  {
    title: 'Curso de Peeling e Decapagem Biológica',
    desc: 'Realizado em 2019 com carga de 8h/aula no centro técnico Porto da Estética.',
    url: 'https://www.dropbox.com/scl/fi/h4xe9blnxewbpu7e40dbb/Peeling-e-Decapagem-Biol-gica.pdf?rlkey=2tn9j81v9jtsrlhnadcenwbmm&st=irosdpvg&dl=0',
    icon: 'fas fa-certificate'
  },
  {
    title: '2° Workshop Esteticista Empreendedora',
    desc: 'Participação em 2018 com carga de 4h, na Faculdade Monteiro Lobato.',
    url: 'https://www.dropbox.com/scl/fi/dws26w800001hcbnu9t2g/2-Workshop-Esteticista-Empreendedora.pdf?rlkey=ag0h60z60zkrbkehnv9fgvu2a&st=qpu46ymx&dl=0',
    icon: 'fas fa-certificate'
  },
  {
    title: 'Curso de Microagulhamento (2019)',
    desc: 'Realizado em 2019 com carga de 18h/aula no centro técnico Porto da Estética.',
    url: 'https://www.dropbox.com/scl/fi/s99ynkf4z7vi7udzrnzxk/Curso-de-Microagulhamento.pdf?rlkey=j4wy689ek2zdnamr6p4lc9dzt&st=f5m4unms&dl=0',
    icon: 'fas fa-certificate'
  },
  {
    title: 'Técnicas de Limpeza de Pele Magic Skin',
    desc: 'Aperfeiçoamento (Básico e Avançado) realizado em 2018 com carga de 20h/aula pela Cursos Bergmann.',
    url: 'https://www.dropbox.com/scl/fi/70u9b4k31tz500zt8qq3d/Aperfei-oamento-em-T-cnicas-de-Limpeza-de-Pele-Magic-Skin-B-sico-e-Avan-ado.pdf?rlkey=qgm8yyk4faelfh34ulw5a1y6t&st=kjftw3cg&dl=0',
    icon: 'fas fa-certificate'
  },
  {
    title: 'Programação do Curso de Limpeza de Pele',
    desc: 'Conteúdo programático detalhando teoria e prática (extração, peelings, hidrossucção).',
    url: 'https://www.dropbox.com/scl/fi/v1pqc7fqabm9fi7vf2zb0/Programa-o-do-Curso-de-Limpeza-de-Pele-Magic-Skin.pdf?rlkey=u7w4fmk24aarccogms0rx6pp8&st=ldeml5iu&dl=0',
    icon: 'fas fa-book'
  },
  {
    title: 'Curso de Microagulhamento (2019)',
    desc: 'Realizado em 2019 com carga de 16h/aula no centro técnico Porto da Estética.',
    url: 'https://www.dropbox.com/scl/fi/f91hdmcgsqu6eytijcys5/Microagulhamento.pdf?rlkey=steeadbkojzwp9yzgzlhty96e&st=tbtjphxm&dl=0',
    icon: 'fas fa-certificate'
  },
  {
    title: 'Curso de Coaching em Limpeza de Pele',
    desc: 'Formação concluída em 2018 pela Escola de Estética Bel Art.',
    url: 'https://www.dropbox.com/scl/fi/f58e5ddvnmoc6npr2e543/Curso-de-Coaching-em-Limpeza-de-Pele.pdf?rlkey=puxr4ee95f766q8k7ysmnqxxl&st=dt0960km&dl=0',
    icon: 'fas fa-certificate'
  },
  {
    title: 'Curso de Drenagem Linfática',
    desc: 'Formação teórico-prática realizada em 2014 com carga de 16h/aula na OKL Escola.',
    url: 'https://www.dropbox.com/scl/fi/dgapqwayu3xdjfusi22qn/Curso-de-Drenagem-Linf-tica.pdf?rlkey=wh6vtu7s5nmcu5rhbu9nloqyo&st=6t2ubymg&dl=0',
    icon: 'fas fa-certificate'
  },
  {
    title: 'II Simpósio Gaúcho de Emergência e Trauma',
    desc: 'Participação em 2016 com carga de 10h/aula (Pré-COLT RS).',
    url: 'https://www.dropbox.com/scl/fi/wy7mghgjnzu9juxavufdv/II-Simp-sio-Ga-cho-de-Emerg-ncia-e-Trauma-e-Pr-COLT-RS.pdf?rlkey=4729y3k1yoesjcm9ufnyxmuw0&st=lzhx5pgr&dl=0',
    icon: 'fas fa-certificate'
  },
  {
    title: 'II Seminário de Saúde Mental',
    desc: 'Participação no evento em 2014 com carga de 8h, promovido pelo Senac Passo D\'areia.',
    url: 'https://www.dropbox.com/scl/fi/e7jn3rgona37wx84dm9bh/II-Semin-rio-de-Sa-de-Mental-Senac-Passo-D-areia.pdf?rlkey=efvp71uqk44o5sihuzxoshja8&st=ritk82ct&dl=0',
    icon: 'fas fa-certificate'
  },
  {
    title: 'Congresso de Tricologia de Campinas 2026',
    desc: 'Participação em 2026 com carga de 20h presenciais e 16h online sobre atualização em saúde capilar.',
    url: 'https://www.dropbox.com/scl/fi/wgjmvbmi4sehmjpcrqpog/Congresso-de-Tricologia-de-Campinas-2026.pdf?rlkey=qv8di9uc5azaqsn0vg2c547g7&st=mai6r8jj&dl=0',
    icon: 'fas fa-certificate'
  },
  {
    title: 'Tratamento de impacto com tecnologia Hyladerm 10',
    desc: 'Realizado em 2022 com carga de 3h.',
    url: 'https://www.dropbox.com/scl/fi/ftccqyw3l4og2mhujuthv/Tratamento-de-impacto-com-tecnologia-Hyladerm-10.jpg?rlkey=r50oyq978yha7sqyrvl9onyqb&st=9qshgxyg&dl=0',
    icon: 'fas fa-certificate'
  }
]
</script>

<template>
  <section id="certificados" class="py-5 min-vh-100 d-flex align-items-center">
    <div class="container py-5">
      <h2 class="section-heading text-center mb-5">Cursos e Certificados</h2>
      
      <div class="row g-4 justify-content-center">
        <div v-for="(cert, index) in certificates" :key="index" class="col-md-6 col-lg-4">
          <div class="card h-100 shadow-sm border-0 cert-card">
            <div class="card-body d-flex flex-column">
              <div class="cert-icon"><i :class="cert.icon"></i></div>
              <h5 class="card-title fw-bold">{{ cert.title }}</h5>
              <p class="card-text text-muted small mb-4">{{ cert.desc }}</p>
              
              <!-- Link configurado para abrir o Dropbox no navegador (target="_blank" com dl=0 na url original) -->
              <a 
                :href="cert.url" 
                target="_blank" 
                rel="noopener noreferrer" 
                class="btn btn-outline-dark btn-sm mt-auto w-100 rounded-pill"
              >
                <i class="fas fa-external-link-alt me-2"></i>Ver Certificado
              </a>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>
