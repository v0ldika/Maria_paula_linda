# 🎨 LYNN - Street Art Portfolio

> Portfólio profissional de street art e graffiti com design moderno, responsivo e integração com Google Drive.

![LYNN Street Art](https://img.shields.io/badge/LYNN-Street%20Artist-FF1493?style=for-the-badge)
![Status](https://img.shields.io/badge/Status-Live-00CED1?style=for-the-badge)
![License](https://img.shields.io/badge/License-MIT-9370DB?style=for-the-badge)

## 🌟 Características

- ✨ Design moderno e vibrante inspirado na cultura street art
- 🎭 Galeria de projetos com sistema de filtros
- 📱 100% Responsivo (Mobile, Tablet, Desktop)
- ⚡ Performance otimizada
- 🔍 SEO friendly
- 🌈 Animações suaves e efeitos visuais
- 📧 Formulário de contato funcional
- 🔗 Integração com Google Drive
- 🚀 Deploy automático via Netlify

## 🛠️ Tecnologias Utilizadas

- **HTML5** - Estrutura semântica
- **CSS3** - Estilização avançada com Grid e Flexbox
- **JavaScript (Vanilla)** - Interatividade e animações
- **Google Fonts** - Tipografia personalizada
- **Netlify** - Hospedagem e deploy contínuo
- **GitHub** - Controle de versão

## 📁 Estrutura do Projeto

```
lynn-portfolio/
│
├── index.html          # Página principal
├── styles.css          # Estilos globais
├── script.js           # Funcionalidades JavaScript
├── README.md           # Este arquivo
├── netlify.toml        # Configurações Netlify
├── .gitignore          # Arquivos ignorados pelo Git
│
├── images/             # Pasta para imagens do projeto
│   ├── modelo1_MariaPaula.jpg
│   ├── modelo2_MariaPaula.jpg
│   ├── modelo3_MariaPaula.jpg
│   └── modelo4_MariaPaula.jpg
│
└── assets/             # Recursos adicionais
    ├── icons/
    └── fonts/
```

## 🚀 Como Usar

### Pré-requisitos

- Conta no [GitHub](https://github.com)
- Conta no [Netlify](https://netlify.com)
- Editor de código (VS Code recomendado)
- Git instalado

### Instalação Local

1. **Clone o repositório**
```bash
git clone https://github.com/seu-usuario/lynn-portfolio.git
cd lynn-portfolio
```

2. **Abra o projeto**
```bash
# Abra no VS Code
code .

# Ou use o Live Server do VS Code
# Clique com botão direito em index.html > Open with Live Server
```

3. **Visualize localmente**
```
http://localhost:5500
```

### Deploy no Netlify via GitHub

#### Opção 1: Deploy Automático (Recomendado)

1. **Criar repositório no GitHub**
   - Acesse https://github.com/new
   - Nome: `lynn-portfolio`
   - Descrição: "LYNN Street Art Portfolio"
   - Público ou Privado (sua escolha)
   - Crie o repositório

2. **Fazer push do código**
```bash
# Inicializar Git (se necessário)
git init

# Adicionar arquivos
git add .

# Commit
git commit -m "🎨 Initial commit - LYNN Portfolio"

# Conectar ao repositório remoto
git remote add origin https://github.com/seu-usuario/lynn-portfolio.git

# Push para GitHub
git branch -M main
git push -u origin main
```

3. **Conectar com Netlify**
   - Acesse https://app.netlify.com
   - Clique em "Add new site" > "Import an existing project"
   - Escolha "Deploy with GitHub"
   - Autorize o Netlify a acessar seu GitHub
   - Selecione o repositório `lynn-portfolio`
   - Configure:
     - Branch to deploy: `main`
     - Build command: (deixe vazio)
     - Publish directory: `/` ou `.`
   - Clique em "Deploy site"

4. **Configurar domínio personalizado (Opcional)**
   - Em Site settings > Domain management
   - Add custom domain
   - Exemplo: `lynnart.netlify.app`

#### Opção 2: Deploy Drag & Drop

1. Acesse https://app.netlify.com/drop
2. Arraste a pasta do projeto
3. Aguarde o upload e deploy automático

## 🔧 Personalização

### Atualizar Informações Pessoais

Edite o arquivo `index.html`:

```html
<!-- Email -->
<a href="mailto:SEU-EMAIL@gmail.com">SEU-EMAIL@gmail.com</a>

<!-- Instagram -->
<a href="https://instagram.com/SEU_INSTAGRAM">@SEU_INSTAGRAM</a>

<!-- Localização -->
<p>Sua Cidade, Brasil</p>
```

### Integração com Google Drive

1. **Criar pasta pública no Google Drive**
   - Crie uma pasta com suas obras
   - Clique com botão direito > Compartilhar
   - Altere para "Qualquer pessoa com o link"
   - Copie o ID da pasta (está na URL)

2. **Atualizar o código**

Em `index.html`, linha do botão "VIEW FULL GALLERY":
```html
<a href="https://drive.google.com/drive/folders/SEU_FOLDER_ID" target="_blank">
```

3. **Para integração avançada (API do Google Drive)**
   - Consulte o arquivo `script.js`
   - Função `loadGoogleDriveImages()`
   - Siga a documentação: https://developers.google.com/drive/api/v3/quickstart/js

### Cores do Tema

Edite as variáveis CSS em `styles.css`:

```css
:root {
    --primary-pink: #FF1493;      /* Rosa principal */
    --primary-purple: #9370DB;    /* Roxo */
    --primary-cyan: #00CED1;      /* Ciano */
    --primary-green: #32CD32;     /* Verde */
    --primary-yellow: #FFD700;    /* Amarelo */
    /* ... */
}
```

### Adicionar Novas Obras

Em `index.html`, adicione dentro de `.gallery-grid`:

```html
<div class="gallery-item" data-category="murals characters">
    <div class="gallery-image">
        <img src="images/nova-obra.jpg" alt="Descrição">
        <div class="overlay">
            <div class="overlay-content">
                <h3>TÍTULO DA OBRA</h3>
                <p>Descrição • Ano</p>
                <span class="view-more">+</span>
            </div>
        </div>
    </div>
</div>
```

## 📧 Configurar Formulário de Contato

### Opção 1: Netlify Forms (Gratuito)

1. Adicione ao `<form>` em `index.html`:
```html
<form name="contact" method="POST" data-netlify="true">
```

2. Visualize mensagens em: Netlify Dashboard > Forms

### Opção 2: FormSpree

1. Acesse https://formspree.io
2. Crie uma conta gratuita
3. Obtenha seu endpoint
4. Atualize o formulário:
```html
<form action="https://formspree.io/f/SEU_ID" method="POST">
```

### Opção 3: EmailJS

1. Acesse https://www.emailjs.com
2. Configure seu serviço de email
3. Siga a documentação para integrar

## 🎨 Adicionar Novas Seções

### Exemplo: Seção de Depoimentos

```html
<section class="testimonials-section">
    <div class="container">
        <h2 class="section-title">O QUE DIZEM</h2>
        <div class="testimonials-grid">
            <!-- Adicione depoimentos aqui -->
        </div>
    </div>
</section>
```

## 📱 Redes Sociais

Atualize os links em `index.html` e `styles.css`:

- Instagram: @lynnartes
- TikTok: @lynnartes (adicionar se necessário)
- YouTube: canal da artista (adicionar se necessário)

## 🔄 Atualizações Futuras

Recursos planejados:
- [ ] Blog/News section
- [ ] Loja online (prints, merchandise)
- [ ] Galeria 3D interativa
- [ ] Modo dark/light toggle
- [ ] Múltiplos idiomas (PT/EN/ES)
- [ ] Integração com Instagram API
- [ ] Sistema de reserva para murais

## 🐛 Problemas Conhecidos

- O formulário de contato precisa de configuração adicional
- Google Drive API requer autenticação para funcionalidades avançadas
- Alguns navegadores antigos podem não suportar todas as animações

## 📄 Licença

Este projeto está sob a licença MIT. Veja o arquivo `LICENSE` para mais detalhes.

## 👤 Autor

**LYNN**
- Street Artist & Muralist
- Location: Rio de Janeiro, Brasil
- Instagram: [@lynnartes](https://instagram.com/lynnartes)
- Email: lynn.streetart@gmail.com

## 🙏 Agradecimentos

- Inspiração: Cultura street art brasileira
- Fontes: Google Fonts (Permanent Marker, Urbanist)
- Hospedagem: Netlify
- Controle de versão: GitHub

---

<div align="center">

### 🎨 Feito com 💖 para a cultura street art

**[⬆ Voltar ao topo](#-lynn---street-art-portfolio)**

</div>
```

Substitua:
- `SEU_FOLDER_ID` pelo ID real da pasta do Google Drive
- `SEU-EMAIL` pelo email real
- `SEU_INSTAGRAM` pelo handle do Instagram
- URLs e informações pessoais conforme necessário
