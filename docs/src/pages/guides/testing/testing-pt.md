# Testando

<p class="description">Escreva testes para evitar regressões e ter uma boa qualidade de código.</p>

## Espaço do usuário

Geralmente é recomendado testar sua aplicação sem vincular os testes ao Material-UI. É assim que os componentes do Material-UI são testados internamente. Uma biblioteca que tem uma API de primeira classe para esta abordagem é [`@testing-library/react`](https://testing-library.com/docs/react-testing-library/intro/).

Por exemplo, ao renderizar um `TextField` seu teste não precisa consultar a instância específica do Material-UI do `TextField`, mas sim um `input`, ou `[role="textbox"]`.

Ao não depender da árvore de componentes React você torna seu teste mais robusto contra mudanças internas no Material-UI ou se você precisar de testes de snapshot, adicione componentes encapsulados adicionais como provedores de contexto. No entanto, não recomendamos teste de snapshot. ["Effective snapshot testing" por Kent C. Dodds](https://kentcdodds.com/blog/effective-snapshot-testing) entra em mais detalhes do porque testes de snapshot podem induzir em erro para testes de componentes React.

## Interno

Material-UI tem **uma vasta gama** de testes para que possamos liberar os componentes com confiança, por exemplo, os testes de regressão visual são feitos através da [Argos-CI](https://www.argos-ci.com/mui-org/material-ui), provaram ser realmente úteis. Para saber mais sobre os testes internos, você pode dar uma olhada no [LEIA-ME](https://github.com/mui-org/material-ui/blob/HEAD/test/README.md).
