# mvc

# Template Readme para Arquitetura MVC em Markdown
- Nome do Projeto: MVC Design
- Descrição: Diagrama no formato de arquitetura MVC que explica o funcionamento dos componentes da solução web a ser desenvolvida para o parceiro de projeto INSPA
- Arquitetura: MVC (Model-View-Controller)
- Ferramenta de Diagramação: Draw.io

#Imagem do template:
<img src="URL_da_Imagem" alt="Texto Alternativo">

# Modelos (Models):
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
## Operation
Controladores específicos às operações dos elementos do site
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
## Header
Seção superior que contém os principais elementos do site
- Logo: Primeiro elemento do Header em formato de imagem
- Perfil: Ícone que redireciona o usuário a sua página de perfil
- Navbar: Barra de pesquisa que permite o usuário acessar conteúdos específicos da página mais facilmente
## Homepage
Página principal do site
- H1: Título com o nome do projeto
- Text: Texto que detalha em mais informações as propostas da solução
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
## Infraestrutura:
###  Banco de dados:
Como banco de dados foi utilizado o PostgreSQL, uma solução open source relacional, selecionada para o projeto por oferecer uma maior organização e categorização dos dados em formato de tabelas, facilitando o acesso aos administradores e a visualização de informações essenciais através dos dashboards.
A Rest API foi escolhida pois permite a integração multiplataforma, como dispositivos mobile, e diferentes sistemas operacionais, fatores fundamentais para o escopo do projeto. Além disso, a Rest API é reconhecida por facilitar a comunicação cliente-servidor, podendo ser usada para expor funcionalidades e dados de um sistema como um serviço web, permitindo que outros sistemas se comuniquem e interajam com ele de forma programática.

### Implicações da Arquitetura:
A Arquitetura MVC descrita representa uma solução versátil que permite a visualização de todos os componentes da solução web e descreve como elas se comunicam entre si. Por conta desses atributos, se trata de uma ferramente altamente escalável, podendo ser utilizada de forma síncrona por todos os membros do grupo enquanto trabalham em diferentes partes do projeto e componentes da arquitetura. Os elementos da lista a seguir indicam um panorama geral do fluxo de dados representado pela arquitetura

1. O usuário se conecta ao servidor que hospeda o site através de um browser (cliente)
2. A seção 'Views' renderiza os elementos:
-   Header, que contém os principais acessos do site;
-   Homepage que representa a página principal com uma 'Call to action' para o usuário preencher o formulário';
-   Footer, com informações de contato e certificados de segurança;
-   Forms, que consiste na página do formulário;
3. A seção Controllers é responsável por receber as requisições da seção 'Views', gerenciando as funções desempenhadas por cada elemento
4. A seção 'Models' conecta os elementos da 'Views' e as requisições efetuadas nos 'Controllers' ao banco de dados, separado em caixas Admin e User.
5. O banco de dados PostgreSQL se conecta com a Rest API, transferindo de forma visual e organizada as requisições dos usuários, transferindo essas informações de volta ao cliente de forma responsível e adaptativa para qualquer plataforma e sistema operacional
