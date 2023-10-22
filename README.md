# Plano de Teste - Sistema de Troca de Serviços 


## 1. Introdução

Este plano de teste tem como objetivo garantir que o "Sistema de Troca de Serviços" atenda aos requisitos funcionais e não funcionais, garantindo que a plataforma seja segura, confiável e eficiente. O sistema é desenvolvido com as seguintes tecnologias: Frontend em HTML e CSS, Backend em Java, e Banco de Dados MySQL

## 2. Objetivos dos Testes

* Validar a funcionalidade do sistema em relação aos requisitos especificados.
* Avaliar o desempenho, escalabilidade e disponibilidade do sistema.
* Garantir a segurança dos dados dos usuários.
* Verificar a usabilidade e acessibilidade do sistema.

## 3. Escopo dos Testes

Os testes abrangem as seguintes áreas do sistema:

* Cadastro de Usuário
* Perfil do Usuário
* Pesquisa de Serviços
* Publicação de Ofertas de Serviços
* Solicitação de Serviços
* Chat de Comunicação
* Avaliações e Classificações
* Gestão de Trocas
* Disponibilidade
* Usabilidade
* Compatibilidade de Navegadores

## 4. Estratégia de Teste
   
Os testes serão conduzidos em várias fases, incluindo:

* Teste de Unidade: Para verificar componentes individuais.
* Teste de Integração: Para garantir a integração entre os módulos.
* Teste de Sistema: Para verificar o sistema como um todo.
* Teste de Desempenho: Para avaliar o desempenho sob carga.
* Teste de Segurança: Para identificar vulnerabilidades.
* Teste de Aceitação do Usuário (UAT): Para avaliar a usabilidade e acessibilidade.

## 5. Casos de Teste
Cada área terá uma série de casos de teste específicos para cobrir os cenários criados pelos roteriros de testes.

#### 5.1 Teste de Unidade

* Caso de Teste 1: Verificar o cadastro de usuário.
* Caso de Teste 2: Verificar a criação de perfil de usuário.
* Caso de Teste 3: Verificar a pesquisa de serviços por categoria.
* Caso de Teste 4: Verificar a detecção de informações duplicadas, como e-mail e CPF já registrado.


#### 5.2 Teste de Integração

* Caso de Teste 5: Verificar a integração entre o cadastro de usuário e o perfil do usuário.
* Caso de Teste 6: Verificar a integração entre a pesquisa de serviços e a publicação de ofertas de serviços.
  

#### 5.3 Teste de Sistema

* Caso de Teste 7: Teste completo do processo de solicitação de serviços e gestão de trocas.
* Caso de Teste 8: Teste de segurança para proteção de dados do usuário.


#### 5.4 Teste de Desempenho

* Caso de Teste 9: Avaliar o desempenho sob carga simulando múltiplos usuários.


#### 5.5 Teste de Segurança

* Caso de Teste 10: Verificar a proteção contra ameaças comuns.
* Caso de Teste 11: Testar a autenticação e autorização.


#### 5.6 Teste de Aceitação do Usuário (UAT)

* Caso de Teste 12: Avaliar a usabilidade da interface do usuário.
* Caso de Teste 13: Avaliar a acessibilidade do sistema.
  

## 6. Recursos e Cronograma

* Recursos: Equipe de teste, ambiente de teste, dados de teste, usuários de teste.
* Cronograma: Os testes ocorrerão ao longo de um período de [31/10 até 27/11].
  

## 7. Critérios de Aceitação

O projeto será considerado aceito se:

* Todos os casos de teste forem bem-sucedidos.
* Os relatórios de bugs forem tratados de acordo com o processo definido.
* Os usuários de teste aprovarem a usabilidade e acessibilidade do sistema.

-------------------------------------------------------------------------------  
-------------------------------------------------------------------------------  

# Roteiro de Teste - Sistema de Troca de Serviços

## Funcionalidade: Cadastro de Usuário

#### Cenário: Cadastro de um novo usuário com informações válidas
   * Dado que o usuário está na página de cadastro
   * Quando o usuário preenche os campos obrigatórios com informações válidas
   * E clica no botão "Cadastrar"
   * Então o usuário deve ser redirecionado para seu perfil

 #### Cenário: Tentativa de cadastro com informações inválidas
   * Dado que o usuário está na página de cadastro
   * Quando o usuário preenche os campos com informações inválidas ou informações já criadas como CPF ou e-mail, já criados
   * E clica no botão "Cadastrar"
   * Então o sistema deve exibir uma mensagem de erro

## Funcionalidade: Perfil do Usuário

 #### Cenário: Atualização do perfil de usuário
   * Dado que o usuário está logado em sua conta
   * E está na página de edição de perfil
   * Quando o usuário atualiza suas informações pessoais
   * E clica no botão "Salvar"
   * Então as informações do perfil do usuário devem ser atualizadas

 #### Cenário: Visualização do perfil de outro usuário
   * Dado que o usuário está logado em sua conta
   * E há um outro usuário registrado no sistema
   * Quando o usuário visualiza o perfil desse outro usuário
   * Então o sistema deve exibir as informações do perfil desse usuário

