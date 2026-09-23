# Desafio de Monitoramento de Temperatura

## 1. Identificação
* **Nome do aluno:** Guilherme Freire Fortuna Lourenço
* **Disciplina:** Algoritmos e Pensamento Computacional
* **Professora:** Profa. Karla Sartin
* **Título do projeto:** Sistema de Monitoramento de Temperatura com Alerta Consecutivo em Linguagem C

## 2. Objetivo
O programa tem como objetivo monitorar leituras de temperatura inseridas pelo usuário, comparando-as com um limite pré-estabelecido. Ele calcula estatísticas essenciais (média, maior, menor valor e percentual de violações) e automatiza a segurança ao interromper o processo caso ocorram três leituras consecutivas acima do limite tolerado.

## 3. Funcionamento do programa
* **Como o limite de temperatura é definido:** O usuário insere um valor inicial no início da execução, que passa por uma validação para garantir que seja estritamente maior que zero.
* **Como as leituras são realizadas:** Em um laço de repetição, o sistema solicita iterativamente valores numéricos correspondentes às medições.
* **Como valores inválidos são tratados:** Caso o usuário digite caracteres não numéricos ou dados inadequados, o programa exibe uma mensagem de erro, limpa o buffer de entrada (`stdin`) e repete a solicitação.
* **Como o programa identifica temperaturas acima do limite:** Cada valor inserido é comparado condicionalmente com a variável do limite configurado.
* **Como funciona a contagem de temperaturas consecutivas:** Uma variável acumuladora (`consecutivas`) é incrementada a cada ocorrência acima do limite. Se uma leitura normal for registrada, o contador é imediatamente zerado.
* **Qual condição encerra o monitoramento:** O programa é encerrado automaticamente caso o contador de temperaturas consecutivas atinja 3, ou manualmente caso o usuário responda 'n' quando questionado se deseja continuar.

## 4. Estruturas de repetição utilizadas
* **`do...while`:** Foi utilizado tanto para a validação das entradas (garantindo que o bloco execute ao menos uma vez para pedir o dado correto) quanto para o fluxo principal de monitoramento das leituras.
* **Justificativa:** A estrutura `do...while` é ideal para validação de dados e menus/fluxos interativos porque assegura que o trecho de código responsável por coletar a entrada do usuário rode obrigatoriamente antes de testar a condição de repetição.

## 5. Como executar
Para compilar e executar o código via terminal (Linux/macOS/Windows com GCC instalado):

```bash
gcc monitoramento.c -o monitoramento
./monitoramento
