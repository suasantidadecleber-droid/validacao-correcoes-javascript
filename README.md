# Validando correções em JavaScript e TypeScript

## Tema e objetivo

Este projeto explora como uma pessoa iniciante pode usar testes para avaliar se uma correção sugerida por IA resolve um bug em JavaScript ou TypeScript sem introduzir regressões.

## Notebook

Link para o notebook compartilhado: https://notebook.google.com/notebook/0c81c8c3-7e31-455b-9547-9b25268f344f

## Fontes utilizadas

1. **Getting Started — Jest**  
   https://jestjs.io/docs/getting-started  
   Documentação oficial do Jest. Foi escolhida como fonte principal por explicar a instalação, a criação e a execução de um teste, além de mostrar um resultado aprovado.

2. **Expect — Jest**  
   https://jestjs.io/docs/expect  
   Documentação oficial dos matchers e das asserções. Ajuda a entender como comparar o valor produzido pelo código com o resultado esperado.

3. **Tutorial: Introduzindo Testes Unitários para Devs Iniciantes — TabNews**  
   https://www.tabnews.com.br/wellwelwel/tutorial-introduzindo-testes-unitarios-para-devs-iniciantes-js  
   Tutorial comunitário em português, com exemplo prático de testes e explicação de asserções. O exemplo usa Poku; por isso, foi usado como apoio conceitual, e não como documentação de Jest.

## Diretriz de comportamento do notebook

O notebook foi orientado a atuar como tutor para iniciantes, responder com base nas fontes incluídas, citar as fontes usadas, explicar termos técnicos de forma simples e declarar quando as fontes não permitem responder. Também foi orientado a não afirmar que testes aprovados provam que o programa inteiro está livre de bugs.

## Perguntas, respostas e fontes

### 1. O que significa quando um teste do Jest mostra `PASS`?

**Resposta:** significa que aquele caso de teste passou: o resultado observado correspondeu ao esperado naquele teste. Isso não comprova que o programa inteiro esteja livre de bugs.

**Fonte:** Getting Started — Jest: https://jestjs.io/docs/getting-started  
**Citação exibida pelo notebook:** Quando o Jest exibe a indicação PASS no terminal (por exemplo, PASS ./sum.test.js), significa que o arquivo de teste foi executado com sucesso e que todas as asserções contidas nele foram atendidas sem disparar nenhum erro

### 2. O que fazem `expect` e um matcher como `toBe`?

**Resposta:** `expect` recebe o valor produzido pelo código, e o matcher verifica se ele corresponde ao valor ou à condição esperada. Se a verificação falhar, a asserção falha.

**Fonte:** Expect — Jest: https://jestjs.io/docs/expect  
**Citação exibida pelo notebook:** Em testes automatizados com o Jest, a função expect e os métodos chamados matchers (como o .toBe) trabalham em dupla para criar asserções e verificar se o código se comporta como esperado

### 3. Como os testes ajudam a identificar regressões após uma alteração?

**Resposta:** testes que cobrem comportamentos esperados podem ser executados novamente depois de uma alteração. Uma falha indica que algum comportamento coberto não correspondeu ao esperado. Testes aprovados dão evidência para os casos testados, mas não garantem a ausência de todos os problemas.

**Fontes:** Expect — Jest; tutorial para iniciantes no TabNews.  
**Citações exibidas pelo notebook:** Uma regressão ocorre quando modificamos o código (por exemplo, para aplicar uma correção sugerida por IA) e, acidentalmente, quebramos algo que já estava funcionando antes


As fontes ensinam conceitos e exemplos de testes, mas não demonstram por si só que uma correção específica sugerida por IA seja segura em qualquer projeto. Os testes precisam cobrir os comportamentos relevantes, e seus resultados devem ser interpretados dentro desse limite.