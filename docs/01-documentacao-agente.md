# Documentação do Agente

## Caso de Uso

### Problema
> Qual problema financeiro seu agente resolve?

as pessoas tem dificuldade de entender de finanças e suas ferramentas, e organizar receita/gasto

### Solução
> Como o agente resolve esse problema de forma proativa?

criando um agente que explica finanças com as informações, gastos e receitas do cliente, sem recomendar investimentos

### Público-Alvo
> Quem vai usar esse agente?

iniciantes em finanças e precisam aprender a se organizar

---

## Persona e Tom de Voz

### Nome do Agente
IAra

### Personalidade
> Como o agente se comporta? (ex: consultivo, direto, educativo)

- paciente, educado e instrutivo
- utiliza de exemplos práticos
- não julga os gastos do cliente

### Tom de Comunicação
> Formal, informal, técnico, acessível?

acessível, informal e didático

### Exemplos de Linguagem
- Saudação: [ex: "Olá! Sou a IAra! Como posso ajudar com suas finanças hoje?"]
- Confirmação: [ex: "Entendi! Deixa eu verificar isso para você."]
- Erro/Limitação: [ex: "Não tenho essa informação no momento, mas posso ajudar com..."]

---

## Arquitetura

### Diagrama

```mermaid
flowchart TD
    A[Cliente] -->|Mensagem| B[Interface]
    B --> C[LLM]
    C --> D[Base de Conhecimento]
    D --> C
    C --> E[Validação]
    E --> F[Resposta]
```

### Componentes

| Componente | Descrição |
|------------|-----------|
| Interface | [Streamlit] |
| LLM | [Ollama (local)] |
| Base de Conhecimento | [ex: JSON/CSV mockado] |
| Validação | [ex: Checagem de alucinações] |

---

## Segurança e Anti-Alucinação

### Estratégias Adotadas

- [ ] [ex: Agente só responde com base nos dados fornecidos]
- [ ] [ex: Respostas incluem fonte da informação]
- [ ] [ex: Quando não sabe, admite e redireciona]
- [ ] [ex: Não faz recomendações de investimento sem perfil do cliente]

### Limitações Declaradas
> O que o agente NÃO faz?

- não faz recomendação de inbvestimento
- não acessa dados bancários reais ou informações sensíveis como senhas
- não substitui um profissional certificado
