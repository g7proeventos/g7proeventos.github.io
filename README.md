# G7PRO - Gestão de Eventos · Site público

Página pública do evento: cronograma, chaves e lutas e checagem de atletas.
Somente leitura. Não tem login nem nenhuma função que altere dados.

## Arquivos

| Arquivo | Para que serve |
|---|---|
| `index.html` | A página inteira (visual e funcionamento) |
| `config.js` | O link do sistema G7PRO (projeto Gestão, final `/exec`) |
| `logo-g7pro.png` | Logo G7PRO |
| `favicon.png`, `icone-192.png` | Ícones da aba do navegador e do celular |

## Como os dados chegam

A página consulta o projeto Gestão no endereço `.../exec?api=publico` a cada 30 segundos.
Essa saída devolve só dados públicos: nome do evento, horários, lutas, resultados e a lista de
atletas com nome, equipe, faixa, peso e situação. Não inclui documento, telefone, data de
nascimento, idade, foto nem dados de usuários. O Gestão guarda a resposta por 30 segundos,
então muitas pessoas acessando ao mesmo tempo não sobrecarregam o sistema.

## Trocar o evento

Não precisa mexer aqui. Nome, logo, áreas e lutas vêm do próprio Gestão.
Só altere o `config.js` se o link `/exec` do Gestão mudar.
