# Projeto Back-End Hotel  - Escola T.Ex

Boas vindas!


Convidamos você a participar em time, do desenvolvimento de um sistema de hotelaria onde as reservas são feitas online. 

## Tipo de Usuário

O sistema contempla dois tipos de usuário:

 - Usuário público que efetua reservas das acomodações.
 - Usuário administrativo que monitora o checkin, checkout e a disponibilidade dos apartamentos. 


## Features da aplicação

O desenvolvimento back-end consiste em :

- Criar os diagramas de classe para o bando de Dados Mysql
- Gerar as tabelas com suas devidas chaves e índices
- Criar views e procedures
- Usar o Node JS para efetuar leitura e escrita (GET/PUT/DELETE/UPDATE)
- Gerar rotas para os endpoints da aplicação
- Criar uma API REST (JSON) para consumo de dados estruturados   
- Criar uma pequena base noSQL para alimentar uma lista com as 'acomodações mais populares'



### Cadastro (público/admin)

- nome, email, telefone, cpf, senha (criptografada), nivel

- A lógica de cadastro deve ser reutilizada tanto para o cadastro de usuário público quanto para o usuário adminstrativo

### Relatórios (Área Administrativa - Acesso restrito)

- listar usuários por categoria (público/admin)
- listar reservas
    - data da reserva, nome do hospede, checkin, checkout, quantidade de pessoas, serviços adicionais, desconto, código do cumpom
- listar acomodações
    - nome, tipo, descrição, status (disponível/ocupada)

### Listagem pública

- listar acomodações
  - nome, tipo, descrição, diaria

- listar serviços opcionais
  - nome, descrição, valor

  
### Abstração da Tela Reservas

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

### Abstração do Cupom de desconto

- Criar uma sequência aleatória de 8 caracteres entre letras e números que deve ser registrada no banco de dados como o código de um cumpom de desconto.
- Quando inserida em um campo da tela Reservas (a ser implementado pelo time) aplica um desconto de 10% sobre o valor total da reserva.
- O código só pode ser utilizado uma única vez.

### Problemática de Back-End:

- Criar uma API que atenda aos requisitos do sistema
- Os wireframes apresentam as telas para abstração sobre os dados renderizados da API
- Para cada tela há uma quantidade especifica de dados, o sistema deve prover a capacidade de entrega dos dados para exibição em tela
- Será analisada a reutilização inteligente do código e resolução da problemática apresentada no back-end


## Considere no seu desenvolvimento

- Código reutilizável e seguindo boas práticas
- Use o conceito de microserviços
- Verifique sempres os componentes interconectados
- Rotas legíveis
- Utilização correta de git/gitHub

## Importante

Neste projeto serão disponibilizadas pela T.EX as telas com os templates em HTML/CSS que consomem a API desenvolvida.

## Tecnologias

- Javascript
- MySQL
- Mongo DB
- Node JS
- Express JS

## Cursos T.EX

Para que o (a) participante obtenha um bom desempenho neste projeto é necessário ter assistido a lista de cursos a seguir ou ter conhecimento equivalentes:

### Fundamentos

- Linux
- VsCode
- Git/GitHub
- Agile
- Lógica de Programação


### Back-End

- Javascript POO
- MySQL
- MongoDB
- Node JS

### Recomendados
A lista a seguir compõe cursos não obrigatório, porém recomendados para reforço dos conceitos abordados: 


#### Back-End

- Typescript  
- SSO
- React consumindo uma API
- API
- JSON



