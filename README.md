# Site — Advocacia Trabalhista para Varejo Alimentício

Site estático (1 arquivo `index.html`, sem build), inspirado no [vanlume-adv.vercel.app](https://vanlume-adv.vercel.app/), com as mudanças pedidas no `site.docx`:

- Foco em mercados, açougues, laticínios e padarias
- Cor principal trocada de marrom-chocolate para **bordô escuro `#4C0A14`**
- Nova seção **"Raio-X Trabalhista"** (diagnóstico gratuito)
- Lista de riscos reescrita para o varejo alimentício (câmara fria, escala 6x1, sazonalidade...)
- Bio da advogada reescrita (ex-empresária do setor de laticínios/frios)
- 3 novas perguntas no FAQ
- Botões duplos (Raio-X + WhatsApp) no hero, na seção de risco, na seção de atuação e no CTA final
- Logo maior no topo
- Meta tags de SEO atualizadas

## ⚠️ Falta você adicionar 3 imagens

Eu não recebo os arquivos de imagem que você colou no chat (só a "foto" da imagem, não o arquivo em si). Por isso o site está rodando com placeholders elegantes no lugar da logo e das fotos.

A pasta fica **direto na Área de Trabalho** (não dentro de `vanlume-adv-site`):

```
Área de Trabalho/
├── assets/              ← salve as imagens aqui
└── vanlume-adv-site/
    └── index.html
```

Salve os 3 arquivos dentro de `Área de Trabalho\assets\` **exatamente com estes nomes**:

| Arquivo a salvar | Onde aparece | Tamanho recomendado |
|---|---|---|
| `assets/logo.png` | Cabeçalho e rodapé | fundo transparente, altura ~400px |
| `assets/foto-hero.jpg` | Foto grande da seção inicial (topo) | retrato vertical, mín. 900×1100px |
| `assets/foto-perfil.jpg` | Foto da seção "A advogada" | retrato vertical, mín. 900×1200px |

Assim que os arquivos estiverem na pasta com esses nomes, é só recarregar a página — não precisa mexer em nada no código.

## Como ver o site agora

Abra uma pasta com um servidor local (necessário por causa das imagens) — já deixei um script pronto:

```bash
node serve.js 5174
```

Depois abra `http://localhost:5174` no navegador.

## Como publicar (deploy)

Como a pasta `assets/` está fora de `vanlume-adv-site/` (para ser fácil de achar), antes de publicar é preciso copiar as imagens para dentro da pasta do site. Me avise quando quiser publicar que eu faço essa cópia e deixo tudo pronto — ou, manualmente, copie `Área de Trabalho\assets` para dentro de `Área de Trabalho\vanlume-adv-site\assets`.

Depois é só arrastar a pasta `vanlume-adv-site` para o [vercel.com](https://vercel.com) (mesmo serviço do site atual, vanlume-adv.vercel.app) ou usar a Vercel CLI:

```bash
npx vercel --prod
```

## O que ainda pode ser ajustado

- O número de WhatsApp usado é o mesmo do site atual: `+55 (81) 99608-3815`. Se mudou, procure por `WA_NUMBER` no final do `index.html`.
- A logo tem um "fallback" em texto (MEVL) enquanto `assets/logo.png` não existir — ele some sozinho assim que você salvar o arquivo.
