# 🎯 DESAFIO FINAL: Portfólio Pessoal Multi-Páginas com Docker

## 🎯 Objetivo
Criar um projeto completo usando**Dockerfile** e **Docker Compose** para orquestrar múltiplos serviços web interconectados. Você aprenderá sobre volumes, dependências entre containers e políticas de restart.

## 📋 O que você vai aprender
- ✅ Estruturação de projetos multi-container
- ✅ Configuração de Docker Compose
- ✅ Gerenciamento de dependências entre serviços
- ✅ Políticas de restart automático

## 🚀 Desafio: Criar seu Portfólio Pessoal

### **📁 Passo 1: Estruturação do Projeto**
Você deve criar uma estrutura organizada para seu projeto:
- Crie uma pasta principal chamada `meu-portfolio`
- Dentro dela, crie 3 subpastas: `home`, `blog` e `portfolio`
- Cada pasta representará um serviço diferente do seu portfólio

### **🏠 Passo 2: Desenvolver a Página Principal (Homepage)**
Crie um arquivo `index.html` dentro da pasta `home` com os seguintes requisitos:

**Conteúdo obrigatório:**
- Título da página: "Minha Homepage" (deve rodar na `http://localhost:8080`)
- Uma mensagem de boas-vindas personalizada com seu nome
- Descrição sobre você e o projeto
- Links de navegação para as outras páginas (blog e portfólio)
- Links devem apontar para `http://localhost:8081` (blog) e `http://localhost:8082` (portfólio)

### **📝 Passo 3: Desenvolver a Página do Blog**
Crie um arquivo `index.html` dentro da pasta `blog` que contenha:

**Estrutura necessária:**
- Título da página: "Meu Blog" ou similar
- 
### **💼 Passo 4: Desenvolver a Página do Portfólio**
Crie um arquivo `index.html` dentro da pasta `portfolio` com:

**Conteúdo essencial:**
- Título da página: "Meu Portfólio" ou "Meus Projetos"

### **🐳 Passo 5: Configurar Docker Compose**
Crie um arquivo `docker-compose.yaml` na raiz do projeto com estas especificações:

**Serviços necessários:**
1. **Homepage Service:**
2. **Blog Service:**
3. **Portfolio Service:**

**Configurações adicionais:**
- Crie a depdência entre a homepage, blog e portfloio
- Crie politicas de restart para quando um container cair

## 🎯 Desafios Extras

### **🌟 Desafio 1: Personalização**
- [ ] Cria a sua própria imagem do docker que irá conter o html dentro dela, faça isso para apenas um dos sites, os outros deve ter o mapeamento o html para dentro do container
