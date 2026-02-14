# 🏥 Rede Soma Drogarias - Santa Cruz | Landing Page

> Landing Page estilo Linktree high-end, otimizada para conversão via anúncios mobile (Meta Ads + Google Ads).

## 📁 Estrutura do Projeto

```
site-farmacia/
├── index.html        # Página principal (tudo em um arquivo)
├── logo.png          # Logo da Rede Soma (branca, fundo transparente)
├── cupomfeed.png     # Banner do cupom de entrega grátis
└── README.md         # Este arquivo
```

## 🚀 Como publicar

### Opção 1 — GitHub Pages (Grátis)
1. Crie um repositório no GitHub.
2. Faça upload dos 3 arquivos (`index.html`, `logo.png`, `cupomfeed.png`).
3. Vá em **Settings → Pages → Source: main / root** → Save.
4. Acesse em `https://seuusuario.github.io/nome-repo`.

### Opção 2 — Netlify / Vercel (Grátis)
1. Arraste a pasta inteira no painel do Netlify.
2. Domínio personalizado opcional.

### Opção 3 — Hospedagem própria
1. Faça upload via FTP para a pasta `public_html`.

## 🎯 IDs de Tracking (Google Tag Manager / Meta Pixel)

| ID | Elemento | Evento sugerido |
|---|---|---|
| `btn-whatsapp-hero` | Botão CTA principal (Resgatar Cupom) | `Lead` / `conversion` |
| `btn-cupom-banner` | Imagem do cupom clicável | `Lead` / `conversion` |
| `btn-ifood` | Link iFood | `click_ifood` |
| `btn-instagram` | Link Instagram | `click_instagram` |
| `btn-facebook` | Link Facebook | `click_facebook` |
| `btn-google-maps` | Link Como Chegar | `click_maps` |
| `btn-crediario` | Botão Crediário (Em Breve) | `click_crediario` |

### Configuração no GTM
1. Crie um **Trigger** do tipo "Click - Just Links" filtrando por `Click ID`.
2. Crie **Tags** do Meta Pixel (`fbq('track', 'Lead')`) e Google Ads Conversion disparando no trigger acima.

## 📊 Checklist de Marketing

### ✅ Meta Ads (Facebook / Instagram)
- [x] Open Graph `og:title`, `og:description`, `og:image`
- [x] Twitter Card tags
- [x] Meta Pixel placeholder pronto (`<!-- META PIXEL -->`)
- [x] Evento de conversão `Lead` nos botões de WhatsApp
- [x] URL limpa sem parâmetros desnecessários
- [x] Imagem OG com dimensões recomendadas (1200x630)

### ✅ Google Ads / SEO
- [x] Schema.org `LocalBusiness` JSON-LD
- [x] Meta description otimizada
- [x] Canonical URL
- [x] Preconnect para CDNs (performance)
- [x] Lighthouse-friendly (sem render-blocking)
- [x] Google Tag Manager placeholder pronto (`<!-- GTM -->`)
- [x] Acessibilidade: `aria-label` em todos os links

### ✅ Segurança & Compliance
- [x] CSP meta tag (Content Security Policy)
- [x] `rel="noopener noreferrer"` em todos os links externos
- [x] `target="_blank"` seguro
- [x] Referência LGPD no footer
- [x] Badge SSL no footer
- [x] Sem coleta de dados pessoais (cookieless na landing)

### ✅ Performance
- [x] Tailwind via CDN (script, não CSS bloqueante)
- [x] FontAwesome via CDN com preconnect
- [x] Imagens com `loading="lazy"` e `decoding="async"`
- [x] Zero JavaScript frameworks pesados
- [x] Single-file deployment (sem build step)

## 🕐 Horário de Funcionamento (automático)

O badge no header atualiza em tempo real (fuso de Brasília):

| Dia | Horário |
|---|---|
| Segunda a Sexta | 07:00 - 22:00 |
| Sábado | 08:00 - 21:00 |
| Domingo | 08:00 - 18:00 |

## 🔧 Personalizações Rápidas

| O que mudar | Onde encontrar no `index.html` |
|---|---|
| Cores da marca | Bloco `tailwind.config` no `<head>` |
| Horários | Função `updateStatus()` no `<script>` |
| Links/URLs | Atributos `href` dos botões |
| Textos | Diretamente no HTML |
| Pixel Meta | Comentário `<!-- META PIXEL -->` no `<head>` |
| GTM | Comentário `<!-- GTM -->` no `<head>` e `<body>` |

## 📝 Licença

Projeto proprietário — Rede Soma Drogarias © 2026. Todos os direitos reservados.
