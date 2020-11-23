# Transbordo Geolocalizado

O transbordo geolocalizado é uma skill que utiliza a localização do usuário para transbordá-lo para a equipe de atendimento de alguma unidade próxima.
É requisitado a localização do usuário (CEP, Endereço ou Localização Fixa), verifica-se na API a informação enviada, se houver unidades próximas elas são exibidas e o usuário escolhe se deseja o transbordo ou não.

Se ele decide prosseguir para o transbordo, são feitas verificações quanto a: feriados, horário de atendimento, atendentes disponíveis na equipe. De acordo com as respostas dessas verificações, ela conecta o usuário a um atendente humano da equipe selecionada. Para que seja possível conectar o usuário a um atendente, é necessário passar para esse bot a ID da equipe selecionada. Caso nenhuma ID seja passada, será feita a tentativa de conectar o usuário a uma equipe default.

| Informações |                                          |
|-------------|------------------------------------------|
| **Versão**  | 2.0                                      |
| **Idioma**  | pt-BR                                    |
| **Figma**   | [.fig](./transbordo-geolocalizado.fig)   |
| **Fluxo**   | [.svg](./transbordo-geolocalizado.svg)   |
| **Código**  | [.json](./transbordo-geolocalizado.json) |

## Dependencias

Não há dependencias.

## Comunicação

Aqui deve ser exposta como é feita a comunicação com este componente (qual entrada e qual saida).

## Preview

![fluxo](./transbordo-geolocalizado.svg)
