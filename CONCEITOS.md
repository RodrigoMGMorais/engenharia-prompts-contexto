# 📖 Conceitos Fundamentais

Aqui estão os termos e definições que você vai encontrar durante os estudos e no dia a dia profissional.

---

## 🧠 O que é Engenharia de Prompts?
É a **técnica de estruturar instruções** para guiar o comportamento de Modelos de Linguagem Grande (LLMs). Não é só "escrever bem" — é definir:
- Qual o papel do modelo
- Quais tarefas deve executar
- Qual formato de resposta deve seguir
- Quais regras deve respeitar

✅ **Objetivo**: Tornar as respostas **previsíveis, consistentes e úteis**.

---

## 📚 O que é Engenharia de Contexto?
É a **gestão das informações** que você envia junto com a pergunta. O modelo só sabe o que está dentro da sua "janela de contexto".

Principais pontos:
- **Janela de contexto**: Limite máximo de tokens/palavras que o modelo consegue processar
- **Qualidade acima da quantidade**: Envie só o que é relevante
- **Estrutura**: Organize os dados para facilitar a compreensão
- **Atualização**: Mantenha o contexto atualizado para evitar informações desatualizadas

✅ **Objetivo**: Evitar alucinações e manter a precisão sem ultrapassar limites.

---

## ⚙️ Técnicas Principais

### 1. Zero-Shot
Instrução sem exemplos: o modelo resolve apenas com a descrição da tarefa.
> *Exemplo*: `Explique o que é API REST em termos simples.`

### 2. Few-Shot
Você fornece **2 a 5 exemplos** de entrada e saída para ensinar o padrão.
> *Exemplo*:
> ```
> Entrada: "Nome: Maria | Cargo: Analista"
> Saída: "Maria trabalha como Analista."
> Entrada: "Nome: Heitor | Cargo: Programador"
> Saída:
> ```

### 3. Chain-of-Thought (CoT)
Pede para o modelo **explicar o raciocínio passo a passo**, melhorando resultados em tarefas lógicas.
> *Exemplo*: `Resolva o problema e mostre cada etapa do cálculo.`

### 4. ReAct
Combina **raciocínio + ação**: o modelo pode "buscar informações" ou "usar ferramentas" antes de responder.

### 5. RAG (Recuperação Aumentada de Geração)
Busca dados de fontes externas (documentos, bancos, arquivos) e adiciona como contexto, para responder com base em fatos reais.

---

## 📌 Termos Importantes
- **LLM**: Modelo de Linguagem Grande (ex: GPT, Gemini, Claude)
- **Token**: Unidade básica de processamento (1 palavra ≈ 1,3 tokens)
- **Alucinação**: Resposta incorreta mas escrita com confiança
- **Prompt Template**: Modelo reutilizável de instrução
- **Chunking**: Dividir textos longos em partes menores para caber no contexto

---

## 🎯 Por que isso importa?
- Reduz erros e respostas inventadas
- Aumenta a confiabilidade para uso profissional
- Diminui custos ao economizar tokens
- Permite criar soluções automatizadas e integradas com sistemas