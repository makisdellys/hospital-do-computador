# Prompt-Mestre — Portal/PWA "Padre Pelágio Sauter, Apóstolo do Cerrado"

> **Como usar este documento:** este é um *prompt* completo, pronto para ser
> colado em outra sessão de IA generativa (ou entregue a uma equipe de
> desenvolvimento) para especificar e construir o Portal/PWA sobre a vida e
> obra do Padre Pelágio Sauter e sua ligação com a história de Goianira (GO).
> Ele não é, em si, o código do site — é o briefing completo que orienta
> quem for construí-lo.

---

## 1. Papel / Persona

Atue como um **conselho multidisciplinar** responsável por especificar e
orientar a construção deste portal, composto por:

- **Historiadores e pesquisadores de memória regional**, responsáveis pela
  exatidão factual da cronologia de Padre Pelágio e de Goianira;
- **Pedagogos e educadores patrimoniais**, responsáveis por tornar o
  conteúdo acessível a diferentes públicos (escolas, turistas, devotos,
  pesquisadores);
- **Curadores de acervo e bibliotecários digitais**, responsáveis pela
  organização cronológica de reportagens, vídeos, hemeroteca e biblioteca
  digital;
- **Assessoria eclesiástica / postulação da causa**, responsável pelo rigor
  e sobriedade ao tratar do processo de beatificação (Positio, título de
  Venerável) e dos relatos de fé;
- **UX/Produto e Engenharia de Software**, responsáveis pela arquitetura
  técnica do PWA, autenticação, loja, painel administrativo e doações.

Esse conselho deve, ao gerar qualquer conteúdo ou especificação,
**priorizar precisão histórica, sobriedade devocional e acessibilidade**
acima de qualquer efeito visual ou funcional.

---

## 2. Objetivo Geral

Criar um **Progressive Web App (PWA) multi-idiomas**, instalável e
responsivo, que seja o **acervo digital definitivo** sobre Padre Pelágio
Sauter — sua biografia, obra e papel fundador na história de Goianira — e
que também funcione como:

1. Portal de notícias e acompanhamento do **processo de beatificação**
   (Causa de Canonização / Positio) junto ao Vaticano;
2. Loja/plataforma de leitura do **livro digital** sobre sua vida;
3. Espaço de **arrecadação** (patrocínios e doações via Pix) para a
   manutenção do acervo e da causa;
4. Ferramenta pedagógica para escolas e pesquisadores sobre a fundação de
   Goianira.

**Critério de sucesso:** qualquer visitante — devoto, pesquisador,
estudante ou turista, em português, inglês, italiano ou espanhol — deve
conseguir, em poucos cliques, entender quem foi Padre Pelágio, como sua
atuação se entrelaça com o nascimento de Goianira, e acompanhar o estado
atual da causa de beatificação, com total confiança na exatidão das
informações.

---

## 3. Diretrizes de Precisão Histórica (regra de ouro)

- Todo conteúdo biográfico e histórico publicado deve ser **rastreável a
  uma fonte** (documento, jornal, ata, depoimento, registro paroquial).
- Este prompt traz, na Seção 12, uma **cronologia-semente** com base no que
  foi relatado por quem solicitou este projeto. Ela **deve ser tratada como
  ponto de partida, não como texto final** — é obrigatório validá-la e
  enriquecê-la com as fontes primárias do acervo do projeto (ex.: cronologia
  biográfica documental, linha do tempo do padre, linha do tempo de
  Goianira, hemeroteca digital "Apóstolo do Cerrado", material de
  homenagem) antes da publicação.
- Datas incertas ou conflitantes entre fontes devem ser marcadas no CMS
  como "a confirmar" e exibidas com nota editorial, nunca apresentadas como
  certeza absoluta.
- **Milagres e graças atribuídas** devem sempre ser apresentados como
  **relatos de fé/testemunhos**, com linguagem do tipo "segundo o relato
  de...", nunca como afirmação médica, científica ou jurídica de causa e
  efeito.
- Qualquer menção ao andamento da Causa de Beatificação (Positio, decretos,
  título de Venerável) deve citar a fonte oficial (Vaticano/Dicastério das
  Causas dos Santos, Arquidiocese, Congregação Redentorista) e a data da
  informação.

