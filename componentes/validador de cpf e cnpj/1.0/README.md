# Validador de CPF/CNPJ

Esse fluxo valida o número de CPF ou de CNPJ de um usuário a partir da entrada do número correspondente.
Há uma tolerância de 3 tentativas antes oferecer uma saída do fluxo.

| Informações |                                    |
|-------------|------------------------------------|
| **Versão**  | 1.0                                |
| **Idioma**  | pt-BR                              |
| **Figma**   | [.fig](./validador-cpf-cnpj.fig)   |
| **Fluxo**   | [.svg](./validador-cpf-cnpj.svg)   |
| **Código**  | [.json](./validador-cpf-cnpj.json) |

## Dependencias

- API que consulte o número na base de dado do cliente
- fluxo de input inesperado (opcional se usar regex para o formato do número)
- fluxo de transbordo (opcional se remover a opção do menu)

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

![fluxo](./validador-cpf-cnpj.svg)
