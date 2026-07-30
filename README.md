# PromIA — Achados de Ofertas

Site do PromIA, grupo grátis com cupons e achadinhos garimpados da Shopee e do Mercado Livre. Além das ofertas publicadas no grupo, o agente do PromIA tem comandos que garimpam por você no privado: monitoramento de preço e busca de produtos com cupom já aplicado. As ofertas são monitoradas na plataforma e passam por seleção manual antes de chegar ao grupo, garantindo o melhor custo-benefício.

🔗 **Site no ar:** https://prom.ia.br

## Recursos do agente

Todos gratuitos e disponíveis apenas no contato direto com o administrador (nunca dentro do grupo).

| Comando | O que faz |
|---|---|
| `#monitorar` | Cadastra um produto + valor máximo. Quando a oferta sai no grupo, o PromIA avisa no privado com o horário do post. |
| `#procura` | Busca o item na hora na Shopee e no Mercado Livre, já com os cupons existentes aplicados no preço. |
| `#procura shopee` | O mesmo do `#procura`, restrito à Shopee. |

Comandos de apoio do `#monitorar`: `#alertas` (lista os monitoramentos), `#remove_monitor N` / `#remove_monitor todos` e `cancelar` (sai do cadastro). Limites: até 10 monitoramentos por pessoa, 30 dias de validade cada e timeout de 30 segundos no cadastro. O link da oferta nunca vai no privado por regra das plataformas de afiliados — só o horário do post no grupo.

## O que o site mostra

- Os três recursos do agente, com guia de uso, exemplos de mensagem e vídeo/banner de demonstração
- Cupons sempre disponíveis das plataformas parceiras, fixados no topo do grupo
- Top 3 das melhores opções para cada produto buscado
- Exemplos reais de ofertas, cupons e prints de seguidores
- Como funciona o processo de curadoria (monitoramento → seleção manual → publicação)
- Acesso direto ao grupo do WhatsApp

## Stack

- HTML + CSS puro, sem dependências de build
- Fontes: [Sora](https://fonts.google.com/specimen/Sora), [Inter](https://fonts.google.com/specimen/Inter) e [IBM Plex Mono](https://fonts.google.com/specimen/IBM+Plex+Mono), via Google Fonts
- Hospedado gratuitamente no [GitHub Pages](https://pages.github.com/), com domínio próprio via `CNAME`

## Estrutura

```
promia-achados/
├── index.html            # home: hero, carrossel de exemplos, índice de recursos, CTA
├── detalhes.html         # página de recursos: #monitorar, #procura, #procura shopee, cupons e como funciona
├── CNAME                 # domínio prom.ia.br
└── assets/
    ├── logo.png          # logo/selo do grupo
    ├── style.css         # estilos das duas páginas
    ├── exemplos/         # prints de ofertas, cupons e carrinho usados como exemplo
    ├── gif/              # vídeo demo do #procura (procura-demo.mp4 + poster.jpg)
    └── promo/            # banners de divulgação dos recursos (ex.: monitorar.jpg)
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

- **Preços, cupons e textos:** editar diretamente no `index.html` (home) ou no `detalhes.html` (recursos)
- **Novo recurso do agente:** criar um `.res-card` no `.res-index` das duas páginas + um bloco `.spotlight` com id próprio no `detalhes.html`, e adicionar o link na `.page-tabs` e no rodapé. Recurso recém-lançado recebe as classes `.is-new` e `.badge-new`
- **Imagens de exemplo:** substituir os arquivos em `assets/exemplos/` mantendo os mesmos nomes, ou trocar os caminhos `src` correspondentes no HTML
- **Vídeos e banners:** o vídeo demo fica em `assets/gif/` e os banners de divulgação em `assets/promo/` — ambos ocupam a coluna direita do `.spotlight` do recurso
- **Link do grupo:** buscar por `chat.whatsapp.com` nos dois HTMLs e atualizar o link nos botões

---

© 2026 PromIA — cupons e achadinhos da Shopee e do Mercado Livre, selecionados a dedo. Projeto independente, sem vínculo oficial com Shopee ou Mercado Livre.
