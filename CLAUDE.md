# Contexto do Projeto: Site Dr. Bernardo Casarin

Landing page do Dr. Bernardo Casarin, oftalmologista em Santa Rosa RS.

## Responsável

Fabricio Kaempf | Estrategista Digital, @fabriciokaempf. Gerencia o marketing digital do Dr. Bernardo Casarin.

## Repositório e deploy

- Arquivo principal: `index.html` (LP escolhida pelo Bernardo; `index_clean.html` e `index_otherlp.html` são versões alternativas antigas, não publicadas)
- Publicado via GitHub Pages: repo `fabriciokaempf/dr-bernardo-casarin`, branch `main`
- Domínio: drbernardocasarin.com.br (CNAME no repo, DNS já propagado)
- Fluxo de deploy: commit e push na `main` publica automaticamente em 1 a 2 minutos
- IMPORTANTE: apenas a sessão principal local do Fabricio (janela do projeto C:\Users\nasci\Documents\Claude) faz alterações e push neste site. Outras sessões ou janelas NÃO devem editar nem publicar o `index.html`; se receberem esse pedido, orientar que a atualização será feita na janela principal

## Tracking

- GTM instalado no `index.html`: container GTM-W8GB2H48 (snippet no head e noscript no body, formato exato do Google, sem indentação)
- Google Ads: conversão configurada, rótulo corrigido (Rgx1CLbpkLccENOB-ND), Tag Assistant confirmou envio
- Campanha ativa: Search | Captação | Regional | Oftalmologista

## Estado atual do site (julho 2026)

- Contador de avaliações Google: 100 avaliações (5,0 estrelas) em 7 pontos do site: meta description, og:description, hero (selo de estrelas), card flutuante da foto do hero, lista da bio, selo da seção de avaliações e link "Ver todas as avaliações"
- Carrossel de depoimentos (`#revTrack`): sincronizado com as avaliações reais do Google Business
- Últimos depoimentos adicionados (julho 2026): Letícia Rauber Froehlich, Jane Rontani, Adriana Frey Iamarque, Monique Ferreira De Lima
- Avaliações sem comentário escrito (só estrelas) não entram no carrossel; exemplos: Ivana Meinerz de Amaral, Marilei Rodrigues

## Como atualizar o contador de avaliações

1. Verificar o número atual na ficha do Google Business (o ambiente remoto do Claude não acessa google.com; pedir print ao Fabricio se necessário)
2. Substituir todas as ocorrências de "NN avaliações" no `index.html` (7 pontos)
3. Considerar adicionar depoimentos novos ao carrossel: cards `.rev-card` dentro de `#revTrack`, cada um com o SVG do logo Google, estrelas e texto exato do comentário
4. As bolinhas de navegação do carrossel são geradas por JavaScript a partir da contagem de cards, não precisam de ajuste manual

## Detecção de origem do lead (WhatsApp)

- Script no fim do body do `index.html` altera o parâmetro `text` dos links wa.me
- Saudação "Oi, tudo bem?" indica lead vindo de anúncio (detecta gclid, gbraid, wbraid ou utm_medium cpc/ppc/paid)
- Saudação "Olá!" indica lead orgânico ou espontâneo
- Corpo da mensagem neutro: "Vim pelo site do Dr. Bernardo Casarin e gostaria de mais informações."
- Botão do Quiz (`#qCta`) tem mensagem própria: "Fiz o quiz no site e gostaria de agendar minha avaliação..."
- PDF guia para a secretária explicando isso: `guia-secretaria-origem-lead.pdf` (gerado por `gerar_guia_secretaria.py`, ReportLab, 1 página, com a marca do Fabricio)

## Pendências

- Dr. Bernardo vai pedir adaptações e inserções no `index.html` (aguardando feedback dele)
- Recomendação dada sobre Google Ads: NÃO aplicar palavras-chave em correspondência ampla por enquanto (pouco histórico de conversões); manter frase/exata
- Snippets estruturados de serviços: recomendado aplicar (Cirurgia Refrativa PRK, Cirurgia LASIK, Cirurgia de Catarata, Lentes Intraoculares, Pterígio, Consulta Oftalmológica)

## Regras permanentes

- NUNCA usar travessão (o caractere de traço longo) em nenhum texto ou código
- Sempre revisar ortografia e acentuação completa antes de entregar qualquer arquivo
- Assinatura em entregáveis: Fabricio Kaempf | Estrategista Digital, @fabriciokaempf