## Funcionalidade: Pesquisa de Serviços

 #### Cenário: Pesquisa de serviços por categoria
   * Dado que o usuário está logado em sua conta
   * E há serviços cadastrados no sistema com categorias específicas
   * Quando o usuário seleciona uma categoria de serviço
   * E clica no botão "Pesquisar" ou nos icones de serviços
   * Então o sistema deve exibir os perfil de serviços da categoria selecionada

 #### Cenário: Pesquisa de serviços com palavras-chave
   * Dado que o usuário está logado em sua conta
   * E há serviços cadastrados no sistema com descrições que contêm palavras-chave
   * Quando o usuário insere palavras-chave na barra de pesquisa
   * E clica no botão "Pesquisar"
   * Então o sistema deve exibir perfil de serviços com base nas palavras-chave

## Funcionalidade: Publicação de Ofertas de Serviços - (em analise sobre como irá funcionar)

#### Cenário: Publicação de uma oferta de serviço
   * Dado que o usuário está logado em sua conta
   * E está na página de publicação de ofertas de serviços
   * Quando o usuário preenche os detalhes da oferta de serviço
   * E clica no botão "Publicar"
   * Então a oferta de serviço deve ser visível para outros usuários

 #### Cenário: Tentativa de publicação de oferta com informações em falta
   * Dado que o usuário está logado em sua conta
   * E está na página de publicação de ofertas de serviços
   * Quando o usuário tenta publicar uma oferta de serviço com informações em falta
   * E clica no botão "Publicar"
   * Então o sistema deve exibir uma mensagem de erro

## Funcionalidade: Solicitação de Serviços

#### Cenário: Envio de uma solicitação de serviço
   * Dado que o usuário está logado em sua conta
   * E está visualizando uma oferta de serviço ( perfil de outro prestador )
   * Quando o usuário envia uma solicitação para ococrrer a troca do serviço
   * E clica no botão "Enviar Solicitação"
   * Então o solicitado deve receber a solicitação

 #### Cenário: Tentativa de envio de solicitação sem preencher informações necessárias
   * Dado que o usuário está logado em sua conta
   * E está visualizando uma oferta de serviço ( perfil de outro prestador )
   * Quando o usuário tenta enviar uma solicitação sem preencher informações necessárias
   * E clica no botão "Enviar Solicitação"
   * Então o sistema deve exibir uma mensagem de erro

## Funcionalidade: Chat de Comunicação

  #### Cenário: Iniciar uma conversa com outro usuário
   * Dado que o usuário está logado em sua conta
   * E está na página de mensagens
   * Quando o usuário inicia uma conversa com outro usuário
   * Então o sistema deve abrir uma janela de chat com o outro usuário

  #### Cenário: Enviar uma mensagem em uma conversa existente
   * Dado que o usuário está logado em sua conta
   * E está em uma conversa existente com outro usuário
   * Quando o usuário digita uma mensagem e a envia
   * Então a mensagem deve ser entregue ao outro usuário

## Funcionalidade: Avaliações e Classificações

  #### Cenário: Avaliar outro usuário após uma troca de serviço
   * Dado que o usuário está logado em sua conta
   * E conclui uma troca de serviço com outro usuário
   * Quando o usuário acessa a página de avaliações
   * E classifica o outro usuário
   * Então a avaliação e classificação devem ser registradas

 #### Cenário: Tentativa de avaliação sem completar uma troca de serviço
   * Dado que o usuário está logado em sua conta
   * E não concluiu uma troca de serviço com outro usuário
   * Quando o usuário tenta avaliar o outro usuário
   * Então o sistema deve exibir uma mensagem de erro

## Funcionalidade: Gestão de Trocas

 #### Cenário: Visualização das trocas de serviço pendentes
   * Dado que o usuário está logado em sua conta
   * E há trocas de serviço pendentes em seu perfil
   * Quando o usuário acessa a página de trocas pendentes
   * Então o sistema deve exibir uma lista das trocas pendentes

 #### Cenário: Visualização das trocas de serviços que foram solicitadas, mas ainda não foram aceita ou recusadas 
   * Dado que o usuário está logado em sua conta
   * E há trocas de serviços que foram solicitas
   * Quando o usuário acessa a página de solicitados poderá aceitar ou recusar dependeno do que deseja

 #### Cenário: Marcar uma troca de serviço como concluída
   * Dado que o usuário está logado em sua conta
   * E há uma troca de serviço pendente em seu perfil
   * Quando o usuário marca a troca de serviço como concluída
   * Então a troca de serviço deve ser atualizada como concluída