---

## 4. Público e Idiomas

- **Idiomas:** Português (padrão/fallback), Inglês, Italiano, Espanhol.
- Estrutura de rotas por idioma (ex. `/pt/`, `/en/`, `/it/`, `/es/`) com
  `hreflang` correto para SEO multilíngue.
- Conteúdo devocional/histórico deve ser traduzido por tradução
  profissional ou IA **com revisão humana** antes de publicar — não expor
  tradução automática crua em páginas de biografia ou liturgia.
- Público-alvo: devotos e fiéis; pesquisadores e historiadores; estudantes
  e escolas de Goianira/Goiás; turistas religiosos; comunidade ítalo/
  teuto-brasileira (origem do sobrenome Sauter); imprensa.

---

## 5. Mapa do Site / Arquitetura de Informação

### 5.1 Home — Landing Page
Minimalista e moderna: imagem/retrato icônico de Padre Pelágio, frase de
efeito, chamada para a linha do tempo, chamada para o livro digital, bloco
de notícias recentes sobre a Causa, bloco de doação via Pix, seletor de
idioma, acesso a login. Deve carregar rápido e funcionar perfeitamente em
celular (público majoritário devocional).

### 5.2 Biografia & Linha do Tempo Interativa
Timeline navegável (scroll ou cliques por década/evento) cobrindo desde o
nascimento até o reconhecimento como Venerável e a devoção atual — ver
cronologia-semente na Seção 12. Cada marco deve linkar para reportagens,
fotos ou documentos relacionados no Acervo/Galeria.

### 5.3 "Goianira: da Fundação à Emancipação"
Seção dedicada cruzando a biografia do padre com a história do município:
do povoado de São Geraldo ao Distrito de Goiânia (1933), Vila Itaim (1943),
Distrito de Goianira (1950) e emancipação como município (04/01/1959).
Pensada como recurso pedagógico para escolas locais.

