# Events

## O que é?
Eventos são formas de reagir a ações dentro do game.

Exemplo:

- Jogador interage com uma entidade(animais, monstros,neutros)
- Jogador entra no mundo
- Uma entidade morre

Basicamente existem varias funcionalidade que acontecem no lado do servidor que acionam eventos. No fabic é possivel coletar o momento em que esses eventos acontecem e criar funcionalidades extras quando eles acontecerem.

## Quando você vai usar?

Basicamente você quase sempre vai usar eventos, a maioria das funções que você ira adicionar no game, será necessário adicionar um evento para coletar quando algo acontece para engatilhar aquela função.

## Exemplo

```java
UseEntityCallback.EVENT.register((player, world, hand, entity, hitResult) -> {
    if (!world.isClient) {
        player sendMessage(Text.literal("Você clicou em uma entidade"), false);
    }
    return ActionResult.PASS
});
```

Nesse trecho de código está sendo coletado quando o player clica em uma entidade no jogo e está enviando uma mensagem no chat quando isso acontece.

