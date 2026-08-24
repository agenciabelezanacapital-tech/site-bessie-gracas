# Bessie — Salão de Beleza

Site institucional do salão de beleza **Bessie**, construído em HTML, CSS e JavaScript puros (sem build, sem dependências).

## Serviços apresentados

Manicure e pedicure · Corte de cabelo · Escova · Maquiagem · Design de sobrancelha · Tratamento capilar · Penteado · Spa dos pés.

## Estrutura

```
site-bessie/
├── index.html    # Página (hero, serviços, sobre, diferenciais, depoimentos, onde estamos, agendar)
├── styles.css    # Estilos e responsividade (tokens de cor no topo do arquivo)
├── script.js     # Menu mobile, animações e agendamento via WhatsApp
└── README.md
```

## Como rodar localmente

Site estático — basta abrir o `index.html`. Para servir localmente:

```bash
python3 -m http.server 5173
# acesse http://localhost:5173
```

## Personalização (importante)

- **WhatsApp:** edite a constante `WHATSAPP` no topo de `script.js` (formato `55` + DDD + número, só dígitos). Atualize também os links `https://wa.me/5500000000000` no `index.html` (botão flutuante e rodapé).
- **Endereço, horários e contato:** na seção `#visite` do `index.html`.
- **Mapa:** substitua o bloco `.map-placeholder` por um `<iframe>` do Google Maps.
- **Cores da marca:** variáveis em `:root` no topo de `styles.css` (`--rose`, `--rose-deep`, `--gold`, `--cream`).
- **Fotos:** o hero e a seção "Sobre" usam blocos decorativos com emoji. Para fotos reais, troque o `background` de `.hero-photo` / `.about-photo` por `background: url('sua-foto.jpg') center/cover;` e remova o `::after`.
- **Textos e depoimentos:** todo o conteúdo (placeholder) está em `index.html`, em pt-BR.

## Deploy

Estático — publique em Vercel, Netlify ou GitHub Pages.

```bash
npx vercel
```

---
Fonts via Google Fonts (Playfair Display + Jost). Sem outras dependências externas.
