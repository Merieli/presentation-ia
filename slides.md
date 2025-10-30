---
# You can also start simply with 'default'
theme: ./theme
# random image from a curated Unsplash collection by Anthony
# like them? see https://unsplash.com/collections/94734566/slidev
background: https://cover.sli.dev
# some information about your slides (markdown enabled)
title: Palestra IA
titleTemplate: "%s - Merieli"
author: Meriéli Manzano
info: |
  ## IA sem Frustração

  Uma apresentação sobre IA produtiva no trabalho de desenvolvedor.
# apply unocss classes to the current slide
class: text-center
# https://sli.dev/features/drawing
# fonts:
#   sans: Roboto
#   serif: Roboto Slab
#   mono: Fira Code
drawings:
  persist: false
# slide transition: https://sli.dev/guide/animations.html#slide-transitions
transition: slide-left
# enable MDC Syntax: https://sli.dev/features/mdc
mdc: true
# open graph
# seoMeta:
#  ogImage: https://cover.sli.dev

presenter: false
---

# De Pedreiro a Arquiteto

Repensando a Programação na Era da IA.

<div class="abs-br m-6 text-xl">
  <a href="https://github.com/Merieli" target="_blank" class="slidev-icon-btn">
    <carbon:logo-github />
  </a>
</div>

---

# O "Momento Copiloto"

A revolução da IA no desenvolvimento não é sobre **substituir** o programador. É sobre **promovê-lo**.

Estamos saindo da era de _digitar código_ para a era de _dirigir a criação de código_.

<br>

**Agenda:**

- O que é a IA Generativa para Devs.
- A Mudança de Paradigma: O "Novo Pensamento".
- Como Usar: A IA no Ciclo de Vida do Dev.
- Desafios: A IA não é mágica.
- O Futuro: O Agente de IA.

---

## O Que Mudou? A IA Generativa para Devs

Não é _qualquer_ IA. Falamos de **LLMs** (Large Language Models) treinados com bilhões de linhas de código.

<div grid="~ cols-3 gap-4" m="t-4">

<div>
<div i-carbon-code text-4xl />
<h4>Assistentes de Código</h4>
<p text-sm>
GitHub Copilot, Tabnine, Codeium. Foco em <b>autocompletar</b>.
</p>
</div>

<div>
<div i-carbon-chat text-4xl />
<h4>Chatbots de Contexto</h4>
<p text-sm>
ChatGPT, Google Gemini, Claude, Cursor. Foco em <b>perguntar e refatorar</b>.
</p>
</div>

<div>
<div i-carbon-cics-program text-4xl />
<h4>Ferramentas Especializadas</h4>
<p text-sm>
Testes (CodiumAI), Documentação (Mintlify), Debugging.
</p>
</div>

</div>

<br>

> O ponto-chave: Elas não são "autocomplete" glorificados. Elas entendem (parcialmente) a **intenção** por trás do seu código.

---

# O Núcleo: A Mudança de Paradigma

| Característica        | Antigo Programador (O Artesão)                             | O Novo Programador (O Arquiteto)                                    |
| :-------------------- | :--------------------------------------------------------- | :------------------------------------------------------------------ |
| **Foco Principal**    | Sintaxe e Algoritmos.                                      | Intenção e Especificação.                                           |
| **Atividade Central** | Digitar código linha a linha.                              | Escrever prompts e _revisar_ código gerado.                         |
| **A Pergunta**        | "Como _eu_ escrevo esta lógica?"                           | "Como _eu explico_ esta lógica para a IA?"                          |
| **Depuração**         | "Onde está o _meu_ erro?"                                  | "O que a IA _não entendeu_ do meu pedido?"                          |
| **Valor Agregado**    | Eficiência na digitação, conhecimento profundo da sintaxe. | Clareza de comunicação, visão de sistema, velocidade de integração. |

<br>

A nova habilidade essencial: **Engenharia de Prompt aplicada ao código.**

---
layout: two-cols
layoutClass: gap-20
---

### O Pedreiro

Constrói a casa do zero. Prepara a fundação, assenta os tijolos, finaliza com o acabamento.
<br><br>
O valor está no **trabalho manual detalhado**. Cada linha de código é escrita e posicionada com cuidado.

::right::

### O Arquiteto (com IA)

Projeta a solução. Define os requisitos, a estrutura, os materiais e o estilo.
<br><br>
A IA (a "fábrica inteligente") gera um protótipo. O arquiteto então **ajusta, refina e valida** a qualidade final.


---

# Como Usar: IA no Ciclo de Vida do Dev

A IA pode ser sua parceira em todas as fases do desenvolvimento.

<div grid="~ cols-2 gap-x-8 gap-y-4" m="t-4">

<div>
<div i-carbon-flash text-3xl text-green-500 />
<h4>1. Geração e Prototipagem</h4>
<p text-sm>
Crie boilerplates, scripts e componentes em segundos a partir de um comentário.
</p>
</div>

<div>
<div i-carbon-loop text-3xl text-blue-500 />
<h4>2. Refatoração e Otimização</h4>
<p text-sm>
Peça para a IA simplificar ifs aninhados, otimizar laços ou aplicar design patterns.
</p>
</div>

<div>
<div i-carbon-search text-3xl text-yellow-500 />
<h4>3. Explicação e Debugging</h4>
<p text-sm>
Cole um erro ou um trecho de código complexo e peça uma explicação em linguagem simples.
</p>
</div>

