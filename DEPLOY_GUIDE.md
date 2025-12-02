# 🚀 GUIA DE DEPLOY - LYNN PORTFOLIO

## Passo a Passo Completo para Deploy no Netlify via GitHub

### 📋 PRÉ-REQUISITOS

Antes de começar, certifique-se de ter:
- ✅ Conta no GitHub (gratuita) - https://github.com/signup
- ✅ Conta no Netlify (gratuita) - https://app.netlify.com/signup
- ✅ Git instalado no computador - https://git-scm.com/downloads
- ✅ Editor de código (VS Code recomendado) - https://code.visualstudio.com/

---

## 🎯 MÉTODO 1: DEPLOY COMPLETO (GitHub + Netlify)

### ETAPA 1: Preparar os Arquivos

1. **Organizar a estrutura do projeto**

Crie a seguinte estrutura de pastas:

```
lynn-portfolio/
├── index.html
├── styles.css
├── script.js
├── README.md
├── netlify.toml
├── .gitignore
└── images/
    ├── modelo1_MariaPaula.jpg
    ├── modelo2_MariaPaula.jpg
    ├── modelo3_MariaPaula.jpg
    └── modelo4_MariaPaula.jpg
```

2. **Copiar as imagens**
   - Crie a pasta `images/` dentro do projeto
   - Copie as 4 imagens do projeto para esta pasta
   - Renomeie se necessário para manter a consistência

3. **Personalizar informações**
   - Abra `index.html` no editor
   - Substitua:
     - Email placeholder por email real
     - Instagram handle (@lynnartes) pelo Instagram real
     - Link do Google Drive (se tiver)

---

### ETAPA 2: Criar Repositório no GitHub

#### 2.1 Via Interface Web (Mais Fácil)

1. Acesse https://github.com/new
2. Preencha:
   - **Repository name**: `lynn-portfolio`
   - **Description**: "Portfólio profissional de street art - LYNN"
   - **Public** (para usar Netlify gratuitamente)
   - ✅ Marque "Add a README file" (apenas se não tiver README)
3. Clique em **"Create repository"**

#### 2.2 Fazer Upload dos Arquivos

**Opção A - Via Interface (Iniciantes):**

1. No repositório criado, clique em "uploading an existing file"
2. Arraste TODOS os arquivos do projeto (exceto a pasta images por enquanto)
3. Escreva uma mensagem: "Initial commit - LYNN Portfolio"
4. Clique em "Commit changes"
5. Repita para a pasta images (crie a pasta primeiro se necessário)

**Opção B - Via Terminal (Avançado):**

```bash
# 1. Navegue até a pasta do projeto
cd caminho/para/lynn-portfolio

# 2. Inicialize o Git
git init

# 3. Adicione todos os arquivos
git add .

# 4. Faça o primeiro commit
git commit -m "🎨 Initial commit - LYNN Portfolio"

# 5. Conecte ao repositório remoto (substitua SEU_USUARIO)
git remote add origin https://github.com/SEU_USUARIO/lynn-portfolio.git

# 6. Renomeie a branch para main
git branch -M main

# 7. Faça o push
git push -u origin main
```

---

### ETAPA 3: Conectar GitHub ao Netlify

1. **Acessar Netlify**
   - Vá para https://app.netlify.com
   - Faça login (ou crie conta se ainda não tiver)

2. **Importar Projeto**
   - Clique no botão **"Add new site"**
   - Selecione **"Import an existing project"**

3. **Conectar GitHub**
   - Clique em **"Deploy with GitHub"**
   - Autorize o Netlify a acessar sua conta GitHub
   - Se pedido, autorize acesso aos repositórios

4. **Selecionar Repositório**
   - Procure por `lynn-portfolio` na lista
   - Clique no repositório

5. **Configurar Build Settings**
   ```
   Branch to deploy: main
   Build command: (deixe VAZIO)
   Publish directory: . (ponto) ou / (barra)
   ```

6. **Deploy Site**
   - Clique em **"Deploy [nome-do-seu-site]"**
   - Aguarde 1-3 minutos para o deploy completar

7. **Seu site está no ar! 🎉**
   - URL gerada: `random-name-123456.netlify.app`

---

### ETAPA 4: Personalizar Domínio

1. **Acessar Domain Settings**
   - No painel do Netlify, vá em **"Domain settings"**
   
2. **Alterar Nome do Site**
   - Clique em **"Options"** > **"Edit site name"**
   - Digite um nome único: `lynnart`, `lynn-streetart`, etc.
   - Clique em **"Save"**
   - Novo URL: `lynnart.netlify.app`

3. **Domínio Personalizado (Opcional - Pago)**
   - Clique em **"Add custom domain"**
   - Digite seu domínio (ex: `lynnart.com`)
   - Siga as instruções de configuração DNS
   - Custo: ~R$50-100/ano

---

## 🔄 COMO ATUALIZAR O SITE

### Método Simples (Via GitHub Web)

1. Acesse seu repositório no GitHub
2. Navegue até o arquivo que quer editar
3. Clique no ícone de lápis (Edit)
4. Faça as alterações
5. Clique em "Commit changes"
6. **Netlify fará deploy automático em 1-2 minutos!**

### Método Avançado (Via Git)

