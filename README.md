# Bella Instituto - Salão de Beleza ✨

Um projeto web moderno e elegante desenvolvido para o Bella Instituto, um salão de beleza premium focado em terapias capilares, estética facial e serviços especializados. A interface foi projetada para encantar clientes com animações fluidas, efeitos de *glassmorphism* e uma paleta de cores rica (Magenta/Rosa).

## 🚀 Tecnologias Utilizadas

Este projeto foi construído utilizando as seguintes ferramentas e tecnologias modernas:

<p align="center">
  <a href="https://skillicons.dev">
    <img src="https://skillicons.dev/icons?i=vue,vite,js,html,css,bootstrap,git&theme=light" alt="Skill Icons" />
  </a>
</p>

*   **Vue.js 3:** Framework reativo e componentizado.
*   **Vite:** Ferramenta de build super rápida para desenvolvimento.
*   **Bootstrap 5:** Estrutura de grid e utilitários de layout.
*   **AOS (Animate On Scroll):** Animações suaves ativadas via scroll.
*   **FontAwesome:** Ícones ricos e vetorizados.

## 🌟 Funcionalidades Principais

- **Design Responsivo:** Adaptável perfeitamente para desktops, tablets e smartphones.
- **Animações e Interações Premium:** Micro-animações e transições de hover (ex: botão de agendar e cartões de fotos) que dão vida à página.
- **Agendamento Integrado:** Incorporação do *Calendly* na seção de Contatos, facilitando a conversão de clientes.
- **Galeria e Certificados:** Integração com Dropbox para visualização de portfólios, fotos de antes/depois e certificados da profissional.

## ⚙️ Como Executar o Projeto Localmente

1. Certifique-se de ter o [Node.js](https://nodejs.org/) instalado em sua máquina.
2. No diretório raiz do projeto, instale as dependências:
   ```bash
   npm install
   ```
3. Inicie o servidor de desenvolvimento:
   ```bash
   npm run dev
   ```
4. O Vite iniciará o servidor, geralmente disponível em `http://localhost:5173`. Acesse no seu navegador preferido.

## 🚀 Deploy em Produção

O site roda em container no servidor próprio (`awlsrv`) e é publicado em
`https://bellainstituto.com.br` por um túnel da Cloudflare. Saiu da hospedagem da
Hostinger em 01/09/2026.

```bash
docker compose up -d --build
```

O `Dockerfile` é multi-stage — `npm ci && npm run build` no `node:22-alpine`, e só o
`dist/` vai para o `nginx:alpine`. Não é preciso ter Node no host, e o `nginx.conf`
cuida do fallback de SPA e do cache dos assets com hash.

O container **não publica porta no host**: ele vive na rede `bellainstituto_net`, e
quem chega da internet é o `bellainstituto_tunnel`, na mesma rede. Por isso a rede é
`external: true` no compose e precisa existir antes:

```bash
docker network create bellainstituto_net
```

A configuração do túnel, os registros DNS e o passo a passo de recuperação estão no
`README.md` do diretório acima (`BellaInstituto/`), junto da stack do cloudflared.

## 📂 Estrutura de Diretórios

```
bellainstituto/
├── public/                 # Imagens e assets estáticos gerais
├── src/
│   ├── assets/images/      # Imagens usadas nos componentes (ex: foto principal)
│   ├── components/         # Blocos da aplicação (Navbar, Hero, About, etc.)
│   ├── App.vue             # Componente raiz
│   ├── main.js             # Ponto de entrada do Vue
│   └── style.css           # Estilos globais, variáveis e efeitos hover
├── index.html              # Template HTML principal (imports CDN)
├── package.json            # Dependências do projeto
├── Dockerfile              # Build da SPA + entrega estática por nginx
├── nginx.conf              # SPA fallback e cache dos assets
└── docker-compose.yml      # Serviço bellainstituto_web
```

---
Feito com 💖 para elevar a presença digital do Bella Instituto!
