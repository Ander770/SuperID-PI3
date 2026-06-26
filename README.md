## Sobre o projeto

SuperID é um aplicativo Android de gerenciamento de senhas desenvolvido como Projeto Integrador do 3º semestre na PUC-Campinas. O app permite que o usuário armazene suas senhas em categorias (Sites Web, Aplicativos, Teclados Físicos, Códigos), com autenticação via Firebase Auth e persistência no Firestore. O app conta com suporte a tema claro e escuro seguindo o sistema do dispositivo.

> Projeto desenvolvido em grupo. Stack: Kotlin · Jetpack Compose · Firebase Auth · Firestore · Material3

---

## 🙋 Minha contribuição

### 🏠 HomeActivity — Tela Principal
- Criei a `HomeActivity` do zero, estruturando o layout com Jetpack Compose
- Implementei a grade de categorias em formato 2x2 usando `LazyVerticalGrid`, onde cada categoria é exibida como um `Card` clicável com ícone e nome
- Defini a paleta de cores dourado/preto do app (`darkColorScheme` com cor primária `#D4AF37`) e depois refatorei para usar o `MaterialTheme` centralizado
- Adicionei o logo do SuperID no topo da tela como cabeçalho, o botão flutuante (FAB) de adicionar senha, e a imagem de fundo com transparência
- Implementei a tela de detalhe por categoria (`CategoryDetailScreen`) com navegação via `NavController`, listagem de senhas do Firestore em cards e FAB para adicionar nova senha com dialog

### 🔐 SignInActivity — Tela de Login
- Refatorei o layout da tela de login para um design mais polido: logo do app centralizado, campos de email e senha com `RoundedCornerShape`, botão de entrar estilizado, e links de "Esqueci minha senha" e "Criar conta"
- Adicionei suporte a tema claro/escuro com cores adaptadas via `isSystemInDarkTheme()`
- Implementei o redirecionamento automático para a `HomeActivity` após login bem-sucedido via Firebase Auth, passando o contexto como parâmetro para a função de login

### 🗂️ AddCategoryActivity — Tela de Adicionar Categoria
- Criei a `AddCategoryActivity` e implementei o layout completo: campo de texto para nome da categoria, botão de confirmar estilizado em dourado, ícone de voltar no canto superior esquerdo e imagem de fundo
- Conectei a navegação da `HomeActivity` para essa tela ao clicar no card "Adicionar Categoria"
- Integrei ao `SuperIDTheme` para respeitar o tema claro/escuro do sistema

### 🎨 Tema e Padronização Visual
- Defini e centralizei toda a paleta de cores do app em `Color.kt` (tons dourados `BotaoDourado`, fundos claros e escuros) e `Theme.kt` (esquemas `DarkColorScheme` e `LightColorScheme`)
- Criei o composable `BackgroundImage()` que troca automaticamente a imagem de fundo entre claro e escuro conforme o tema do sistema, reutilizando esse componente em todas as telas
- Substituí cores hardcoded (`Color(0xFFFFC107)`, `Color(0xFF1E1E1E)`) por variáveis do `MaterialTheme.colorScheme` em todo o projeto, garantindo consistência visual
- Adicionei imagens de fundo para os temas claro (`fundoclarocerto.jpg`) e escuro (`fundoescurocerto.jpg`)

### 🔧 Configuração e Infraestrutura
- Registrei as Activities (`HomeActivity`, `AddCategoryActivity`) no `AndroidManifest.xml`
- Adicionei as dependências `navigation-compose` e `material3` ao `build.gradle.kts` e `libs.versions.toml`
- Atualizei versões do AGP e Gradle Wrapper ao longo do desenvolvimento

---

## 🛠️ Tecnologias utilizadas

![Kotlin](https://img.shields.io/badge/Kotlin-7F52FF?style=flat&logo=kotlin&logoColor=white)
![Android](https://img.shields.io/badge/Android-3DDC84?style=flat&logo=android&logoColor=white)
![Jetpack Compose](https://img.shields.io/badge/Jetpack_Compose-4285F4?style=flat&logo=jetpackcompose&logoColor=white)
![Firebase](https://img.shields.io/badge/Firebase-FFCA28?style=flat&logo=firebase&logoColor=black)
![Material3](https://img.shields.io/badge/Material_3-757575?style=flat&logo=material-design&logoColor=white)

<!-- Informações originais do repositório abaixo -->

---

# PROJETO-INTEGRADOR-III
Repositório do Projeto Integrador do 3° semestre do curso de Engenharia de Software 2025 PUC Campinas. 
Grupo: 
- [Anderson Lucas do Nascimento Gondim](https://github.com/Ander770); 
- [Daniel Henrique Inoue Jange](https://github.com/djange2);  
- [Luca Diniz Santos](https://github.com/Luca-DS); 
- [William Kenzo Nakao](https://github.com/WilliamPuc01);
#
# Instruções de Uso
- Clone o repositório
- Entre em "SuperID/app/release/app-release.apk" para baixar o apk do aplicativo android
- Entrar na pasta "SuperID_web/frontend/pages/login SuperID" e abrir a página na web