```bash
# 1. Faça alterações nos arquivos localmente

# 2. Adicione as mudanças
git add .

# 3. Commit com mensagem descritiva
git commit -m "✨ Adicionada nova obra na galeria"

# 4. Push para GitHub
git push

# Deploy automático acontece em 1-2 minutos!
```

---

## 🎯 MÉTODO 2: DEPLOY RÁPIDO (Drag & Drop)

### Para quem quer testar rapidamente

1. **Preparar Arquivos**
   - Coloque todos os arquivos em uma pasta
   - Certifique-se que `index.html` está na raiz

2. **Acessar Netlify Drop**
   - Vá para https://app.netlify.com/drop

3. **Arrastar Pasta**
   - Arraste a pasta inteira do projeto
   - Aguarde upload completar

4. **Site no Ar!**
   - URL gerado automaticamente
   - Sem deploy contínuo (precisa fazer upload novamente para atualizar)

⚠️ **Limitação**: Cada atualização requer novo upload manual

---

## 🔗 INTEGRAÇÃO COM GOOGLE DRIVE

### Configurar Link para Galeria Completa

1. **Criar Pasta no Google Drive**
   - Faça upload de todas as suas obras
   - Organize em uma pasta

2. **Tornar Público**
   - Clique com botão direito na pasta
   - **"Compartilhar"** > **"Alterar"**
   - Selecione **"Qualquer pessoa com o link"**
   - Copie o link

3. **Extrair ID da Pasta**
   - URL do Google Drive: 
   ```
   https://drive.google.com/drive/folders/1abc123DEF456ghi789
   ```
   - O ID é: `1abc123DEF456ghi789`

4. **Atualizar no Site**
   - Abra `index.html`
   - Encontre: `YOUR_FOLDER_ID`
   - Substitua pelo ID real:
   ```html
   <a href="https://drive.google.com/drive/folders/1abc123DEF456ghi789">
   ```

---

## 📧 CONFIGURAR FORMULÁRIO DE CONTATO

### Opção 1: Netlify Forms (GRÁTIS - Recomendado)

1. **Editar HTML**
   
   Abra `index.html` e modifique o `<form>`:
   
   ```html
   <form name="contact" method="POST" data-netlify="true" data-netlify-honeypot="bot-field">
       <input type="hidden" name="form-name" value="contact">
       <!-- resto do formulário -->
   </form>
   ```

2. **Fazer Deploy**
   - Commit e push das mudanças
   - Aguarde deploy

3. **Acessar Mensagens**
   - Netlify Dashboard > Forms
   - Todas as mensagens aparecerão aqui

4. **Configurar Notificações**
   - Forms > Notifications
   - Adicione seu email
   - Receba alertas de novas mensagens

### Opção 2: FormSpree (GRÁTIS - Alternativa)

1. **Criar Conta**
   - Acesse https://formspree.io
   - Crie conta gratuita

2. **Criar Form**
   - New Form
   - Copie o endpoint: `https://formspree.io/f/xyzabc123`

3. **Atualizar HTML**
   ```html
   <form action="https://formspree.io/f/xyzabc123" method="POST">
   ```

---

## ✅ CHECKLIST FINAL

Antes de considerar completo, verifique:

- [ ] Site carregando corretamente no Netlify
- [ ] Todas as imagens aparecem
- [ ] Links do menu funcionam
- [ ] Filtros da galeria funcionam
- [ ] Formulário de contato configurado
- [ ] Links de redes sociais corretos
- [ ] Email atualizado
- [ ] Instagram atualizado
- [ ] Google Drive linkado (se aplicável)
- [ ] Site responsivo em mobile
- [ ] Domínio personalizado (se comprou)

---

## 🆘 RESOLUÇÃO DE PROBLEMAS

### Problema: Imagens não aparecem

**Solução:**
- Verifique se as imagens estão na pasta `images/`
- Confirme os caminhos no HTML:
  ```html
  <img src="images/modelo1_MariaPaula.jpg">
  ```
- As imagens devem estar commitadas no Git

### Problema: Deploy falhou no Netlify

**Solução:**
- Verifique se `index.html` está na raiz do projeto
- Confirme que não há erros de sintaxe no HTML
- Veja os logs de deploy no Netlify

### Problema: Formulário não envia

**Solução:**
- Certifique-se de adicionar `data-netlify="true"` no form
- Faça novo deploy após alterar
- Teste após 5 minutos do deploy

### Problema: Site lento

**Solução:**
- Otimize imagens (use TinyPNG.com)
- Mantenha imagens abaixo de 500KB cada
- Converta para WebP se possível

---

## 📞 SUPORTE

Se tiver problemas:

1. **Documentação Netlify**: https://docs.netlify.com
2. **Documentação GitHub**: https://docs.github.com
3. **Fórum Netlify**: https://answers.netlify.com
4. **Stack Overflow**: https://stackoverflow.com

---

## 🎉 PRÓXIMOS PASSOS

Após o site estar no ar:

1. ✅ Compartilhe nas redes sociais
2. ✅ Adicione o link na bio do Instagram
3. ✅ Monitore acessos via Netlify Analytics
4. ✅ Continue adicionando novos trabalhos
5. ✅ Solicite feedback e depoimentos
6. ✅ Considere SEO e marketing digital

---

<div align="center">

### 🎨 Sucesso no seu portfólio! 🚀

**Dúvidas? Revise este guia ou consulte a documentação oficial.**

</div>
