# Padrão Observer - Javascript

## O que é o Padrão Observer 
> É um padrão de design de software no qual um objeto (chamado de `Subject`), mantém uma lista de seus dependentes (`Observers`) e os notifica automaticamente sobre qualquer alteração de estado, geralmente *trazendo/invocando/retornando* um de seus métodos.

Este padrão define um relacionamento um para muitos; Assim, quando um objeto (`subject`) é atualizado, ele notifica todos outros objetos (`observers`) de que eles foram atualizados.

Quando começamos a estudar padrões de projeto, é difícil imaginar um cenário em que podemos usar ou até mesmo, identificar se estão sendo usados e aonde estariam aplicados.

Se pararmos pra pensar, ele é utilizado por muitas aplicações e frameworks na web. Um dos exemplos que me vieram à cabeça ao estudar o padrão recentemente foi o "Framework Progressivo" VueJs e a lib React. De fato, é assim que a reatividade funciona em alguns desses framework's.

Imagine que temos vários estados na nossa aplicação e queremos que eles sejam atualizados quando algo importante acontece.

## Analogia

Vamos analisar um exemplo da vida real, reflita como uma newsletter funciona:

* Seu blog preferido começa a publicar vários artigos na semana, logo você não irá querer perder as novidades.
* Você resolve então assinar a newsletter; A partir de agora, sempre será avisado quando algo novo for publicado até o momento que não quiser mais.
* Em um segundo momento, resolve que não é mais interessante receber aquilo, então cancela a assinatura e o blog pára de enviar as novidades.
* Enquanto você realiza esse processo, podem ter várias outras pessoas assinando e cancelando a assinatura.

No padrão observer, o Blog seria o Subject e você seria o Observer.

## Prática

Para implementar os padrões de projeto temos que ter em mente que a grande maioria deles tem um contrato a ser seguido. Ele pode ser representado em programação orientada a objetos como uma `interface`, mas como não temos esse recurso, iremos implementar classes que representam nossos contratos, onde outras classes podem extender delas.

### Classe Subject

Nós teremos a classe Subject que irá manter uma lista de Observers e que precisam ser notificados quando ocorrer uma atualização; Também terá outras responsabilidades como adicionar ou remover Observers.

## Classe Observer

O objetivo da classe Observer é implementar um método update() que será chamado pelo método Subject notify(). Onde o update será responsável por renderizar o elemento novamente.

#### Mini biblioteca

Vamos ver como seria esse código na prática implementando uma mini lib de estados e renderização similar ao que o `React` faz. Nosso projetinho será o famoso TODO list.