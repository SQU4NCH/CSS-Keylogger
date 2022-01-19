# CSS-Keylogger

Este é um Keylloger muito simples utilizando atributos do CSS.

Ele seleciona todos os atributos do site que tenham o tipo igual a "password" e depois tenta carregar uma imagem que está em "http://[IP-SERVER]:[PORT]/" enviando na requisição a tecla que foi digitada no campo de senha

Ele pode ser usado para criar um arquivo que vai ser chamado pelo site ou pode ser injetado em sites vulneráveis a XSS.

## Limitações

* Ele só consegue pegar dados muito específicos. Por exemplo, o campo de entrada deve ser do tipo password e não pode estar usando alguma outra forma de mascarar os caracteres
* Ele só funciona com a teclas que foram precionadas no campo selecionado, e não por pressionamento de tecla nem depois de sair do campo
* Não é acionado para valores que foram preenchidos automaticamente pelo gerenciador de credenciais do navegador ou por uma ferramenta de gerenciador de senhas
* Ele não pode lidar com caracteres repetidos, pois o navegador não solicitará novamente a imagem de fundo nesse caso
