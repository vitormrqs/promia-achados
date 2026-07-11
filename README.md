# PromIA — Achados de Ofertas

Landing page do PromIA, grupo grátis com cupons e achadinhos garimpados da Shopee e do Mercado Livre. As ofertas são monitoradas na plataforma e passam por seleção manual antes de chegar ao grupo, garantindo o melhor custo-benefício.

🔗 **Site no ar:** https://prom.ia.br

## O que o site mostra

- Cupons sempre disponíveis das plataformas parceiras
- Top 3 das melhores opções para cada produto buscado
- Exemplos reais de ofertas e cupons já publicados no grupo
- Como funciona o processo de curadoria (monitoramento → seleção manual → publicação)
- Acesso direto ao grupo do WhatsApp

## Stack

- HTML + CSS puro, sem dependências de build
- Fontes: [Fraunces](https://fonts.google.com/specimen/Fraunces), [Work Sans](https://fonts.google.com/specimen/Work+Sans) e [IBM Plex Mono](https://fonts.google.com/specimen/IBM+Plex+Mono), via Google Fonts
- Hospedado gratuitamente no [GitHub Pages](https://pages.github.com/)

## Estrutura

```
promia-achados/
├── index.html            # página única do site
└── assets/
    ├── logo.png           # logo/selo do grupo
    └── exemplos/          # prints de ofertas, cupons e carrinho usados como exemplo
```

## Rodando localmente

Não precisa de instalação nem servidor — é só abrir o `index.html` direto no navegador, ou usar uma extensão tipo Live Server no VS Code para recarregar automaticamente durante edições.

## Deploy

O site é publicado via **GitHub Pages**, direto a partir da branch `main`:

1. `Settings` → `Pages`
2. Source: `Deploy from a branch`
3. Branch: `main` / pasta `/ (root)`

Qualquer alteração enviada (commit) para a `main` atualiza o site automaticamente em alguns minutos.

## Atualizando conteúdo

- **Preços, cupons e textos:** editar diretamente no `index.html`
- **Imagens de exemplo:** substituir os arquivos em `assets/exemplos/` mantendo os mesmos nomes, ou trocar os caminhos `src` correspondentes no HTML
- **Link do grupo:** buscar por `chat.whatsapp.com` no `index.html` e atualizar o link nos botões

---

© 2026 PromIA — cupons e achadinhos da Shopee e do Mercado Livre, selecionados a dedo.
