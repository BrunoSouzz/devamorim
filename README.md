# 🌐 DevAmorim — Portfólio Pessoal

<p align="center">
  <img src="https://img.shields.io/badge/Vue.js-3.x-4FC08D?style=for-the-badge&logo=vuedotjs&logoColor=white" alt="Vue 3" />
  <img src="https://img.shields.io/badge/Vite-646CFF?style=for-the-badge&logo=vite&logoColor=white" alt="Vite" />
  <img src="https://img.shields.io/badge/Tailwind_CSS-38B2AC?style=for-the-badge&logo=tailwind-css&logoColor=white" alt="Tailwind CSS" />
  <img src="https://img.shields.io/badge/Vercel-000000?style=for-the-badge&logo=vercel&logoColor=white" alt="Vercel" />
</p>

> Aplicação web desenvolvida para apresentar minha trajetória profissional, competências técnicas e os principais projetos desenvolvidos em Full Stack, Mobile e Automação.

🔗 **Acesse o site ao vivo:** [devamorim.vercel.app](https://devamorim.vercel.app)

---

## 📋 Sumário

- [Visão Geral](#-visão-geral)
- [Tecnologias Utilizadas](#-tecnologias-utilizadas)
- [Estrutura do Projeto](#-estrutura-do-projeto)
- [Como Executar Localmente](#-como-executar-localmente)
- [Deploy & Build](#-deploy--build)
- [Autor](#-autor)

---

## 🎨 Visão Geral

O **DevAmorim** foi construído com foco em performance, acessibilidade e design responsivo. A interface é dividida em seções modulares para proporcionar uma navegação fluida ao visitante:

- **Hero Section:** Apresentação inicial e síntese do meu perfil profissional.
- **Projetos:** Exposição dos meus principais trabalhos com links diretos, repositórios e tecnologias utilizadas.
- **Contato:** Canais diretos para conexões profissionais e envio de mensagens.

---

## 🛠️ Tecnologias Utilizadas

- **Core:** [Vue 3](https://vuejs.org/) (Composition API)
- **Bundler / Build Tool:** [Vite](https://vitejs.dev/)
- **Estilização:** [Tailwind CSS](https://tailwindcss.com/)
- **Ícones & UI:** Feather / Lucide / FontAwesome
- **Hospedagem & CI/CD:** [Vercel](https://vercel.com) / [Netlify](https://netlify.com)

---

## 📂 Estrutura do Projeto

```text
devamorim/
├── public/                 # Arquivos estáticos (favicon, imagens, assets)
├── src/
│   ├── assets/
│   │   └── css/
│   │       └── tailwind.css # Configuração principal de estilos do Tailwind
│   ├── components/
│   │   ├── projectcard.vue  # Componente reutilizável para exibição de projetos
│   │   └── footer.vue       # Rodapé do site com redes sociais
│   ├── sections/
│   │   ├── hero.vue         # Seção de apresentação principal
│   │   ├── projects.vue     # Seção com a listagem de projetos
│   │   └── contact.vue      # Seção com informações e formulário de contato
│   ├── App.vue              # Componente raiz da aplicação
│   └── main.js              # Ponto de entrada (initialization do Vue)
├── index.html               # Documento HTML principal
├── tailwind.config.js       # Configurações do Tailwind CSS
├── vite.config.js           # Configurações do Vite
└── package.json             # Dependências e scripts do projeto
