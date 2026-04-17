# Documento de Requisitos de Software (SRS)  

|Campo|Descrição|
|-----|-----|
|Nome do Projeto|Controle de Hotel|
|Dono do Projeto|Sr. Geraldo|
|Versão|1.0|
|Data|16/04/2026|

## Introdução
O objetivo deste projeto é a criação de um Software para controle de quartos e entrada/saída de dinheiro do Hotel Bela Vista, nele deve estar incluso funcionalidades como, registro por cpf, mapeamento dos quartos, registro de gastos do frigobar, e resposta rápida quando solicitado o lucro ou prejuízo do mês.

## Escopo
O escopo do Controle de Hotel inclui, mas não se limita às seguintes funcionalidades:  
* Funcionalidade 1: Calcular entrada e saída de dinheiro automaticamente.
* Funcionalidade 2: Mapear os quartos ocupados e livres.
* Funcionalidade 3: Registrar consumo do frigobar no CPF do cliente.

## Requisitos Funcionais
|ID|Descrição do Requisito|
|-----|-----|
|RF01|O sistema deve fornecer uma interface visual que indique, em tempo real, quais quartos estão ocupados (vermelho), e quais estão desocupados (verde).|
|RF02|O sistema deve permitir o cadastro de hóspedes com os seguintes campos obrigatórios: CPF, nome, telefone.|
|RF03|O sistema deve permitir configurar diferentes valores para cada quarto, e aplicar o valor correto automaticamente no momento da reserva.|
|RF04|O sistema deve permitir associar ao CPF do hóspede os itens consumidos do frigobar durante a estadia, com cobrança automática no sistema.|
|RF05|O sistema deve gerar um alerta para a equipe de limpeza assim que um quarto for desocupado.|
|RF06|O sistema deve gerar um relatório mensal com o total de receias, total de despesas e lucro ou prejuízo do período.|

## Requisitos Não Funcionais

* RNF07: O sistema deve mostrar o lucro ou prejuízo, quando desejado, dentro de 1 segundo.
* RNF08: A interface deve ser simples para facilitar o uso.

## Design da Interface do Usuário (UI)
* Design: Cores mais básicas, como branco, cinza e preto.

## Cronograma do Projeto
|Tarefa|Data de Início|Data de Término|
|-----|-----|-----|
|Levantamento de Requisitos|09/04/2026|16/04/2026|

## Revisões
|Versão|Data|Descrição|
|-----|-----|-----|
|1.0|16/04/2026|Versão Inicial|

## Assinaturas
* Dono do Projeto: Sr. Geraldo.
* Gerente de Projeto: Douglas Patroni
