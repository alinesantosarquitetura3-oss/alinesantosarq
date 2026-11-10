# Cafezinho Coado com Arquitetura — Definições da newsletter

Guia permanente da newsletter quinzenal do escritório Aline Santos Arquitetos.
Tudo o que é padrão está aqui e no gerador; o que muda a cada edição é só o conteúdo.

## Arquivos desta pasta

| Arquivo | O que é |
|---|---|
| `gerador.html` | App que monta a newsletter: preencher os campos → copiar o HTML → colar no Brevo. Também publicado como artefato no Claude. |
| `template-n01.html` | Fonte canônica da edição Nº 01, byte a byte igual ao que está salvo no Brevo (SHA-256 `298c46f3…`). Referência de padrão. |
| `DEFINICOES.md` | Este guia. |

## Identidade visual (fixa)

- **Largura:** 600px, centrada, sobre fundo `#0A0A0A`; cartão `#0D0F0D`; divisórias `#2A2724`
- **Cores de texto:** títulos `#F3F0EA` (creme) · corpo `#D8D5CD` · apoio `#A79E92` · notas `#6E675F` · destaque `#BE6718` (laranja)
- **Fontes:** títulos Cormorant Garamond (400, itálico no destaque) · corpo Jost (300; negrito 500)
- **Header:** logo Cafezinho à esquerda (184px) · logo alinesantos|arq à direita (170px, com 17px de compensação vertical)
- **Imagens de conteúdo:** 504px (dupla: 246px + 246px); capa com 28px de respiro no topo
- **Assinatura:** foto 240px à esquerda + nome em Cormorant itálico + botão laranja "Me chama para um Café!"
- **Rodapé:** Site · Instagram · WhatsApp + frase do bloco + `{{ unsubscribe }}` (obrigatório para o Brevo)

## Conteúdo (a cada edição)

- **Cadência:** quinzenal
- **Kicker fixo:** "— Uma conversa a cada quinze dias"
- **Receita editorial:** um projeto real + uma decisão que fez diferença + algo útil para o espaço do leitor
- **Estrutura:** capa com legenda → título grande com 1–2 palavras em laranja → abertura pessoal ("Olá!") → 3–4 seções numeradas (01 ·, 02 ·…) → convite final com botão de WhatsApp → assinatura → bloco Desapego na Obra (opcional) → rodapé
- **Tipos de seção:** texto e fotos · box de destaque (fundo `#141210`, borda esquerda laranja) · duas colunas comparativas
- **Assunto:** curto e curioso (ex.: "O que cabe em 30 dias?") — sem caixa alta, sem exclamações em série
- **Frase de espiada (preheader):** complementa o assunto, não repete

## Envio (Brevo)

- **Remetente:** Aline Santos e Arquitetos Associados `<aline@alinesantosarquitetura.com.br>` (DKIM/SPF/DMARC verificados: PASS)
- **Plano gratuito:** 300 e-mails/dia → **um bloco por dia**
- **Blocos de contatos:**
  - **A — clientes, parceiros e amigos** (lista "Nº01 - Bloco A"): rodapé "Você recebe este e-mail porque já teve contato com o escritório."
  - **B — contatos antigos** (lista "Nº01 - Bloco B (incerto)"): rodapé "Você recebe este e-mail porque em algum momento trocamos contatos — se preferir não receber, é só sair abaixo."
  - **C — lojas e fornecedores** (lista "Nº01 - Bloco C (lojas e fornecedores)"): rodapé "Você recebe este e-mail porque sua loja já esteve em nossos projetos e especificações."
- **Passo a passo:** Campanhas → Criar campanha → Criação → **Cole seu código** → colar o HTML do gerador → salvar → **enviar teste** para `aline@alinesantosarquitetura.com.br` → conferir no webmail → agendar/enviar
- **Entre blocos:** conferir descadastros e reclamações de spam do bloco anterior antes de disparar o próximo

## Fotos novas

Subir para a pasta `assets/` deste repositório (o site publica em `https://alinesantosarquitetura.com.br/assets/...`).
No gerador, basta escrever `assets/nome-da-foto.jpg`. Pedir no chat do Claude que ele sobe e otimiza.

## Checklist antes de enviar

1. Número da edição e mês atualizados
2. Assunto + frase de espiada novos
3. Links de WhatsApp com mensagem desta edição
4. Frase do rodapé compatível com o bloco
5. Teste enviado e aberto no webmail (logos alinhadas, fotos com margem)
6. `{{ unsubscribe }}` presente (o gerador já garante)
