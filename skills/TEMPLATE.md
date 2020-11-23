# {{SKILL}}

{{Aqui será colocado toda a descrição da skill.}}

| Informações |                             |
|-------------|-----------------------------|
| **Versão**  | {{versao}}                  |
| **Idioma**  | {{idioma_PAIS}}             |
| **Figma**   | {{link para arquivo .fig}}  |
| **Fluxo**   | {{link para arquivo .svg}}  |
| **Código**  | {{link para arquivo .json}} |

## Dependencias

Aqui será listado todas as dependecias da skill, i.e:

- se precisa de um banco de dados especifico
- se precisa de alguma variavel definida
- se precisa de alguma API
- outras dependencias a mais que a skill necessite para funcionar

## Comunicação

Aqui deve ser exposta como é feita a comunicação com esta skill (qual entrada e qual saida atraves do redirecionamento, seguindo o guideline de router).

Por exemplo:

### Entrada

A skill espera a entrada no formato

```json
{
    "origin": "serviceName from the bot that is redirecting",
    "destination": "serviceName of the bot you are redireting to",
    "userInput": "the user's last message",
    "flow": "someId",
    "custom": { "field": "value" }
}
```

### Saida

A skill retorna para o destino xxxxx com yyyy informação no formato:

```json
{
    "origin": "serviceName from the bot that is redirecting",
    "destination": "serviceName of the bot you are redireting to",
    "userInput": "the user's last message"
}
```

## Preview

{{preview da imagem do fluxo do figma}}
