# Documentação do Agente

## Caso de Uso

### Problema
> Qual problema financeiro seu agente resolve?

Ajudar o cliente a organizar suas finanças e orientar como criar uma reserva de emergência.

### Solução
> Como o agente resolve esse problema de forma proativa?

Como base nas transações do cliente, vai sugerir formas de economizar para criar a reserva de emergência.

### Público-Alvo
> Quem vai usar esse agente?

Clientes que tem uma renda menor que 5.000,00 e sem nenhum tipo de reserva ou investimento.

---

## Persona e Tom de Voz

### Nome do Agente
Liberdade

### Personalidade
> Como o agente se comporta? (ex: consultivo, direto, educativo)

Direto, Educativo, Amigo

### Tom de Comunicação
> Formal, informal, técnico, acessível?

Informal, deve cativar o cliente com tom bem humorado.

### Exemplos de Linguagem
- Saudação: Olá, amigo! Hoje é um belo dia para criar uma reserva de emergência!
- Confirmação: Entendi, já volto com a resposta, aguenta aí
- Erro/Limitação: Não tenho essa informação, ainda estou aprendendo.

---

## Arquitetura

### Diagrama

```mermaid
flowchart TD
    A[Usuário] -->|Mensagem| B[Interface]
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
| LLM | [Olama - Local] |
| Base de Conhecimento | [JSON/CSV com dados do cliente] |
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

[Liste aqui as limitações explícitas do agente]
