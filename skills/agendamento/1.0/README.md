# Agendamento

Esse fluxo consulta fornecedores próximos ao usuário e faz o agendamento de um serviço mecânico.
Para funcionar, depende de banco de dados de fornecedores.

| Informações |                             |
|-------------|-----------------------------|
| **Versão**  | 1.0                         |
| **Idioma**  | pt-BR                       |
| **Figma**   | [.fig](./agendamento.fig)   |
| **Fluxo**   | [.svg](./agendamento.svg)   |
| **Código**  | [.json](./agendamento.json) |

## Dependencias

- Banco de dados de fornecedores

## Comunicação

Aqui deve ser exposta como é feita a comunicação com esta skill (qual entrada e qual saida atraves do redirecionamento, seguindo o guideline de router).

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

![fluxo](./agendamento.svg)
