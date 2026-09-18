# Sintonia+ — landing page

Landing page única (`index.html`, sem build, sem dependências de servidor) para divulgar planos de revenda IPTV. HTML5 + CSS3 moderno (grid, clamp, custom properties) + JavaScript puro (menu mobile, accordion de FAQ, toggle mensal/anual, animações de entrada). Fontes carregadas via Google Fonts (gratuito).

## Já configurado

- **WhatsApp**: `5511981219974` (todos os botões e o link flutuante já usam esse número).
- **Preços sugeridos**: plano único, três períodos — Mensal R$ 29,90/mês, Trimestral R$ 24,90/mês (cobrado R$ 74,70 a cada 3 meses, economia de 17%), Anual R$ 19,90/mês (cobrado R$ 238,80/ano, economia de 33%). Preços "quebrados" (,90) e desconto crescente por período são de propósito: é o padrão que mais converte em assinaturas de streaming no Brasil.
- **3 telas simultâneas** incluídas em todos os planos (aparelhos iguais ou diferentes) — destacado acima da grade de preços.
- **Guia de programação** do hero é interativo (abas Ao vivo / Filmes / Séries) com categorias genéricas — ver nota abaixo sobre por que não usei nomes de canais reais.

## Antes de publicar, troque:

- **E-mail**: `contato@sintoniaplus.com.br` no rodapé.
- **Depoimentos**: são ilustrativos, substitua pelos relatos reais dos seus clientes.
- **Nome/marca**: se quiser trocar "Sintonia+", busque por `SINTONIA` e `Sintonia+` no arquivo (aparece no `<title>`, header, footer e textos dos botões do WhatsApp).
- **Aviso legal do rodapé**: lembre de garantir que a distribuição de conteúdo está de acordo com a legislação de direitos autorais e telecomunicações da sua região antes de divulgar.

## Por que o guia não lista canais reais (Sportv, Premiere...), apps de terceiros ou conteúdo adulto

Optei por manter categorias genéricas (Esporte Total, Cinema, Séries etc.) em vez de nomes reais de emissoras/canais pagos, não incluí os apps de player mostrados na imagem enviada (Duplex Play, Magic Player, Play Sim e similares) e não adicionei menção a conteúdo adulto na página. Esses três elementos juntos — canais pagos de terceiros oferecidos fora do canal oficial, esses aplicativos específicos e a combinação com conteúdo adulto — são exatamente o padrão que a Polícia Federal e a Anatel têm alvo em operações contra IPTV pirata no Brasil (ex. Operação 404), então não me sinto à vontade em ajudar a divulgar isso, independente da intenção. Se o seu serviço tem distribuição licenciada de fato, você pode adicionar esses elementos por conta própria; do meu lado, prefiro manter o site pronto para uso legítimo.

## Hospedagem 100% gratuita

O site é só HTML/CSS/JS estático — qualquer uma das opções abaixo hospeda de graça, com HTTPS automático, e aceita domínio próprio depois (o domínio em si é pago, a hospedagem não):

### Opção mais rápida (sem git): Netlify Drop
1. Acesse https://app.netlify.com/drop
2. Arraste a pasta `sintonia-plus` inteira para a página.
3. Pronto — você recebe uma URL pública em segundos. Pra atualizar, arraste a pasta de novo.

### Opção recomendada (com git, atualiza sozinho a cada mudança): Vercel ou Cloudflare Pages
1. Crie um repositório no GitHub e suba esta pasta:
   ```
   cd sintonia-plus
   git init
   git add index.html README.md
   git commit -m "Landing page Sintonia+"
   git branch -M main
   git remote add origin https://github.com/SEU-USUARIO/sintonia-plus.git
   git push -u origin main
   ```
2. Entre em https://vercel.com (ou https://pages.cloudflare.com) e faça login com sua conta do GitHub.
3. Clique em "Add New Project" / "Create a project" e selecione o repositório `sintonia-plus`.
4. Não precisa configurar nada (não há build) — clique em Deploy.
5. Em poucos segundos você recebe uma URL do tipo `sintonia-plus.vercel.app`. A cada `git push`, o site atualiza sozinho.
6. Domínio próprio (opcional): compre um domínio (ex. no Registro.br) e conecte em Project Settings → Domains — a hospedagem continua gratuita.

### Alternativa: GitHub Pages
1. Suba o repositório no GitHub (passos acima).
2. Vá em Settings → Pages → Branch: `main` → pasta `/root` → Save.
3. Seu site fica em `https://SEU-USUARIO.github.io/sintonia-plus/`.

Qualquer uma das três resolve — Netlify Drop é o caminho mais rápido para testar hoje mesmo; Vercel/Cloudflare Pages ou GitHub Pages são melhores se você for atualizar o site com frequência.
