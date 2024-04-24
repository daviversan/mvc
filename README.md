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
O elemento Admin se refere ao administrador do projeto. Esse tipo de usuário tem acesso aos dados coletados pela solução web e possui autorização para editar o formulário, alterar informações da landing page, excluir e adicionar usuários, entre outras funções administrativas.
- Dashboard: Página que contém gráficos, dados relevantes e informações catalogadas acerca das interações dos usuários com o site
- Configurações: Seção que permite ao administrador configurar as demais áreas do site conforme suas preferências
- ID: Código de identificação único para cada administrador
- Senha: Senha de administrador única usada para se cadastrar ou logar no site
## User
User é uma classe de usuário pdrão que não possui as autorizações do Admin, podendo interagir com o site sem alterar seus elementos e funcionalidades
- Nome: Nome de usuário
- Endereço: Endereço residencial
- Email: Email usado para realizar a autenticação da conta
- ID: Código de indentificação único para cada usuário padrão
- Senha: Senha de usuário única usada para se cadastrar ou logar no site

# Controladores (Controllers):
- Liste os controladores do seu projeto e suas responsabilidades.
- Descreva as ações (methods) de cada controlador e seus parâmetros de entrada e saída.
- Explique como os controladores interagem com os modelos e views.
## Admin
Controladores exclusivos aos usuários classificados como Admin
- CRUD: Acrônimo para Create(C), Read(R), Update(U), Delete(D). Permite que o administrador realize essas funções em relação aos formulários e gerenciamento de usuários;
- Login / Logout: Permite que o usuário Admin possar entrar ou sair de sua conta
- Cadastro: Permite que o Admin se cadastre no site
## User
Controladores específicos ao User
- Read-only: Permite que o usuário interaja com o site, sem modificar seus elementos e funcionalidades
- Login / Logout: Permite que o usuário entre ou saia de sua conta
- Interação: Representa as diversas interações permitidas ao usuário de realizar com os elementos do site
- Resposta ao forms: Permite que o usuário registre suas respostas no campo especificado dentro do forms
- Cadastro: Permite que o usuário se cadastre no site
## Elements
Controladores específicos aos elementos do site
- Renderização: Permite que elementos sejam renderizados na tela
- Evento on-click: Indica todas as ações que ocorrem após o usuário clicar em determinado elemento
- Autenticação: Ferramentas que verificam a conta do usuário e conferem sua autenticação
## Forms
Controladores específicos ao forms
- Selecionar: Indica a ação de selecionar os elementos do forms: Botão de iniciar, seguir ou retroceder para alguma pergunta, selecionar a área de respostas etc.
- Deletar: Função que permite o usuário deletar sua resposta ao formulário. No caso do Admin também é possível deletar a própria questão do forms
- Salvar: Permite o salvamento automático das respostas do forms. Assim, caso o usuário perca a conexão com a internet ou saia do site por algum motivo ele poderá acessar a página novamente de onde parou
- Transição: Se refere a todas as transições de página que ocorrem dentro da solução web

# Views (Views):
- Liste as views do seu projeto e sua função.
## Header
Seção superior que contém os principais elementos do site
- Logo: Primeiro elemento do Header em formato de imagem
- Perfil: Ícone que redireciona o usuário a sua página de perfil
- Navbar: Barra de pesquisa que permite o usuário acessar conteúdos específicos da página mais facilmente
## Homepage
Página principal do site
- H1: Título com o nome do projeto
- Text: Texto que detalha em mais informaçõs as propostas da solução
- Images: Imagens que fazem referência ao projeto e compõe a identidade visual do site
- Botão: Botão que direciona o usuário ao formulário
## Footer
Última seção do site que contém uma síntese dos conteúdos disponíveis
- Contatos: Links para redes sociais do INSPA, números para contato e redes sociais dos desenvolvedores
- Links: Redirecionamento para websites relacionados, como do INSPA e outras páginas externas que possam ser úteis ao usuário
- Copyright e certificados de segurança: Certificado de segurança SSL; Marca de registro e direitos autorais; Documentos que atestem conformidade com a LGPD etc.
## Forms
Página do formulário
- Blocos de texto: Seção que contém as perguntas do formulário
- Botões: Botões para 'Iniciar', 'Retornar uma pergunta', 'Ir para próxima pergunta', 'Entregar formulário'
- Barra de progresso: Barra localizada na parte inferior do formulário que é gradativamente preenchida conforme o usuário responde as perguntas do formulário
- Caixas de texto: Seção em que o usuário poderá digitar suas respostas ou selecionar as alternativas corretas
### Infraestrutura:

- Descreva os componentes de infraestrutura do seu projeto, como bancos de dados, APIs externas e outras dependências.
- Explique como a infraestrutura se integra à arquitetura MVC.


### Justifique as escolhas feitas e como elas impactam o projeto.
#### Implicações da Arquitetura:
Descreva as implicações da arquitetura em termos de escalabilidade, manutenção, testabilidade e outros aspectos importantes.


