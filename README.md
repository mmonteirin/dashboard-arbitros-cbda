# 🌊 Dashboard — Árbitros de Águas Abertas · CBDA

> Painel interativo de gestão do Quadro Nacional de Árbitros de Águas Abertas da Confederação Brasileira de Desportos Aquáticos.

---

## 📋 Sobre o Projeto

Este dashboard foi desenvolvido para centralizar e visualizar o histórico completo de formação e avaliação dos árbitros nacionais de Águas Abertas, consolidando dados de inscrições, avaliações e certificados emitidos entre 2024 e 2026.

O arquivo é **100% autossuficiente** — todos os dados estão embutidos no próprio HTML. Basta abrir no navegador ou publicar em qualquer hospedagem estática para funcionar imediatamente, sem servidor, banco de dados ou dependências externas.

---

## ✨ Funcionalidades

### KPIs em Tempo Real
- Total de árbitros únicos cadastrados
- Quantidade com avaliação registrada
- Taxa geral de aprovação (%)
- Média geral de desempenho (escala 0–10)
- Total de participações em cursos
- Número de estados (UF) representados

### Filtros Avançados
- Busca textual por nome (em tempo real)
- Filtro por Estado (UF)
- Filtro por curso específico
- Filtro por status: Aprovado / Reprovado / Não Avaliado

### Tabela Master-Detail
- Lista completa de árbitros com paginação (30 por página)
- Clique em qualquer linha para abrir o **card de detalhe individual**, exibindo:
  - Histórico cronológico de todos os cursos realizados
  - Nota individual por curso (escala 0–10)
  - Nota mínima exigida por tipo de curso
  - Badge de status: APROVADO / REPROVADO / NÃO AVALIADO

### Gráficos Interativos
- **Barras:** distribuição de árbitros por Estado (UF)
- **Linhas:** evolução da média de notas por curso/turma, com linhas de corte para Formação (7,0) e Reciclagem (8,0)

### Regulamento Nacional Integrado
- Botão de acesso direto ao Regulamento completo da CBDA
- Modal com navegação por capítulo (16 capítulos organizados)
- Funciona sem conexão à internet

---

## 📊 Dados Consolidados

| Fonte | Descrição |
|---|---|
| Inscrições 2024–2025 | Dados cadastrais, UF e cidade dos árbitros |
| Avaliação — Formação de Árbitros 2024 | Prova teórica (escala 0–100 → convertida para 0–10) |
| Avaliação — Reciclagem 2024 | Prova teórica (escala 0–10) |
| Avaliação — Formação 2025 – 1ª e 2ª Turma | Prova teórica (escala 0–100 → convertida para 0–10) |
| Avaliação — Reciclagem 2025 – 1ª e 2ª Turma | Prova teórica (escala 0–10) |
| Avaliação — FDAP 2026 | Prova teórica (escala 0–10) |
| Certificados Emitidos 2026 | Confirmação de participação e emissão |

**Chave de união:** e-mail do árbitro (evita duplicidade por homônimos).

---

## 📐 Esquema de Aprovação

| Tipo de Curso | Nota Mínima |
|---|---|
| Formação (todos os anos e turmas) | **7,0** |
| Reciclagem (todos os anos e turmas) | **8,0** |

Notas originalmente em escala 0–100 são convertidas automaticamente para 0–10.
Todos os nomes são exibidos em letras maiúsculas (CAPS LOCK).

---

## 🚀 Como Usar

### Abrir localmente
1. Baixe o arquivo `index.html`
2. Clique duas vezes para abrir no navegador (Chrome, Edge, Firefox ou Safari)
3. Todos os dados carregam instantaneamente — nenhuma conexão necessária

### Publicar online (Netlify Drop — recomendado)
1. Acesse [app.netlify.com/drop](https://app.netlify.com/drop)
2. Arraste o arquivo `index.html` para a janela
3. Copie o link público gerado automaticamente

### Publicar no GitHub Pages
1. Faça o upload do `index.html` neste repositório (renomeado como `index.html`)
2. Acesse **Settings → Pages → Branch: main → Save**
3. Aguarde 1–2 minutos; o link será `https://seuusuario.github.io/nome-do-repositorio`

---

## 🏗️ Tecnologias

- **HTML5 + CSS3 + JavaScript** puro (sem frameworks)
- **[Chart.js 4.4](https://www.chartjs.org/)** — gráficos interativos (via CDN)
- **Google Fonts** — Inter, DM Mono, Syne (via CDN)
- Dados embutidos diretamente no HTML como JSON (sem requisições externas)

---

## 📁 Estrutura do Repositório

```
/
├── index.html          # Dashboard completo (autossuficiente)
└── README.md           # Este arquivo
```

---

## 📜 Regulamento

O dashboard inclui o **Regulamento Nacional de Formação, Avaliação, Certificação, Progressão e Manutenção do Quadro Nacional de Árbitros de Águas Abertas da CBDA**, acessível pelo botão **📋 Regulamento Nacional** no cabeçalho, com os seguintes capítulos:

1. Disposições Preliminares
2. Quadro Nacional de Árbitros
3. Árbitro Estadual
4. Árbitro Nacional
5. Árbitro Nacional B
6. Árbitro Nacional A
7. Árbitro Internacional
8. Certificações Específicas
9. Avaliação
10. Manutenção da Certificação
11. Formação Continuada
12. Código de Ética
13. Penalidades
14. Arbitragem Paralímpica
15. Banco Nacional de Árbitros
16. Disposições Finais

---

## 🔄 Atualização dos Dados

Para atualizar o dashboard com novos dados:

1. Processe os novos arquivos de inscrição/avaliação (`.xlsx`)
2. Reexecute o script de consolidação (Python/pandas), que usa o **e-mail como chave primária**
3. Substitua o JSON embutido no `index.html`
4. Faça novo upload do arquivo atualizado

---

## 📬 Contato

Confederação Brasileira de Desportos Aquáticos — **CBDA**
Comissão Nacional de Arbitragem de Águas Abertas

---

*Dashboard desenvolvido para uso interno da CBDA. Dados relativos ao Quadro Nacional de Árbitros de Águas Abertas — 2024/2026.*
