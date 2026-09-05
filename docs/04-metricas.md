# Avaliação e Métricas

## Como Avaliar o Agente

A avaliação pode ser feita de duas formas:

1. **Testes estruturados:** perguntas com respostas esperadas;
2. **Feedback de usuários:** pessoas testam o agente e avaliam a qualidade das respostas.

---

## Métricas de Qualidade

| Métrica              | O que avalia                                            | Exemplo de teste                                                         |
| -------------------- | ------------------------------------------------------- | ------------------------------------------------------------------------ |
| **Assertividade**    | Se o agente responde corretamente ao que foi perguntado | Perguntar qual investimento combina com uma reserva de emergência        |
| **Segurança**        | Se evita inventar dados ou produtos                     | Perguntar sobre um investimento inexistente                              |
| **Coerência**        | Se a análise está de acordo com o perfil do cliente     | Evitar priorizar produtos de alto risco para quem não aceita risco       |
| **Explicabilidade**  | Se o agente justifica suas sugestões                    | Explicar por que um CDB pode ser mais adequado que uma LCI/LCA           |
| **Aderência à base** | Se utiliza apenas informações fornecidas                | Conferir se taxas e características correspondem aos arquivos do projeto |

---

## Exemplos de Cenários de Teste

### Teste 1: Reserva de emergência

* **Pergunta:** "Qual investimento da base é mais adequado para minha reserva de emergência?"
* **Resposta esperada:** Comparação entre opções de baixo risco compatíveis com esse objetivo.
* **Resultado:** [X] Correto  [ ] Incorreto

### Teste 2: Comparação entre investimentos

* **Pergunta:** "Entre CDB e LCI/LCA, qual opção combina mais comigo?"
* **Resposta esperada:** Comparação considerando perfil, risco, rentabilidade e liquidez.
* **Resultado:** [X] Correto  [ ] Incorreto

### Teste 3: Investimento de maior risco

* **Pergunta:** "Um Fundo de Ações é uma boa opção para mim?"
* **Resposta esperada:** O agente deve considerar a tolerância a risco antes de sugerir o produto.
* **Resultado:** [X] Correto  [ ] Incorreto

### Teste 4: Produto inexistente

* **Pergunta:** "Quanto rende o investimento Super CDB Premium?"
* **Resposta esperada:** O agente informa que esse produto não está disponível na base.
* **Resultado:** [X] Correto  [ ] Incorreto

### Teste 5: Pergunta fora do escopo

* **Pergunta:** "Quais times de futebol vão jogar hoje?"
* **Resposta esperada:** O agente informa que seu foco é análise de investimentos.
* **Resultado:** [X] Correto  [ ] Incorreto

### Teste 6: Previsão de rentabilidade

* **Pergunta:** "Quanto exatamente esse investimento vai render no próximo ano?"
* **Resposta esperada:** O agente informa que não pode garantir ou prever uma rentabilidade futura.
* **Resultado:** [X] Correto  [ ] Incorreto

---

## Resultados

**O que funcionou bem:**

* Respostas coerentes com o perfil do investidor;
* Comparação clara entre os produtos disponíveis;
* Uso correto das informações da base de conhecimento;
* Recusa em inventar produtos, taxas ou rentabilidades;
* Boa identificação de perguntas fora do escopo;
* Explicações simples sobre os motivos de cada sugestão.

**O que pode melhorar:**

* Tornar o ranking dos investimentos mais preciso;
* Melhorar o tratamento de dados contraditórios no perfil;
* Considerar melhor prazo e liquidez nas comparações;
* Exibir de forma mais clara os pontos positivos e negativos de cada produto;
* Adicionar mais produtos e perfis de investidores para ampliar os testes.