<div>
<div i-carbon-test-tool text-3xl text-orange-500 />
<h4>4. Geração de Testes</h4>
<p text-sm>
Gere testes unitários, de integração e mocks para garantir a qualidade do seu código.
</p>
</div>

</div>

---
layout: two-cols
---

### Pensamento Antigo

"Preciso criar uma API REST em Node. Ok, `npm init`, `install express`, criar pastas, `app.get`..."

```typescript
// Horas depois...
import express from "express";

const app = express();
app.use(express.json());

// ...código manual para cada rota...
app.post("/produtos", (req, res) => {
  // ...lógica de criação...
});

app.listen(3000);
```

::right::

### Pensamento Novo

(Prompt para a IA)

```md
Crie um servidor Express básico com endpoints CRUD
para um recurso 'produto' (com nome e preco),
usando TypeScript e rotas separadas.
```

<br>

O dev faz o quê? **Valida as rotas, conecta ao banco de dados real e adiciona a lógica de negócio.**

---

## layout: two-cols

::left::

### Pensamento Antigo

"Este 'if' aninhado está horrível. Como posso simplificar isso? Talvez um _strategy pattern_?"

```javascript
function calcularDesconto(usuario) {
  let desconto = 0;
  if (usuario.tipo === "premium") {
    if (usuario.compras > 10) {
      desconto = 0.2;
    } else {
      desconto = 0.1;
    }
  } else {
    if (usuario.compras > 5) {
      desconto = 0.05;
    }
  }
  return desconto;
}
```

::right::

### Pensamento Novo

(Seleciona o bloco e pergunta à IA)

`"Refatore este código para ser mais legível e eficiente. Use 'early returns' e remova a complexidade ciclomática."`

```javascript
function calcularDesconto(usuario) {
  if (usuario.tipo !== "premium") {
    return usuario.compras > 5 ? 0.05 : 0;
  }

  return usuario.compras > 10 ? 0.2 : 0.1;
}
```

O dev faz o quê? **Analisa a sugestão e garante que os testes ainda passam.**

---

## class: px-20

# Desafios: A IA não é mágica

A confiança cega é o maior erro do "novo pensamento".

- 🤹 **Alucinações**: A IA _inventa_ fatos, APIs que não existem ou lógicas sutilmente erradas.
- 💀 **Viés e Segurança**: A IA aprende com código bom, mas também com código ruim, inseguro e antigo.
- 📝 **Falta de Contexto**: O código gerado pode ser bom em teoria, mas ruim na prática do seu projeto.
- 📉 **Risco da "Atrofia"**: Se a IA faz tudo, vamos "desaprender" a programar?

<br>

> Assim como a calculadora não nos fez parar de entender matemática, a IA não nos fará parar de entender lógica. Ela nos permite focar em problemas mais complexos.

---

## layout: quote

## A Regra de Ouro

A IA é sua **estagiária**.

Uma estagiária brilhante, incrivelmente rápida, mas sem experiência de mundo ou contexto do seu projeto.

**Você é o Sênior. Você é o responsável final pelo `commit`.**

---

## class: px-20

# O Futuro: O Agente de IA

Estamos evoluindo do "Copiloto" para o "Agente Autônomo".

<br>

**O Novo Prompt:**

<div class="text-left p-4 border rounded-lg bg-gray-500/10">

_Hoje:_ `"Escreva uma função para..."`

<br>

_Amanhã:_ `"Monitore o app. Se a latência da API 'X' subir acima de 200ms por 5 minutos, analise os logs, identifique o gargalo, escreva um patch, teste-o em staging e, se passar, abra um Pull Request para minha revisão."`

</div>

<br>

O desenvolvedor se torna um Gerente de Produto Técnico, um Arquiteto de Sistemas e um **validador de alto nível**.

---

## class: px-20

# Conclusão

A IA não está tirando seu emprego; ela está **mudando a descrição do seu trabalho**.

<br>

### Chamado à Ação (Call to Action)

<div grid="~ cols-3 gap-4" m="t-4">

<div>
<div i-carbon-tool-box text-4xl />
<h4>1. Adote as Ferramentas</h4>
<p text-sm>
Use Copilot, ChatGPT, etc., <b>diariamente</b> para acelerar seu fluxo de trabalho.
</p>
</div>

<div>
<div i-carbon-critical text-4xl />
<h4>2. Seja Cético</h4>
<p text-sm>
Revise, entenda e valide <b>todo</b> o código gerado. A responsabilidade é sua.
</p>
</div>

<div>
<div i-carbon-architect text-4xl />
<h4>3. Pense como Arquiteto</h4>
<p text-sm>
Foque mais em <b>"o quê"</b> e <b>"por quê"</b>, e menos em "como digitar".
</p>
</div>

</div>

---

layout: quote
class: text-center

---

> "O futuro da programação não é sobre saber a sintaxe perfeita; é sobre fazer as perguntas perfeitas."

---

layout: center
class: text-center

---

# Perguntas?

**Obrigado!**

<br>
<br>

Meriéli Manzano

<div class="mt-4">
  <a href="https://github.com/Merieli" target="_blank" class="slidev-icon-btn">
    <carbon:logo-github />
    /Merieli
  </a>
</div>

<PoweredBySlidev mt-10 />
