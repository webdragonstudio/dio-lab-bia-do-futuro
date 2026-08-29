# Base de Conhecimento

## Dados Utilizados

| Arquivo | Formato | Para que serve na IAra |
|---------|---------|---------------------|
| `historico_atendimento.csv` | CSV | Contextualizar interações anteriores e dar continuidade nos atendimentos|
| `perfil_investidor.json` | JSON | Personalizar as explicações, dúvidas e necessidades do cliente |
| `produtos_financeiros.json` | JSON | conhecer produtos para serem ensinados ao cliente |
| `transacoes.csv` | CSV | Analisar padrão de gastos do cliente e usar de forma inteligente e didática |


---

## Estratégia de Integração

### Como os dados são carregados?
> Descreva como seu agente acessa a base de conhecimento.

[ex: Os JSON/CSV são carregados no início da sessão e incluídos no contexto do prompt]

### Como os dados são usados no prompt?
> Os dados vão no system prompt? São consultados dinamicamente?

Dados do Cliente:
- Transações do cliente
- Perfil do cliente
- transações do cliente
- histórico de atendimento
- Produtos disponíveis

---

## Exemplo de Contexto Montado

> Mostre um exemplo de como os dados são formatados para o agente.

```
Dados do Cliente:
- Nome: João Silva
- Perfil: Moderado
- Saldo disponível: R$ 5.000

Últimas transações:
- 01/11: Supermercado - R$ 450
- 03/11: Streaming - R$ 55
...
```