### 5.4 Livro Digital
Três modalidades de acesso, todas **mediante login**:
- Leitura online (modo protegido/streaming de páginas, sem download livre);
- Compra do e-book (download protegido pós-compra, com DRM leve/marca
  d'água personalizada);
- Compra da versão impressa (com dados de frete e rastreio).

### 5.5 Portal de Notícias
Notícias gerais sobre o legado do padre e, em destaque, uma **trilha
dedicada ao andamento da Causa de Beatificação** (linha do tempo de
decretos, fases do Positio, reconhecimento de milagres, viagens a Roma,
pronunciamentos da Arquidiocese/Congregação Redentorista). Publicação
multi-idioma via painel administrativo.

### 5.6 Acervo (Hemeroteca Digital)
Reportagens, vídeos e matérias organizados **cronologicamente**, com
filtros por década, tipo de mídia e tema (fundação da cidade, vida
religiosa, processo de beatificação, homenagens). Base para isso: o
material de hemeroteca digital "Apóstolo do Cerrado" do acervo do projeto.

### 5.7 Depoimentos
Relatos de fiéis e graças atribuídas, com moderação obrigatória no painel
administrativo antes de publicação, consentimento expresso do autor (LGPD)
e linguagem de "testemunho de fé" (ver Seção 3).

### 5.8 Galeria
Fotos históricas e atuais (povoado, construção da Igreja Matriz, o sino
trazido de Minas Gerais, emancipação de 1959, velório, translados,
reconhecimento do Vaticano, festividades atuais), com legendas e fontes.

### 5.9 Biblioteca Digital
Documentos de referência: atas, cópias de jornais, materiais da Positio
(quando de domínio público), bibliografia, materiais pedagógicos para
escolas — organizados por categoria e pesquisáveis.

### 5.10 Patrocinadores e Doações (Pix)
Página de transparência com lista de patrocinadores institucionais e bloco
de doação via Pix (QR code dinâmico + chave copia-e-cola), com emissão de
comprovante e relatório simples de uso dos recursos.

### 5.11 Painel Administrativo
Ver Seção 8.

### 5.12 Login / Cadastro
Ver Seção 6.

---

## 6. Autenticação e Cadastro

Fluxo de autenticação **sem senha cadastrada pelo usuário**, com senha
temporária enviada por WhatsApp:

1. **Cadastro:** nome completo, número de WhatsApp (com verificação de
   formato/país), e-mail (opcional, para recuperação e notificações).
2. **Geração de senha temporária:** sistema gera código numérico/alfanumérico
   seguro e o envia via API oficial do WhatsApp Business.
3. **Validade de 24 horas:** a senha expira automaticamente após 24h;
   login após expiração exige solicitar novo código.
4. **Reenvio:** usuário pode solicitar novo código, com limite de
   tentativas/tempo para evitar abuso (rate limiting, proteção anti-spam).
5. **Segurança:** senha/código armazenado com hash (nunca em texto puro),
   números de WhatsApp tratados como dado pessoal sensível (LGPD),
   registro de consentimento no cadastro.
6. **Sessão:** após validar o código, emitir sessão/token (ex. JWT) com
   expiração própria, renovável por refresh token.
7. **Login obrigatório** para: leitura/compra do livro digital, acesso à
   área de compras/pedidos, envio de depoimentos.

---

## 7. Loja do Livro Digital

- Catálogo com o(s) livro(s) sobre Padre Pelágio (e-book e impresso).
- Checkout com meios de pagamento nacionais (cartão, Pix).
- Pós-compra: liberação automática de acesso à leitura online/download do
  e-book vinculado à conta do usuário; para impresso, geração de pedido com
  endereço de entrega e rastreio.
- Proteção de conteúdo: leitura online sem permitir download bruto do PDF
  completo; e-book comprado com marca d'água de identificação do
  comprador.

---

## 8. Painel Administrativo (CMS)

Funcionalidades mínimas:

- Gestão de conteúdo multi-idioma (biografia, linha do tempo, notícias,
  acervo, biblioteca, galeria) com fluxo de rascunho → revisão → publicação;
- Gestão de usuários e logins (bloqueio, histórico de acessos);
- Gestão de pedidos (e-book e impresso) e status de entrega;
- Gestão de doações via Pix (conciliação, emissão de recibos, relatório de
  transparência);
- Moderação de depoimentos (aprovar/rejeitar/editar antes de publicar);
- Publicação de notícias e atualizações da Causa de Beatificação, com
  campo obrigatório de "fonte";
- Métricas básicas (acessos por idioma/página, conversão da loja, total
  arrecadado).
- Controle de permissões por papel (ex.: editor de conteúdo, financeiro,
  moderador, administrador geral).

---

## 9. Doações via Pix

- Chave Pix institucional configurável pelo admin, com geração de QR code
  dinâmico por valor/campanha quando aplicável;
- Opção de doação com valor livre ou sugerido;
- Emissão de comprovante/recibo (e-mail, se informado);
- Página de transparência mostrando, de forma simples, a destinação dos
  recursos (manutenção do acervo, causa de beatificação, obras sociais
  ligadas à memória do padre, conforme aplicável).

---

## 10. Requisitos Técnicos (PWA)

- **Instalável** (manifest + ícones + service worker), com funcionamento
  básico offline (ao menos páginas estáticas de biografia/linha do tempo
  em cache);
- **Responsivo** mobile-first (público majoritário acessa via celular/
  WhatsApp);
- **Performance**: carregamento rápido mesmo em conexões móveis mais
  lentas do interior de Goiás;
- **SEO multi-idioma**: `hreflang`, sitemap por idioma, dados estruturados
  (schema.org Article/Person/Event) para biografia e notícias;
- **Acessibilidade** (WCAG AA): contraste, navegação por teclado, textos
  alternativos em fotos históricas;
- **LGPD**: política de privacidade clara sobre uso de WhatsApp/telefone,
  consentimento explícito, direito de exclusão de conta e dados.

---

## 11. Diretrizes de Design

- Visual **minimalista e moderno**, mas com tom **institucional e
  devocional** — nunca comercial ou "pop" demais;
- Paleta sóbria (tons terrosos do Cerrado + um tom litúrgico/eclesiástico,
  ex. dourado ou vinho, usado com moderação);
- Tipografia legível, hierarquia clara entre "fato histórico" e
  "testemunho de fé";
- Fotografia histórica em preto e branco tratada com cuidado (sem filtros
  exagerados), separada visualmente de conteúdo institucional atual.

---

## 12. Cronologia-Semente (conteúdo histórico inicial — validar com fontes originais)

> ⚠️ **Importante:** a cronologia abaixo foi fornecida verbalmente por quem
> encomendou este projeto, como ponto de partida. **Não deve ser publicada
> sem conferência** com as fontes primárias do acervo (cronologia
> biográfica documental, linha do tempo do Padre Pelágio, linha do tempo de
> Goianira, hemeroteca digital "Apóstolo do Cerrado", material da homenagem
> de 2026) e, idealmente, com registros paroquiais/municipais oficiais.

- Padre Pelágio Sauter, religioso redentorista, chega a Goiás e inicia seu
  trabalho de evangelização a partir de Trindade (GO).
- Reúne-se com fazendeiros da região e forma uma comissão para a criação de
  um povoado.
- Fixa o cruzeiro simbólico e batiza o povoado nascente de **São Geraldo**,
  dando-lhe como padroeiro **São Geraldo Magela**.
- O povoado é agrupado como **Distrito de Goiânia**, nova capital do estado
  fundada em **1933**.
- Cria a comissão para a construção da primeira **Igreja Matriz de São
  Geraldo**; levanta fundos e viaja a Minas Gerais para buscar o sino da
  igreja.
- O distrito muda de nome: de **Distrito de São Geraldo** para **Vila
  Itaim**, em **1943**, e depois para **Distrito de Goianira**, em **1950**.
- Esteve presente na solenidade oficial de **emancipação política** e
  transformação em **município de Goianira**, em **04/01/1959**.
- Faleceu em **1961**, em Goiânia. Seu primeiro velório reuniu uma
  multidão estimada em mais de **50 mil pessoas** (cerca de metade da
  população de Goiânia na época).
- Foi sepultado inicialmente no **Cemitério Santana**, em Campinas
  (Goiânia).
- Seu corpo foi posteriormente transladado para a **Igreja Matriz de
  Campinas**, sede dos Redentoristas, onde exerceu seu ofício paroquial até
  os últimos dias de vida.
- Foi transladado novamente, sendo criado seu **túmulo oficial na Igreja de
  Trindade**, de onde iniciou seus trabalhos ao chegar a Goiás.
- Foi aberto o processo de **Positio**, enviado ao Vaticano, documentando
  sua vida e obra para fins de beatificação.
- Em **2014**, o **Papa Francisco** reconheceu formalmente seu trabalho
  pela fé, pela Igreja e pela humanidade, concedendo-lhe o título de
  **Venerável**.
- É hoje aclamado por devotos como o **"Apóstolo do Cerrado"**, com relatos
  de graças e milagres atribuídos à sua intercessão.

---

## 13. Conformidade e Ética

- **LGPD**: dados de cadastro (nome, WhatsApp, e-mail), compras e
  depoimentos são dados pessoais; definir base legal, retenção e processo
  de exclusão a pedido do titular.
- **Direitos de imagem**: fotos históricas e depoimentos devem ter
  autorização/registro de consentimento, especialmente para pessoas vivas.
- **Relatos de fé vs. fato**: reforçar, em toda a plataforma, a separação
  entre informação histórica verificável e testemunho religioso/milagre
  (ver Seção 3) — essencial também por ser matéria de processo oficial de
  beatificação em andamento.
- **Transparência financeira** nas doações via Pix e vendas do livro.

---

## 14. Entregáveis Esperados de Quem Receber Este Prompt

1. Arquitetura técnica proposta (stack, banco de dados, hospedagem,
   integração com API do WhatsApp Business e com provedor de Pix);
2. Wireframes/mockups da Home e das páginas-chave (Biografia/Linha do
   Tempo, Livro Digital, Acervo, Painel Administrativo);
3. Modelo de dados (usuários, pedidos, conteúdo multi-idioma, depoimentos,
   notícias, doações);
4. Especificação detalhada do fluxo de autenticação via WhatsApp;
5. Plano de i18n (estrutura de rotas, fluxo de tradução/revisão);
6. Plano de testes de aceitação cobrindo cada item das Seções 5–10 deste
   documento;
7. Plano de carga inicial de conteúdo, condicionado à validação da
   cronologia (Seção 12) contra as fontes primárias do acervo do projeto.
