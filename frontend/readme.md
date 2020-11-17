# Frontend Challenge

O desafio consiste em desenvolver um pequeno projeto utilizando JavaScript com um _framework_ SPA da sua preferência, como Vue, React, Svelte, Angular ou Vanilla. Sua aplicação deverá se conectar com uma API que contém dados fictícios de empreendimentos imobiliários, bem como exibir uma lista onde cada empreendimento estará alocado em um componente de _card_.

![Card](assets/card.png)

Mas **atenção**, você precisará exibir os empreendimentos de acordo com algumas **regras de negócio**:

1. Empreendimentos sem geolocalização (chave `geo_location`) ou com valores nulos deverão ser desconsiderados.
2. A informação "localização privilegiada" deverá ser exibida apenas quando o empreendimento estiver dentro do _bounding box_:

```
MIN_LAT = -21.269
MIN_LNG = -47.857
MAX_LAT = -21.211
MAX_LNG = -47.780
```

3. Um empreendimento pode conter mais de um valor de área útil dos apartamentos (chave `usable_areas`), mas o mesmo deve ser desconsiderado da lista quando ao menos um dos valores for menor ou igual a 10.
4. Não exibir o número de suítes (chave `en_suites`) caso não existam valores. Também não exibir apenas o valor que seja menor do que 1, isto é, quando [0, 1, 2] exibir apenas "1 e 2".

---

Aqui vão algumas informações relevantes:

- O endereço da API é [`https://static-content.bivilabs.com.br/challenges/products.json`](https://static-content.bivilabs.com.br/challenges/products.json), ela já é _CORS ready_.
- Seja fiel ao _layout_ que [pode ser acessado aqui](https://xd.adobe.com/view/190d017b-e1a3-48f1-bdb0-e707a34e4b8d-4c5e/screen/38ba68f1-cff1-4a19-aaa9-01684b87a65e/).
- Na hora de usar CSS, escolha o seu pré (ou pós) processador preferido (ou não).
- Testes automatizados são desejáveis, sejam unitários, de integração ou ponta a ponta.
- Coloque o seu código em um repositório **privado** no GitHub, compartilhe com o usuário `@navedevs` e nos avise por e-mail. **Não se esqueça de documentar o passo a passo para rodar o seu projeto.**

Boa sorte!

**;)**
