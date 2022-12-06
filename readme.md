# Projeto FullStack Hotel  - Escola T

Boas vindas!

Convidamos você a participar em time, do desenvolvimento de um sistema de hotelaria onde as reservas são feitas online. Por se tratar de uma demanda FullStack, o projeto envolve o front-end e o back-end. 

## Tipo de Usuário

O sistema contempla dois tipos de usuário:

 - Usuário público que efetua reservas das acomodações.
 - Usuário administrativo que monitora o checkin, checkout e a disponibilidade dos apartamentos. 


## Features da aplicação

O desenvolvimento front-end consiste em :

  - Criar os documentos HTML em blocos que possam ser convertidos em componentes
  - Aplicar o CSS para diagramar, organizar e tematizar as telas da interface
  - Criar funcionalidades usando a linguagem Javascript
  - Utilizar um pré-procesador CSS
  - Persistir os dados em `localStorage`
  - Aplicar um framework reativo para lidar com os blocos de conteúdo, gerar as rotas do front-end e renderizar os dados do back-end
  

### Tela Login

- Acesso mediante usuário cadastrado
- Link 'esqueceu sua senha' com reset de senha. O teste de email pode ser feito com MailHog.
- Notificação de senha forte (Uppercase/Lowercase/Números/Caracteres Especiais)
- Opcional: envio de código de verficação.


### Tela Home

- Exibe saudação ao usuário autenticado e opção de logout (caso acesso sem autenticação apenas imprimir o botão Cadastre-se)
- Sobre o nosso Hotel, resumo que direciona para a tela 'Sobre'.
- Exibe 3 (três) cards com as acomodações mais poulares
- Cada card é um link que direciona para os detalhes da respectiva acomodação.
- Botão 'Conheça mais sobre nossas acomodações: direciona para tela 'Acomodações'
- Gastronomia, direciona para tela nossa cozinha.
- Localização (Pode ser uma exibição Google Maps ou apenas ou apenas a descrição do local fictício )
- Contatos: considere inserir ícones de redes sociais

### Tela Sobre

- Exibe informações gerais sobre o Hotel
- Exibe 3 (três cards aleatórios de 3 (três)acomodações 
- Cada card contém: nome, valor de uma diária para uma pessoa e imagem da acomodação, é um link que direciona para os detalhes da respectiva acomodação.
- Botaõ 'Precisa de ajuda?' : abre modal com formulário de contato. (O mesmo da tela 'Contato')
 
### Tela Acomodações

- Lista de cards com as acomodações do Hotel: Crie ao menos 9 (nove) cards
- Cada card contém: nome e imagem da acomodação, é um link que direciona para os detalhes da respectiva acomodação.
- Produto em destaque: card com imagem e descrição. Este card é resultado da última escolha do usuário na lista de cards que deve persistir em `localStorage`.
- Ao carregar a tela 'Acomodações' o produto em destaque recupera o produto em destaque armazenado em `localStorage`
  
### Tela Reservas

- Usuário insere data de entrada (check-in), data de saída (check-out) via input type date
- Usuário insere quantidade de pessoas via input type number
- Cases para exibição:
  - Usuário acessa a tela via barra de navegação, neste caso não há escolha pré-definida de acomodação, então exibir as 3 três mais populares acomodações (Executive,Classic,Premium)
  - Usuário faz uma escolha via telas 'Home','Sobre' ou 'Acomodações': então exibir no topo da lista a acomodação alvo da escolha, mantendo as três opções existentes.
  - Cada card contém nome, descrição e o valor de uma diaŕia para uma pessoa, e um radioButton para registrar a escolha do usuário.
  - O card 'Resumo da Reserva' exibe nome, data de check-in/check-out, quantidade de pessoas e o valor total da Reserva. Este card deve ser reativo atualizando de forma assíncrona as informações caso o usuário troque de acomodação, data ou quantidade de pessoas
  - O valor das diárias aumenta conforme a quantidade de pessoas e as escolhas de opções de serviços adicionais.
  - Botão 'Adicionar mais Serviços': Exibe um dropDownList com diversos serviços e preços.
  - Exemplos:Cofre,Decoração com pétalas de rosas, Massagem Relaxante Masculina/Feminina,Serviço de Despertador, Academia com Personal Trainer, Lavanderia, Sala de Conferência, Hotelzinho Kids, Hotelzinho Pet)
  - Botão 'Continuar': abre um modal com o resumo da Reserva que é composto do descritivo das escolhas (Acomodação [Tipo, Período e Quantidade de Pessoas] + Serviços Adicionais)
  - A modal deve conter um botão 'Confirmar Resverva' que registra os dados no banco relacional.
  - A confirmação habilita um novo item da barra de navegação chamado 'Minhas Reservas' que exibe as reservas do usuário autenticado.

