# Base de Conhecimento

## Dados Utilizados

| Arquivo | Formato | Utilização no Agente |
|---------|---------|---------------------|
| `historico_atendimento.csv` | CSV | Contextualizar interações anteriores |
| `perfil_investidor.json` | JSON | Personalizar recomendações |
| `produtos_financeiros.json` | JSON | Sugerir produtos adequados ao perfil |
| `transacoes.csv` | CSV | Analisar padrão de gastos do cliente |


## Adaptações nos Dados

> Você modificou ou expandiu os dados mockados? Descreva aqui.

[Não foi feita nenhuma alteração nos dados]

---

## Estratégia de Integração

### Como os dados são carregados?
> Descreva como seu agente acessa a base de conhecimento.

[Os arquivos JSON e CSV são carregados pela aplicação e utilizados como contexto nas consultas enviadas ao agente.]

### Como os dados são usados no prompt?
> Os dados vão no system prompt? São consultados dinamicamente?

[O perfil, as metas e os produtos disponíveis são enviados ao Gemini junto com a pergunta do usuário. O agente deve responder apenas com base nesses dados.]

---

## Exemplo de Contexto Montado

> Mostre um exemplo de como os dados são formatados para o agente.

```
Dados do Cliente:
- Nome: João Silva
- Perfil: Moderado
- Saldo disponível: R$ 5.000

Investimentos disponíveis:
- Tesouro Selic: baixo risco, 100% da Selic
- CDB Liquidez Diária: baixo risco, 102% do CDI
- LCI/LCA: baixo risco, 95% do CDI
- Fundo Imobiliário: risco médio
- Fundo de Ações: risco alto
...
```
