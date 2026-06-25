# 🧪 Lab 02 — Estrutura, Formato e Validação de Saída

**Objetivo**: Aprender a definir regras claras para que a resposta venha no formato correto, com dados organizados e sem informações extras.

---

## 🎯 Por que isso é importante?
Se você não especificar o formato, o modelo pode responder com texto solto, listas, tabelas ou até parágrafos — impossível de usar em códigos ou sistemas. Com a estrutura definida, você garante **padronização e confiabilidade**.

---

## ✅ Etapa 1: Definir o formato da resposta

❌ **Sem definição**:
*Resultado*:
Temos os seguintes usuários:
Rodrigo, 35 anos, trabalha como Analista
Heitor, 22 anos, é Programador
Ana, 30 anos, atua como Desenvolvedora


✅ **Com formato especificado**:
Papel: Organizador de dados.Tarefa: Liste os usuários e seus dados.Formato de saída: Apenas JSON válido, sem texto extra, sem explicações.
Dados:
Rodrigo | 35 | Analista
Heitor | 22 | Programador
Ana | 30 | Desenvolvedora

*Resultado esperado*:
```json
[
  {"nome": "Rodrigo", "idade": 35, "cargo": "Analista"},
  {"nome": "Heitor", "idade": 22, "cargo": "Programador"},
  {"nome": "Ana", "idade": 30, "cargo": "Desenvolvedora"}
]

✅ Etapa 2: Adicionar restrições e limites
Você pode definir regras para evitar respostas longas ou fora do escopo:
Papel: Assistente técnico.
Tarefa: Resuma o que é uma API REST.

Regras obrigatórias:
- Máximo de 3 linhas
- Sem usar termos excessivamente técnicos
- Inclua apenas os 4 métodos principais (GET, POST, PUT, DELETE)
- Não adicione exemplos ou comparações
- Comece com: "API REST é..."

✅ Etapa 3: Usar marcadores para separar partes
Para facilitar a leitura e extração da resposta, use delimitadores claros:
Papel: Revisor de código.
Tarefa: Analise o código abaixo e retorne o resultado separado por seções.

Código:
def soma(a,b):
    return a + b

Formato:
---
✅ PONTOS POSITIVOS:
- [lista]

---
⚠️ MELHORIAS:
- [lista]

---
💡 SUGESTÃO DE CÓDIGO:
```python
[seu código aqui]


---

## ✅ Etapa 4: Validar e corrigir o formato

Muitas vezes pedimos um formato, mas o modelo pode acrescentar texto. Para evitar:
Instrução:Responda apenas com o formato solicitado.Se não for possível, responda somente: "Formato inválido".Não adicione explicações, observações ou comentários fora da estrutura.
Tarefa: Converta os dados para CSV.Dados:ID: 1 | Nome: Rodrigo | Cargo: AnalistaID: 2 | Nome: Heitor | Cargo: Programador

*Resultado correto*:
```csv
ID,Nome,Cargo
1,Rodrigo,Analista
2,Heitor,Programador
📝 Resumo do Lab
Sempre inclua no seu prompt:✅ Formato: JSON, CSV, tabela, lista, texto curto✅ Delimitadores: Seções claras para separar conteúdo✅ Restrições: Tamanho, linguagem, escopo✅ Regra final: "Sem texto extra", "Apenas o resultado"

💻 Exemplo prático em código
Veja como usar essa estrutura no Python:
def montar_prompt_formatado(dados):
    return f"""
    Papel: Organizador de dados.
    Tarefa: Converta a lista de usuários para JSON.
    Formato: Apenas JSON válido, sem comentários, sem texto adicional.

    Usuários:
    {dados}
    """

# Uso
lista = "- 1 | Rodrigo | Analista\n- 2 | Heitor | Programador"
print(montar_prompt_formatado(lista))

---

## 🚀 Adicionar ao repositório
Agora vamos salvar e enviar esse novo laboratório:

```bash
# Adiciona o arquivo do Lab 02
git add labs/lab-02-estrutura.md

# Confirma a alteração
git commit -m "Adiciona Lab 02: Estrutura e formato de saída"

# Envia para o GitHub
git push

