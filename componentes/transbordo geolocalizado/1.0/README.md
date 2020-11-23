# Transbordo Geolocalizado

Verifica a disponibilidade de atendimento de uma equipe informada previamente ao fluxo.
Caso esteja disponível, procede com o transbordo do usuário para o atendimento humano. Do contrário, informa qual o horário e pode sugerir consultar outra equipe/unidade.

| Informações |                                          |
|-------------|------------------------------------------|
| **Versão**  | 1.0                                      |
| **Idioma**  | pt-BR                                    |
| **Figma**   | [.fig](./transbordo-geolocalizado.fig)   |
| **Fluxo**   | [.svg](./transbordo-geolocalizado.svg)   |
| **Código**  | [.json](./transbordo-geolocalizado.json) |

## Dependencias

- fluxo anterior que selecione uma equipe/unidade.

## Comunicação

Aqui deve ser exposta como é feita a comunicação com este componente (qual entrada e qual saida).

### Entrada

O componente espera a entrada no formato de uma string contendo xxxxx, por exemplo:

> exemplo 1
> exemplo 2

### Saida

O componente retorna para xxxxx com yyyy informação no formato:

> formato de saida (json/string...)

## Preview

![fluxo](./transbordo-geolocalizado.svg)