### Tela Contato

- Formulário: 
  - Nome: input type text
  - Email: input type email
  - Telefone: input type text 
  - Assunto: select(assunto [Cancelamento de Reserva,Ouvidoria,Departamento Financeiro], textarea (comentários)  
  - O teste de email pode ser feito com MailHog.

### Telas adicionais

- Tela Cadastro (formulário com os campos nome, email, telefone, cpf, senha e confirmação de senha). Desafio: Implementar a lógica de cadastro que possa ser reutilizada tanto para o cadastro de usuário público quanto para o usuário adminstrativo

- Tela Relatórios (Área Administrativa). Criar telas que listem usuários por categoria (público/admin), no caso dos usuários públicos (clientes),listar também suas respectivas reservas.

- Tela Acomodações (Área administrativa). Criar uma tela para listar as acomodações existentes e seu status (disponível/ocupada), no caso do status 'ocupada' exibir período de ocupação e usuário público associado a reserva.


- A aplicação é um sistema web, as telas são acessadas por rotas definidas na aplicação front-end (desenvolvido em Vue ou React)
- Parte da persistência deve ser armazenada temporariamente em `localStorage` otimizando o carregamento de informações como no caso da tela Reservas após o primeiro acesso.
- Para o uso do Banco de Dados NoSql, crie documentos em MongoDb para alimentar a lista de Cards da tela 'Acomodações'
  


### Problemática de Front-End:

- Os wireframes sugerem telas de resolução para Desktops. Imagine que a versão 'mobile' não foi definida e cabe a você e seu time aplicar a responsividade para solucionar essa questão.
- A aplicação deverá ser responsiva.
- O ajuste, a diagramação e  a organização visual do o conteúdo é livre, desdes que todos blocos sugeridos no wireframes sejam incluídos.
- Será analisada a reutilização inteligente do código e resolução da problemática apresentada no front.
- Os cálculos do valor total da reserva devem ser computados no front e as escolhas armazenadas em `localStorage`. 

- Total da reserva igual a:
  - valor da diaria multiplicado pelo quantidade de noites multiplicado pela quantidade de pessoas (limte de 4 pessoas)
  - Esse valor poderá ser somado a quantidade de serviços adicionais escolhidos.

### Cupom de desconto

- Criar uma sequência aleatória de 8 caracteres entre letras e números que deve ser registrada no banco de dados como o código de um cumpom de desconto.
- Quando inserida em um campo da tela Reservas (a ser implementado pelo time) aplica um desconto de 10% sobre o valor total da reserva.
- O código só pode ser utilizado uma única vez.

  
##  Testes de Responsividade
- O layout deve se adaptar e mudar de acordo com o tamanho da tela (Responsividade)
  - Smartphones, tablets (modos portrait e landscape)
  - Monitores a partir de 1024px até 1900px
- A fonte utilizada é a [Roboto](https://fonts.google.com/specimen/Roboto)
- A largura máxima do conteúdo é 1100px

## Importante!

- Observe que no layout da tela Reservas, o resumo não apresenta o campo 'Valor Total', você terá que inserir esta informação que é essencial para a completude da interface.
- Fique atento a outros detalhes e adicione itens que considere essencial, mas que não estejam descritos, desde que não saia do escopo do proposta.
- Precifique os serviços adicionais a seu critério
- Isole blocos header, nav, main e footer
- Todos os elementos da interface devem ser componentes
- Escolha a imagem do logo
- Escolha imagens para as acomodações (Pense em 9 opções)



## Considere no seu desenvolvimento

- HTML semântico, limpo e claro
- CSS responsivo, semântico, reutilizável e seguindo boas práticas
- Componentes reativos
- Utilização correta de git/gitHub

## Tecnologias

- Javascript
- Framework reativo: React ou Vue
- Para o CSS, não utilize BootStrap. Escreva o CSS nativo ou use o Sass (scss)
- Para o Javascript, sempre que possível use Vanilla
- Não utilize Jquery





- Os dados que a interface exibe são resultados do consumo da API desenvolvida no back-end que interage com o Banco de Dados MySql em conjunto com Node.js.
- Somente na momento da confirmação da reserva, os dados são registrados no Banco de Dados MySql.


- Boas práticas incluir uso de Javascript OOP e TypeScript