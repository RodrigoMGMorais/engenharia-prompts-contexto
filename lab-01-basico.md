# 🧪 Lab 01 — Conceitos Básicos e Primeiros Prompts

**Objetivo**: Entender como pequenas mudanças na estrutura mudam totalmente a qualidade da resposta.

---

## ✅ Etapa 1: Prompt Genérico vs Estruturado

❌ **Muito vago**:
Me fale sobre APIs.
*Resultado*: Resposta genérica, superficial, sem foco.

✅ **Com papel e objetivo**:
Papel: Você é um desenvolvedor backend.Tarefa: Explique o que é uma API REST de forma simples para alguém que está começando.Destaque: Principais métodos HTTP e o que cada um faz.Formato: Texto curto com tópicos.
*Resultado*: Resposta direta, organizada e com o que você precisa.

---

## ✅ Etapa 2: Zero-Shot e Few-Shot

### Zero-Shot
Converta o texto abaixo para formato JSON:
Nome: Rodrigo | Idade: 35 | Cargo: Analista

### Few-Shot
Converta os dados para JSON seguindo o exemplo:
Exemplo 1:Entrada: Nome: Maria | Idade: 28 | Cargo: SuporteSaída: {"nome": "Maria", "idade": 28, "cargo": "Suporte"}
Exemplo 2:Entrada: Nome: Heitor | Idade: 22 | Cargo: ProgramadorSaída: {"nome": "Heitor", "idade": 22, "cargo": "Programador"}
Agora converta:Entrada: Nome: Ana | Idade: 30 | Cargo: Desenvolvedora

## ✅ Etapa 3: Definindo Restrições
Papel: Revisor de código Python.

Tarefa: Verificar se o código abaixo segue boas práticas.

Restrições:
Não use termos técnicos excessivos
Aponte apenas os problemas mais importantes
Sugira uma correção para cada ponto
Limite a resposta a 4 tópicos
Código:def soma(a,b):return a+b

---

## 📝 Anotações do Lab
- ✅ Sempre defina o **papel** e o **objetivo**
- ✅ Especifique o **formato** da resposta
- ✅ Use exemplos quando precisar de padrões específicos
- ✅ Adicione **restrições** para evitar respostas longas ou fora do escopo