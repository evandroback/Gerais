# Simulador Mega-Sena

E se você tivesse jogado sempre os mesmos números? Você marca de 6 a 20 dezenas e a página mostra, já a partir da sexta dezena, quanto você teria gastado e recebido em todos os concursos da Mega-Sena desde 1996.

**Site:** https://evandroback.github.io/Gerais/mega-sena/

## O que tem

- **Simulador:** saldo, senas, quinas e quadras comparadas com o esperado pela probabilidade, gráfico do gasto e do recebido ao longo do tempo, distribuição dos acertos e a lista dos concursos premiados.
- **Atalhos:** surpresinha, dezenas mais e menos sorteadas, mais atrasadas, digitar dezenas ou repetir o resultado de um concurso.
- **Filtros:** período (desde 1996, 10, 5 ou 1 ano, ou anos à escolha) e "só Mega da Virada".
- **Jogos salvos:** ficam no navegador de quem salvou e servem para comparar jogos no mesmo período.
- **Estatísticas:** frequência das dezenas, atrasos, maiores jejuns, duplas, pares e ímpares, repetições, soma das dezenas, maiores prêmios e estados onde saíram as senas.

## Dados

Planilha oficial de resultados da Mega-Sena da Caixa, com todos os concursos até o nº 3073 (22/10/2026): dezenas, ganhadores e valor por faixa, e o valor acumulado da sena. Os dados ficam embutidos no `mega-sena/index.html`; a página não consulta nenhum serviço externo.

## Como calcula

- Aposta simples a **R$ 6,00** (preço atual) em todos os concursos. Um jogo de n dezenas vale C(n, 6) apostas.
- Para k acertos num concurso: senas = C(k,6), quinas = C(k,5)·(n−k), quadras = C(k,4)·C(n−k,2).
- O prêmio de cada faixa é dividido entre os ganhadores reais e as suas apostas: prêmio total da faixa × suas apostas ÷ (ganhadores + suas apostas).
- Quando a sena acumulou, considera-se que você levaria sozinho o valor acumulado do concurso.
- Valores sem correção pela inflação. Jogos acima de 15 dezenas são simulados mesmo nos anos em que a Caixa não os aceitava.

## Atualização

Baixar a planilha nova em loterias.caixa.gov.br (Mega-Sena → Download de resultados) e regenerar o `mega-sena/index.html`.

---

Ferramenta independente, sem vínculo com a Caixa. Loteria é jogo de azar: resultados passados não mudam a chance do próximo sorteio.
