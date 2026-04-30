# Client vs Server

## O que é

No minecraft o jogo roda em dois lados:

- **Client (cliente)** - O lado cliente é responsável pela renderização, pelos inputs do jogador(teclas clicadas, e mouse) e interface do game. Ou seja, tudo que acontece somente para o jogador, não incluindo o mundo, entidades, acontecimentos dentro do mundo...
- **Server (servidor)** - O lado do servidor é o responsável pela lógica de jogo que acontece dentro do mundo, ele controla entidades, mundo, eventos que ocorrem nele.

Mesmo que o player jogue singleplayer, esses dois lados ainda existem.

## Quando usar

É bom entender isso sempre que você for criar eventos para o seu mod, principalmente se você deseja que esse mod seja jogado por vários jogadores ao mesmo tempo.

## Exemplo

```java
if (world.isClient) {
    // dentro desse condicional rodam apenas eventos no lado do cliente
    world.spawnEntity(entity);
}
```

Se você não utilizar conferências como essa todos os acontecimentos e funções que você criar irão rodar nos dois lados, isso causa duplicações de eventos...

## Observações

- Tudo que altera coisas no mundo deveria rodar no server.
- Use o client para alterar somente para alterações visuais e par feedback do próprio player.



