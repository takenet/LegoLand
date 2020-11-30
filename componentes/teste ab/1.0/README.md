# Teste A/B

Este componente faz a decisão de um teste A/B dentro do fluxo. Com ele é possivel decidir um fluxo a partir de uma porcentagem, grupo seleto de usuários ou dois grupos de usuários (com fallback para usuários não definidos em nenhum dos grupos).

| Informações |                            |
|-------------|----------------------------|
| **Versão**  | 1.0                        |
| **Idioma**  | en-US                      |
| **Figma**   | {{link para arquivo .fig}} |
| **Fluxo**   | {{link para arquivo .svg}} |
| **Código**  | [.json](./ab-testing.json) |

## Dependencias

- Váriavel de `Contexto` de nome `abTestConfig`, mais detalhes no tópico de [entrada da comunicação](#Entrada).

## Comunicação

A configuração do componente é feita a partir da váriavel `abTestConfig`.

### Entrada

O componente espera uma váriavel do tipo `object`, que sempre deve ter os campos `type` e `options`.

| Campo   | Tipo     | Descrição                       |
|---------|----------|---------------------------------|
| type    | `string` | tipo de teste A/B               |
| options | `object` | configurações do tipo escolhido |

```json
{
    "type": "percent | groups | selected",
    "options": {
        "percent": 50,
        "selected": "selected@broadcast.msging.net",
        "groups": {
            "a": "group-a@broadcast.msging.net",
            "b": "group-b@broadcast.msging.net"
        }
    }
}
```

#### type

O campo `type` é uma `string` com os possiveis valores:
| type     |
|----------|
| percent  |
| selected |
| groups   |

#### options

O campo `options` é um `object` com os possiveis campos:
| Campo    | Tipo      | Descrição                                                                                                                         |
|----------|-----------|-----------------------------------------------------------------------------------------------------------------------------------|
| percent  | `integer` | Porcentagem de usuários que devem seguir no **fluxo A**                                                                           |
| selected | `string`  | `identity` da [lista de distribuição][broadcast] dos usuários que devem seguir no **fluxo A**                                     |
| groups   | `object`  | `identities` das [listas de distribuição][broadcast] do grupo A e grupo B de usuários que devem seguir em seus respectivos fluxos |

##### groups

| Campo | Tipo     | Descrição                                                                                   |
|-------|----------|---------------------------------------------------------------------------------------------|
| a     | `string` | `identity` da [lista de distribuição][broadcast] de usuários que devem seguir o **fluxo A** |
| b     | `string` | `identity` da [lista de distribuição][broadcast] de usuários que devem seguir o **fluxo B** |

#### Exemplos

Alguns exemplos de valores da váriavel `abTestConfig`

##### Fluxo com 85% dos usuários

```json
{
    "type": "percent",
    "options": {
        "percent": 85
    }
}
```

##### Fluxo para usuários de uma lista

```json
{
    "type": "selected",
    "options": {
        "selected": "new-payment-users@broadcast.msging.net"
    }
}
```

##### Fluxo diferentes para usuários especificos

```json
{
    "type": "groups",
    "options": {
        "groups": {
            "a": "br-users@broadcast.msging.net",
            "b": "na-users@broadcast.msging.net"
        }
    }
}
```

### Saida

O componente vai direcionar o usuário baseado na váriavel `abGroup` que pode ter os seguintes valores:

| Valor | Descrição                                                                                                                                                             |
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| A     | Usuário deve ir para o fluxo A                                                                                                                                        |
| B     | Usuário deve ir para o fluxo B                                                                                                                                        |
| C     | Caso alguma configuração não tenha sido passada ou foi utilizado o `type` `groups` e o usuário não pertence a nenhum dos dois grupos deve ir para o fluxo de fallback |

## Preview

{{preview da imagem do fluxo do figma}}

[broadcast]: https://docs.blip.ai/#broadcast
