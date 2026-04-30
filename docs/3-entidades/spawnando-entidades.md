# Spawnando Entidades

## Quando usar

Pode ser que em algum momento você queira spawnar uma entidade no seu mundo.
Quando falamos de entidade estamos nos referindo a qualquer ser vivo(salvo exceções) do minecraft.
No jogo a hierarquia dos seres vivos é liderada pelas pelo termo entidade.

## Como usar

```java                                                         
                                                //Essa função pede o mundo em que será spawnado o mob e ele pede um motivo pelo qual esta sendo spawnado. "Triggered" diz para o jog que esse mob foi criado.
Entity minhaEntidade = entityType.ZOMBIE.create(serverWorld, SpawnReason.TRIGGERED);

serverWorld.spawnEntity(minhaEntidade);

```


