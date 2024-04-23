# mvc

# Template Readme para Arquitetura MVC em Markdown
- Nome do Projeto: MVC Design
- Descrição: Diagrama no formato de arquitetura MVC que explica o funcionamento dos componentes da solução web a ser desenvolvida para o parceiro de projeto INSPA
- Arquitetura: MVC (Model-View-Controller)
- Ferramenta de Diagramação: Draw.io

# Modelos (Models):
- Descreva as entidades do seu projeto e seus atributos.
- Explique as relações entre as entidades.
## Admin
- Dashboard
- Configurações
- ID
## User
- Nome
- Endereço
- Email
- ID

# Controladores (Controllers):
- Liste os controladores do seu projeto e suas responsabilidades.
- Descreva as ações (methods) de cada controlador e seus parâmetros de entrada e saída.
- Explique como os controladores interagem com os modelos e views.
## Admin
- CRUD
- Login / Logout
## User
- Read-only
- Login / Logout
- Interação
- Resposta ao forms
## Elements
- Renderização
- Evento on-click
- Autenticação
## Forms
- Selecionar
- Deletar
- Salvar
- Transição

# Views (Views):
- Liste as views do seu projeto e sua função.
## Header
- Logo
- Perfil
- Navbar
## Homepage
- H1
- Text
- Images
- Botão
## Footer
- Contatos
- Links
- Copyright e certificados de segurança
## Forms
- Blocos de texto
- Botões
- Barra de progresso
- Caixas de texto  
### Infraestrutura:

- Descreva os componentes de infraestrutura do seu projeto, como bancos de dados, APIs externas e outras dependências.
- Explique como a infraestrutura se integra à arquitetura MVC.


### Justifique as escolhas feitas e como elas impactam o projeto.
#### Implicações da Arquitetura:
Descreva as implicações da arquitetura em termos de escalabilidade, manutenção, testabilidade e outros aspectos importantes.


