# Hacktoberfest VueNorte 2019

Chegamos à mais uma edição do [Hacktoberfest](http://hacktoberfest.digitalocean.com)!

> Não sabe o que é?
> A [Jéssica Temporal (@jessicatemporal)](https://medium.com/@jessicatemporal/ajude-algum-projeto-ganhe-uma-camiseta-e-d%C3%AA-o-primeiro-passo-no-mundo-do-c%C3%B3digo-aberto-74b425509f9c) fez um excelente artigo. É de 2017, mas continua muito atual.

```
É um evento que dura o mês inteiro e busca incentivar a participação em projetos open source, então saber um pouquinho de código para participar é interessante, mas não se deixe intimidar, tem espaço para todos os níveis de conhecimento. E a melhor parte: qualquer pessoa que queira pode participar da sua própria casa! - Jessica Temporal
```

Então, planejamos um evento especial direcionado à região Norte.

Vamos aprender o básico de Backend, usando `Node + Express` e ainda participar deste evento?

> Hey ho, Let´s Go! - Ramones

## Requisitos
```
- Ter o NodeJs instalado
- Ter uma conta no Github
- Cadastro no Hacktoberfest
```

## Conceitos
De forma bem simplificada, todo funcionamento web parte do princípio de Solicitação (`request`) e Resposta (`response`).

Você digita o site do google, o navegador faz uma solicitação aos servidores globais e recebe como resposta o conteúdo do site.

Outro exemplo é quando você digita seu login/senha num site qualquer (`request`) e obtém o acesso/recusa (`response`) do servidor.

Ok! Isto será o suficiente pra gente já fazer um backend.

## Sua Vez!
Acesse o repositório deste [PROJETO](https://github.com/RenatoSiqueira/Test_HacktoTest), clique em FORK (canto superior direito) e aguarde o processo terminar. Este projeto será copiado para sua conta, lhe dando permissão de modificar.

Entre na pasta `Contributors`, localize e clique no botão `Create new file`.

> Preencha a primeira linha com seu **nome**. E na segunda linha com seu usuário GitHub. **Colocar @ é um bônus.**

Exemplo: Seu nome é `John Doe`, o arquivo se chamará `johndoe`.
```
John Doe
@johndoe
```

Vá até o final do arquivo e MARQUE A OPÇÃO: **Create a new branch for this commit and start a pull request**
> Não deixe de marcar esta opção!
Deixe o resto em branco e clique em `Commit new file`

O novo arquivo está criado! Vamos fazer nosso primeiro `Pull Request`, vulgo `PR`?

Localize e clique no botão `Pull Request`. Na nova página que se abrirá, clique em `Create pull request` e em seguida, confirme `Create pull request` mais abaixo da página, sem precisar preencher nada.

**Parabéns!** Primeiro PR feito e faltam somente três!

Localize e clique em `Code` para voltar à página inicial. Agora vamos entender os arquivos que temos neste projeto.

### Arquivos do Repositório
.gitignore: 
> Responsável por dizer ao github quais arquivos não devem ser salvos no servidor.

README.md:
> Arquivo de texto utilizado para descrever o seu projeto. Ele é essencial se o seu projeto for público, ou seja, visa a criação e a participação de uma comunidade. É um arquivo simples onde você poderá descrever, documentar e exemplificar o seu projeto. Afinal, como saberemos usar se não tem instruções de uso?

package.json: 
> O arquivo package.json é o ponto de partida de qualquer projeto NodeJS. Ele é responsável por descrever o seu projeto, informar as engines (versão do node e do npm), url do repositório, versão do projeto, dependências de produção e de desenvolvimento dentre outras coisas. - [WBruno](http://wbruno.com.br/nodejs/package-json-entendendo-os-scripts/)

index.js:
> É aqui que vamos adicionar nossos códigos neste tutorial.

## Explicando o Conteúdo do index.js
```
const express = require('express')
const app = express()





app.listen(3000, () => console.log('Server Running...'))
```
> Linha 1: Importamos o pacote express que instalamos e atribuimos à constante 'express'.

> Linha 2: Vamos usar a constante 'app', recebendo e executando o express (o uso de parênteses ao final significa execução)

> Linha 3: Com o 'app' sendo executado, informamos que queremos 'ouvir' a porta 3000. O 'console.log' é a mensagem que será mostrada na tela se tudo estiver certo.

Salve o index.js.
No terminal, use o comando:
```
node index.js
```
E você será capaz de visualizar a mensagem 'Server Running...'
