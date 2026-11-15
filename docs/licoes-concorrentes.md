# O que aprender com os 789 repositórios

Lições tiradas dos READMEs e dos documentos de método, validação, decisões, demo e uso de IA dos outros times, lidos em [data anterior a 14/11/2026] (repositórios 1 a 27), em [data anterior a 14/11/2026] (28 a 56) e em [data anterior a 14/11/2026] (57 a 111) em [data anterior a 14/11/2026] (112 a 124), em [data anterior a 14/11/2026] (125 a 169) e em 14/11/2026 (170 a 292, 293 a 336 às 10h e 337 a 352 às 11h, 356 a 362 às 12h, 363 a 391 às 15h30, 392 a 413 às 16h, 416 a 434 às 17h, 435 a 467 às 22h e 468 a 482 às 23h; e em 15/11/2026, 483 a 487 à meia-noite, 488 a 524 à 1h, 525 a 541 às 2h, 542 a 554 às 3h, 555 a 573 às 4h, 574 a 592 às 5h, 593 a 601 às 6h, 602 a 617 às 7h, 618 a 641 às 8h, 642 a 667 às 9h e 668 a 696 às 10h, e 697 a 789 às 14h, só pelos metadados), mais as mudanças nos antigos. As lições 128 a 131 vêm da vigésima quarta inspeção, em 15/11/2026, às 14h. As lições 45 a 49 vêm da inspeção dos sites no ar, em [data anterior a 14/11/2026] à noite, as 50 a 55 da leitura e da inspeção de [data anterior a 14/11/2026] e as 56 a 62 do primeiro dia do evento, 14/11/2026, e as 63 a 65 da inspeção das 10h do mesmo dia, e as 66 a 68 da inspeção das 11h, e as 69 e 70 da inspeção das 12h ([sites-concorrentes.md](sites-concorrentes.md)). A lista dos repositórios está em [repos-concorrentes.md](repos-concorrentes.md) e a análise geral em [concorrencia.md](concorrencia.md).

Aprender com métodos e fontes públicas é estudo. Copiar código de outro time, não. Os números citados aqui são o que cada time declara: não rodei nada. Antes de usar um número deles, conferir no artigo original.

## As 12 lições que mais mudam o nosso plano

1. **Pergunte ao Local Lead as regras do evento local.** O evento de Bangladesh tem uma "Stage 1" que pedia um link público do GitHub até 7/10 (SIGHTLINE, decisão D-010). Eventos locais podem ter prazos e regras próprios. O SIGHTLINE listou três perguntas que também valem para nós: (a) pode ter documento de conceito antes do evento? (b) pode baixar dados públicos antes? (c) pode ter templates genéricos prontos?
2. **Um PROMPT.md preparado antes é legítimo, e o BroBYW mostra como.** O arquivo deles foi escrito para ser colado no Claude Code em 14/11: visão do produto, funcionalidades P0/P1/P2, métricas definidas e a regra "o enunciado oficial vence". Eles acabaram começando antes, por escolha. Nós podemos preparar o mesmo documento e só usá-lo em 14/11.
3. **A coordenada publicada quase nunca é o ponto certo.** Mover 51 m levou o ponto de Shackleton do Mazarico [período anterior] de 0% para 72% de Sol (BroBYW). O centro do quadrado do SIGHTLINE em Shackleton caiu numa parede de cratera com 11% de Sol e Terra nunca visível. A regra dos dois times é a mesma: usar o ponto mais alto dentro da região, ou dentro de 250 m da coordenada publicada.
4. **Validar só contra estudos que usaram LOLA.** Bryant [período anterior] (radar de Goldstone), Bussey [período anterior] (Kaguya) e Speyerer [período anterior] (imagens) usaram outros mapas, e as coordenadas deles não batem com o LOLA (BroBYW). Os pares bons para comparar são o Gläser [período anterior]/[período anterior], o Barker [período anterior] e os mapas do PGDA 69 / AVGVISIB.
5. **Comparar as mesmas métricas e a mesma altura.** O BroBYW calcula as três definições (fração média do disco, "algum pedaço do Sol" e "Sol inteiro") na mesma altura do estudo. A 0 m o resultado cai muito (55,7% contra os 76% do Gläser), porque o relevo dos primeiros metros passa a mandar.
6. **Os primeiros 30 m mandam no resultado com mastro baixo.** No Connecting Ridge, o SIGHTLINE achou 24,8% de Sol sem mastro e 35,2% com 2 m. O DEM de 5 m perto do sítio é obrigatório, e a altura do mastro precisa ser um controle visível.
7. **A máscara de horizonte é barata.** O POLAR WINDOW mediu ~130 ms por sítio (43 ms com numba) para 1.440 raios até 50 km. Isso derruba a premissa de que só dá para pré-calcular: dá para calcular coordenadas livres na hora.
8. **Não é preciso baixar o DEM inteiro.** O POLAR WINDOW lê só uma janela de 20 km em volta de cada sítio, com requisições HTTP de intervalo (range), sem baixar o arquivo de 1,85 GB.
9. **Fixar a tolerância antes de rodar o teste e incluir um controle negativo.** O SIGHTLINE escreveu o limite de 0,02° antes de existir qualquer resíduo e testou que um deslocamento de 10 min ou de 0,01° na longitude quebra o teste. Isso convence um juiz.
10. **Separar geometria de sobrevivência.** Dois dos três landers CLPS que pousaram terminaram com Sol e Terra ainda visíveis (POLAR WINDOW). A ferramenta diz quando há luz e contato. Não diz se a missão sobrevive.
11. **Uma frase de validação que qualquer um entende.** "O pôr do Sol do Blue Ghost 1 caiu no dia em que a NASA anunciou o fim da missão" (POLAR WINDOW, [data anterior a 14/11/2026], ±32 min). Cabe num slide.
12. **Na demo, só números de uma tabela fechada.** O SIGHTLINE proíbe ler na gravação um valor que não esteja numa tabela com definição e fonte, e proíbe dizer "validado no sítio": o certo é "conferido". Também proíbe o logo da NASA e pessoas menores de 18 no vídeo.

## Lições novas de 14/11/2026

Vêm do primeiro dia do evento: os repositórios 170 a 292, os 42 projetos já enviados no site do Space Apps e os sites que abri. O que é de repositório ou de site é o que o time declara ou mostra.

56. **O Occluder deixou de ser só nosso.** O 170 (Purple Haze, Surat) diz no ar "última luz em 56 min, atrás do relevo perto da cratera Henson, 8,1 km, 236°" e nomeia o morro que esconde a Terra (Mons Malapert, 138 km), pelo gazetteer da IAU, como nós. No pitch não dá mais para dizer "ninguém faz". O que dá para dizer é o que só nós juntamos: os 130 sítios do Wueller, português, a escada de resolução na tela e a história do IM-2.
57. **A hora "sem relevo" ao lado da contagem.** O 170 escreve, embaixo de cada pôr do Sol, quando ele aconteceria num horizonte plano ("88,1 d depois") e tem uma faixa "plano 0°" na linha do tempo. É a prova mais curta de que o relevo manda, e é a mesma ideia do botão do 4 (lição do repositório 4), agora na contagem.
58. **Pousos reais com controle negativo, e o critério escrito.** O 170 roda o motor para trás em cinco pousos e marca o IM-1 e o IM-2 como "a luz não foi o limite". Ele conta o Blue Ghost 1 como acerto por cair a 4,6 h do fim registrado; a nossa página de prova marca o Blue Ghost 1 como falha. São critérios diferentes, não um erro de um dos dois. Não mexer na nossa tolerância: vale deixar escrito na página de prova qual é o critério e por que (lição 9).
59. **O primeiro envio foi às 23:58 UTC de 13/11.** Às 09:00 UTC de 14/11 já havia 42 projetos enviados neste desafio, quase todos de Bangladesh, Malásia, Índia, Emirados e Cairo, quase todos com vídeo no YouTube e link de demo. Os links de projeto mostram o que um juiz vai abrir primeiro: um site no ar ou um repositório. Três times enviaram o endereço do próprio Space Apps como link do projeto.
60. **Português deixou de ser só nosso.** O 194 (ViaLunae, time Via Lunae, de Fortaleza) diz ser PT/EN, com horizonte ainda liso. Na fase local de Guarulhos isso não pesa; na global, o português continua raro, mas não é exclusivo.
61. **Responder "quando?" em uma linha.** O Wasl (182) abre com o melhor, o típico e o pior dia de pouso do ano no sítio; o Orrery Space ordena todos os sítios numa tabela na mesma tela e oferece cenários com nome de história ("a Terra logo atrás de uma crista", "o fundo do Shackleton nunca iluminado"). Os cenários com nome servem de roteiro para o vídeo sem código novo.
62. **Começar antes com o aval do Local Lead.** O README do 170 diz que o protótipo começou antes do evento com a aprovação do Local Lead dele. É a pergunta que está aberta para nós desde a lição 1: a resposta do nosso Local Lead vale mais do que qualquer leitura da regra.
63. **Duas portas na mesma página: planejador e aluno** (14/11/2026, às 10h). O TrueSouth (Cairo, [truesouth.abdallahmostafa.com](https://truesouth.abdallahmostafa.com/)) abre com a pergunta e dois caminhos: "Mission Control", com perfis de missão reais como o do IM-2, e uma "Academia" de 8 lições curtas para estudantes. É a nossa frase "para um professor tanto quanto para um planejador" posta em tela. Ligado ao #174 (número de aula).
64. **A dispersão do pouso cabe numa faixa de uma linha** (14/11/2026, às 10h). O TrueSouth escreve "em 160 m: 39% a 87% de Sol" ao lado do sítio, com um botão para ir ao ponto mais iluminado. É o jeito mais curto que vi de contar a história do IM-2 sem gráfico. Ligado ao #176.
65. **Comparar a iluminação média com o PGDA é o novo padrão de validação** (14/11/2026, às 10h). O 293 declara 60 pontos sorteados em estratos de iluminação, diferença média de 0,58 ponto percentual no Sol e 0,53 na Terra, r = 0,999, e diz que nada foi ajustado; o 294 (Quiral Labs, Campina Grande) e o Sunchaser fazem o mesmo tipo de conta. Se a nossa prova só tem efemérides e pousos, falta essa linha. Conferir o número no repositório antes de citar.
66. **Duas leituras, a cautelosa e a otimista, são a incerteza mais barata** (14/11/2026, às 11h). O 338 (LUNAR//SHIFT, Seul, [site](https://serin30.github.io/lunar-shift/)) julga cada data duas vezes: com mais da metade do disco do Sol e a Terra 0,5° acima do relevo, e com um décimo do Sol e a Terra rente. Quando discordam, a tela mostra a cor mais cuidadosa. Enquanto a faixa do DEM (#49) não existe, é uma forma honesta de dizer "depende" sem gráfico novo.
67. **A folga de atraso cabe na frase principal** (14/11/2026, às 11h). O LunarLink_JO (Amã, [lunarlinkjo.web.app](https://lunarlinkjo.web.app)) e o 338 dizem, logo depois do veredito, quantos dias o pouso ainda aguenta escorregar ("1 dia de folga"). O nosso #175 já calcula isso; falta subir para a frase.
68. **Os 130 sítios do Wueller já estão em outro site** (14/11/2026, às 11h). O LunaNav (base44, evento universal) usa o conjunto do Wueller et al. 2026 (Zenodo 17084058) para ranquear 78 sítios por dias seguidos de Sol ou de Sol e Terra, só com os valores publicados. O 300 e o SELENE usam um ponto por região com o código do Wueller. O que segue só nosso é calcular a geometria nesses sítios e dizer o Occluder, não a lista.
69. **Um calendário de 365 dias responde "quando?" e defende vários sítios** (14/11/2026, às 12h). O 357 ([site](https://lunar-landing-navigator.streamlit.app/)) pinta cada dia do ano por sítio: dá ou não dá 6,5 dias seguidos de Sol, e quanto da estadia tem a Terra. Fecha com "em 19 de 365 dias nenhum sítio serve". É o melhor/típico/pior dia em forma de figura, e um argumento pronto para o pitch.
70. **Validação em cinco linhas com Δ cabe num slide** (14/11/2026, às 12h). O SelenoGrid (356, [site](https://hatim-a.github.io/selenogrid/)) mostra azimute e elevação do Sol e da Terra e o diâmetro da Terra em Shackleton, o valor dele, o do Horizons e a diferença. O ranking dele usa TOPSIS com pesos e avisa que a nota "não é probabilidade".
71. **Mostrar as falhas na página de validação** (14/11/2026, às 15h30). O SunSight (363, [site](https://gursimranjs.github.io/sunsight/)) declara 8 checagens, 4 passam, 2 falham e 2 passam em parte, e deixa as falhas na página com a causa provável. Para a nossa Prova: não esconder o que não passa dá mais confiança que um muro verde.
72. **O atraso de lançamento virou a pergunta de abertura** (14/11/2026, às 15h30). O Lunar Window (364, [site](https://machinedramon.github.io/lunar-window/)) abre com "quando o lançamento atrasa, veja o que ainda funciona" e calcula um ano de janelas para 15 sítios e 72 pontos vizinhos no navegador. Já são três sites com atraso de lançamento (364, 368 e o LunarLink).
73. **Assistente de IA com a chave do visitante** (14/11/2026, às 15h30). O VNI (366, [site](https://vni-moon-navigator.vercel.app)) põe o assistente atrás da chave do próprio visitante, guardada só na aba, e limita as respostas aos números calculados. É uma saída para o assistente que o Luiz decidiu trazer sem custo de API nosso.
74. **Validar contra fotos datadas, com controle negativo** (14/11/2026, às 16h). O Sightline (392, [site](https://lunarsightline.com)) confere se o modelo tinha o chão iluminado no momento de cada foto do LROC: declara 92% de acerto em 235 fotos de 8 pontos, e 32% com o Sol meio mês fora do lugar. É observação, não outro modelo. Nós validamos contra Horizons e PGDA, não contra fotos.
75. **"Conferir no Horizons" ao lado de cada número** (14/11/2026, às 16h). O Sightline põe sob o Sol e a Terra um link com a consulta pronta ao Horizons para aquele sítio e aquela hora. O juiz confere sem ler a página de prova.
76. **O critério da Terra muda o resultado em um dia** (14/11/2026, às 16h, pela consulta de referência). No Connecting Ridge, de 01/12/2026, o Dawnline (393) e nós damos 46,8% de Terra visível contando o centro; o Sunchaser (125) e o Sightline (392) dão cerca de 360 h, 29 h a mais. Quem não diz o critério na tela parece errado para quem compara.
77. **A contagem pode vir como janela, pela incerteza do relevo** (14/11/2026, às 17h). O Ridgeline (65, [site](https://ridgeline-taupe.vercel.app)) não dá uma hora para o nascer da Terra: dá "entre 12 d 14 h e 12 d 17 h", e explica que a janela supõe ±0,1° no relevo. O Lunaris (346, [site](https://lunaris-lovat.vercel.app)) refaz o risco "com o erro do mapa de altura (0,6 m, horizonte até 0,35° mais alto)". É a forma mais barata da nossa faixa do DEM (#49): uma frase, no lugar onde a pessoa lê o número.
78. **O plano B cabe numa linha** (14/11/2026, às 17h). O 220 ([site](https://projeto analisado-sigma.vercel.app)) abre com "Launch slipped? Pick the new date – we rank the sites" e responde: "Becomes GO if you land 10 days later (2026-12-11)", o melhor sítio na nova data e "Move 3.9 km E" com o ganho. É o que a #246 pede, já com a frase pronta.
79. **Um teste de estresse que muda o veredito é validação** (14/11/2026, às 17h). O LunaMargin (176, [site](https://lunamargin.vercel.app)) soma 0,02° ao horizonte e mostra que no ROI 4 o resultado cai de 9/9 para 8/9 pontos ("perturbation changed the verdict"). Não precisa de clones do DEM e mostra onde a resposta é frágil.
80. **O português deixou de ser só nosso** (14/11/2026, às 17h). O 166 ([site](https://projeto analisado-theta.vercel.app)) tem a interface inteira em português, com LOLA de 80 m, SPICE e a linha do Horizons. Ainda é o único outro, e não tem data livre nem Occluder; mas "o único em PT" sai do pitch.
81. **O Bussey [período anterior] confirma a lição 4, com número** (14/11/2026, às 17h). O Lunar Window (416, [site](https://adqm0001.github.io/lunar-window/)) compara a parte do ano com Sol nos cinco "picos de luz" com o Bussey [período anterior] e acha 3,7 pontos de diferença média, até +7,2 no Connecting ridge B. Explica: as coordenadas do artigo caem 50 a 160 m abaixo do cume no LOLA, e só o cume do LOLA bate. É a mesma armadilha do nosso Wueller, que falha na Prova (75 de 130 dentro de 1 dia).
82. **1,8 km mudam o nascer da Terra em 11 h** (14/11/2026, às 17h, pela consulta de referência). No Connecting Ridge, de 01/12/2026, o Horizon404 (250) e o Lunaris (346), os dois em 89,45°S 222,69°E, põem o nascer da Terra em 14/12 perto das 03h UTC. Nós, em 89,4661°S 136,949°W, às 16:05 de 13/12; o Ridgeline (89,4395°S) dá entre 14h e 17h de 13/12; o LunaMargin (89,4389°S 222,904°E) dá 331,8 h de Sol e Terra juntos, contra as nossas 331,4. Quem compara números do Connecting Ridge precisa dizer qual ponto usou. Na tela, a coordenada ao lado do nome (que já temos) é o que permite essa conferência.

83. **Na Athena, o Sol começa cortado pelo relevo** (14/11/2026, às 22h, pela consulta de referência). Em [data anterior a 14/11/2026] 00:00 UTC, no ponto do IM-2, quatro sites dizem a mesma coisa: o Apollo Harness ([site](https://apolloharness.web.app)) põe o Sol a 1,73° com o horizonte a 1,81°, 30% do disco, nascendo em 37 min; o GIT_HAPPENS (453) dá os mesmos 1,73° e 1,82°; o Ribbon (447) dá "o Sol escondido no pouso, volta em 0,7 h"; o 456, "volta em 15 min". O Ridgeline já dava 31% do disco. As nossas 48 h de Sol contam qualquer pedaço do disco (a API dá um só período de Sol de 00:00 a 48:00), e a fração média de 97,5% é o número que carrega esse começo. Os quatro não contradizem o nosso; dizem com mais clareza que a primeira meia hora é de Sol cortado. No código, o `Sky` usa a fração do disco de cada instante para iluminar a cena (`now.sun.fraction`), mas não achei um número dessa fração no Cursor; o `Numbers` só mostra a média.
84. **A regra do disco pode ir para a tela como faixa** (14/11/2026, às 22h). O GIT_HAPPENS (453, [site](https://projeto analisado-beige.vercel.app)) deixa escolher "qualquer pedaço", "centro" ou "disco inteiro" e mostra ao lado de cada porcentagem a faixa do disco inteiro ao qualquer pedaço. No nosso ponto do Connecting Ridge, com qualquer pedaço da Terra, ele dá 50% contra os nossos 46,8% pelo centro. O Apollo Harness, no mesmo ponto, conta 82% do disco da Terra à vista como "contato marginal". É a dúvida da lição 76 e da #245, resolvida com um número em vez de uma frase.
85. **A 500 m da crista, o Sol some por 4,6 dias** (14/11/2026, às 22h, pela consulta de referência). O Ribbon (447, [site](https://kakaman-kakaman.github.io/lunar-ribbon/)) põe o centro do sítio 1 do Goddard (89,460°S 137,500°W, a 0,5 km do nosso ponto) com o Sol escondido em 01/12/2026 "por relevo a 0,1 km" durante 4,6 dias, no DEM de 80 m; na crista do mesmo sítio (89,438°S 137,283°W) o Sol fica a +4,3° e a Terra nasce em 12,7 dias, como no nosso. O 456, no nosso ponto exato com uma grade de 960 m, perde o Sol em 4 d 16 h. Perto da crista, o declive local decide, e só um DEM fino o vê: é o argumento da nossa escada de resolução.
86. **Validar a energia com pousos que tombaram** (14/11/2026, às 22h). O Shadowline (466, [site](https://shadowline.space/science/landings)) calcula quando os painéis de SLIM, IM-1, IM-2 e Blue Ghost 1 recebiam Sol na posição em que pararam e compara com os eventos relatados pelas equipes, separando os eventos que ajustam a orientação ("fit") dos que ficam guardados para testar ("check"). É um teste contra observação que não depende de fotos, e usa o pouso que conta a nossa história.
87. **Os 130 sítios do Wueller deixaram de ser só nossos** (14/11/2026, às 23h). O Fly Me to the Moon (Los Piratas de Mach, Madri, [site](https://nasaspaceapps.volmer.es/)) carrega os 130 com a fonte e o DOI dos dados, calcula o horizonte do LOLA de 80 m em cada um e se compara ao SunDays27 do artigo nos 130: diferença mediana de 1 dia, média de 4,4, correlação 0,79, 68% de acordo no limite de 10 dias, com a lista sítio a sítio e as diferenças grandes à mostra (NR105: 3 publicados, 16,2 deles). A nossa checagem do mesmo artigo falha (75 de 130 dentro de 1 dia). Os dois números falam do mesmo fato: perto das cristas, o ponto do artigo e o do DEM não coincidem (lição 81). Mostrar também a mediana e a correlação na Prova seria uma segunda leitura, sem mexer na nossa tolerância.
88. **O português virou comum** (14/11/2026, às 23h). Além do 166, agora têm a interface em português o Ridgelight (469, dez línguas), o ViaLunae (194, Fortaleza, PT e EN, com relevo) e o IDK (Dubai, oito línguas). "Em português" sai de vez da lista do que é só nosso; o que segue nosso é o texto feito em português para o professor brasileiro, não a tradução.
89. **Validar a sombra contra fotos do LROC, com o horizonte plano como controle, virou padrão dos fortes** (14/11/2026, às 23h). O Ridgelight (469) compara a sombra do modelo com 37 quadros do LROC WAC em 200 pontos: 94,1% de acordo e kappa 0,707, contra 56,1% com horizonte plano. A Luna Atlas ([site](https://13-54-224-119.sslip.io)) usa 6 quadros de [período anterior] com a regra de aprovação fixada antes de rodar e mostra a que falha (82,7%), e mostra o pôr do Sol do Blue Ghost 1 falhando por 2,4 h, como a nossa Prova. O nosso teste do LROC (duas imagens do IM-2) tem controle negativo; falta o número "sem relevo" na mesma linha.
90. **A faixa do DEM como "a escolha vira ou não vira"** (14/11/2026, às 23h). O SITE REGRET (Bilbao, [site](https://site-regret.vercel.app/)) compara dois pontos do Connecting Ridge a 648 m um do outro com o DEM de 5 m do PGDA 78, viés regional, campo correlacionado e os cinco clones publicados, e diz quando a decisão entre os dois muda: "B ganha com 14 h 40 min de escuro; com outra hipótese de relevo vai a 49 h e A passa à frente". É a forma mais clara que vi da #49: uma frase sobre a decisão, não uma barra de erro.
91. **No Connecting Ridge, três pontos e três horas do nascer da Terra** (14/11/2026, às 23h, pela consulta de referência). O Aphelion (386), no ponto do De Rosa [período anterior] (89,468°S 137,411°W), dá a Terra em 47% e 12 d 16 h sem Terra a partir de 01/12, como nós. O Lightlanders e o Sightline, no ponto do Glaser [período anterior] (89,4505°S 137,16°W), dão o nascer às 01:00 de 13/12; o Horizon Breachers, no ponto do Lunar Surface Data Book (89,4632°S 137,49°W), às 23:55. Nós: 16:05. Confirma a lição 82: a fonte da coordenada pesa mais que o método, e mostrar a fonte ao lado do Site (já temos) é o que permite comparar.

## Lições novas de 15/11/2026

92. **Uma tabela de fontes de erro, com o tamanho e o efeito de cada uma** (15/11/2026, à meia-noite). O Praseodymium Lunar Planner ([site](https://praseodymiumlunarplanner.vercel.app/), evento universal, enviado) tem, na página de precisão, uma tabela "fonte, tamanho, efeito, conserto": resolução do relevo de 312 m a 1,6 km, de 0,4° a 3° no horizonte, deixa o Sol "um pouco otimista ou pessimista"; efeméride truncada, uns 0,1°, minutos nos eventos; passo de 3 h, ±3 h nas bordas; um ano só, até ±10 pontos. E escreve onde o horizonte dele erra: RMS de 2,65° no Mons Mouton Plateau contra 0,43° no Connecting Ridge. A nossa Prova diz o que cada checagem não cobre, mas não junta as fontes de erro numa tabela com o tamanho de cada uma. Para o juiz de Validity, é a leitura mais rápida de "onde este número pode errar".
93. **Na Athena, 290 m mudam a resposta inteira** (15/11/2026, à meia-noite, pela consulta de referência). O Lunar Sightline Planner (toni, Legazpi, [site](https://roaring-salamander-43b1db.netlify.app/)) usa um "IM-2 Athena (approx.)" em 84,800°S 29,200°E, a uns 290 m do ponto final do LROC, com LOLA de 20 m: lá o horizonte no azimute do Sol fica a 5,04° e o Sol some por 35 dias a partir de [data anterior a 14/11/2026]. No ponto do LROC, o RidgeLight da Tech Arena, o Lightlanders, o Aphelion e nós damos o Sol cortado só na primeira meia hora (30% do disco às 00:00) e 47 a 48 h de Sol. É o argumento da Athena em outra escala: o ponto exato, com a fonte, decide. Reforça as lições 82 e 91.
94. **Duas rodadas de modelo, servidas lado a lado** (15/11/2026, à meia-noite). O Moon Plan B ([lunavigator.com](https://lunavigator.com/), Hanói) calcula 2026 a 2030 duas vezes, uma com SPICE e o LOLA do PGDA e outra com o Horizons e o Moon Trek, publica os manifestos com SHA-256 e deixa o visitante trocar de rodada. Também anota em cada sítio que o mesmo ponto do Connecting Ridge dá 76% de Sol a 20 m e 89% a 240 m, e que por isso a comparação pede uns 10 pontos de tolerância. A nossa escada de resolução mostra a mesma coisa na tela; a nota por sítio é uma forma curta de dizer isso no seletor.
95. **O rumo do lander como pergunta** (15/11/2026, à 1h). O LANDERPRINT (494, [site](https://landerprint.vercel.app)) pergunta "para que lado o lander deve ficar virado": com quatro faces de painel fixas, virar o corpo 10° faz a energia de uma semana de outubro de 2027 passar de suficiente a insuficiente (10.628,79 Wh contra 13.360 Wh de carga, declarado pelo time). É a história da Athena contada do lado do painel. A nossa bateria já tem painéis fixos num azimute (`phase4/battery`); falta contá-la assim no pitch (#180).
96. **Uma lista do que ainda não foi conferido, no topo da validação** (15/11/2026, à 1h). O 490 ([site](https://lunar-site-navigator.cutenitki.workers.dev)) abre "How we know it's right" com quatro números (PGDA r = 0,976, sombra permanente IoU 0,81, Chandrayaan-3 e Blue Ghost 1 a menos de 4 h do pôr previsto, Horizons a 3e-5°) e fecha com "What we haven't checked yet": o horizonte contra o QuickMap ou o Moon Trek e as alturas contra outra ferramenta. A nossa Prova diz o que cada checagem não cobre, uma por uma; uma lista curta da página inteira seria a forma rápida para o juiz. Junta bem com a tabela de fontes de erro (lição 92).
97. **O `gh search code` acha o que o `gh search repos` perde** (15/11/2026, à 1h). A busca por código com o nome do desafio trouxe 37 repositórios que nenhuma rodada tinha achado, vários com site no ar desde 13 ou 14/11 (Malapert, 490, LunaWindow 488, o time de Recife, SEAL). O `gh search repos` só olha nome e descrição; quem põe o nome do desafio só no README não aparece. Entra na rotina a partir desta rodada.
98. **Uma ferramenta independente bate conosco ao minuto no Connecting Ridge** (15/11/2026, às 2h, pela consulta de referência). O Zoriana (526, [site](https://zoriana.fly.dev/)), com o Horizons de hora em hora, o LOLA de 40 m e interpolação de 5 min, dá no nosso ponto exato o nascer da Terra às 16:05 de 13/12, o mesmo minuto do nosso, e o pôr às 11:35 de 27/12 (nós: 11:29). À 1h o time de Recife (491) tinha dado 15:47. Duas ferramentas de outros times, com outro código, chegando ao mesmo nascer não são uma referência independente no sentido da Prova, mas são o melhor argumento de pitch que a consulta de referência já deu: "dois outros times, com outro código, acham a mesma hora".
99. **A incerteza do relevo dita como horas de Sol, de P10 a P90** (15/11/2026, às 2h). O LunarSync ([site](https://nasa-space-apps-challenge-liard.vercel.app/app/accuracy), Ahmedabad) propaga o erro vertical do LOLA (σz de 0,37 m) até a potência e mostra uma faixa: "P10 mean 0.0%, P50 58.3%, P90 93.3%", mais um Monte Carlo de 500 pousos num círculo de 100 m e as sombras de uma foto do LROC comparadas por área (IoU 0,807). O moonle (373) faz o mesmo com a nota de cada região, "± terrain res.", trocando 240 m por 960 m, e o CeyNova escreve o Earthset como "13 d 23 h to 14 d 15 h". Três formas de dizer a #49 numa linha que o juiz lê.
100. **Doze dos 29 links novos desta hora não abrem para quem visita** (15/11/2026, às 2h). Google Sites que pedem login, apps do FlutterFlow fora do ar, senha, Codespaces e ngrok em 404, `localhost` e GitHub Pages em 404, entre eles o Skimline, que parece forte pelo README e foi enviado com o site em 404. O juiz vê o mesmo que nós. O nosso site também não abre para quem está fora (403 na Cloudflare, de propósito): no envio, o link precisa abrir de qualquer lugar.
101. **O Earthrise deixa o juiz refazer a validação no próprio navegador** (15/11/2026, às 3h; repositório 542). Três das checagens da página "How we know it is right" têm um botão que baixa o relevo, refaz a conta na placa de vídeo do visitante e põe o número dele ao lado do número do time. Também usa a Tabela 2 do Barker [período anterior] (sete regiões do Connecting Ridge, a 1 m e a 5 m) do jeito certo: como o artigo dá percentis sobre 100 cópias do relevo, o time só confere que cai do lado certo de cada limite (42 de 42), em vez de pedir igualdade. Para a nossa Prova: uma checagem que roda na frente do juiz convence mais que uma tabela, e o Barker [período anterior] é uma referência independente para o nosso ponto B, que hoje não tem nenhuma.
102. **Três ferramentas novas dão a Terra escondida às 00:00 de 01/12 no nosso ponto B, com o horizonte entre −0,84° e −1,2° no azimute 143,6°** (15/11/2026, às 3h). O Horizon Line (LOLA de 240 m, a Terra a −2,0°), o TIM Academy (LOLA de 80 m, −2,04° contra −0,9°) e o Earthrise (LOLA ajustado, "1.2° below the terrain") concordam conosco, contra o Apollo Harness e o Selene Horizon, que viam a Terra nessa hora. O Horizon Line ainda dá 331 h de Terra no mês, as nossas 331 h, e o nascer em 12 d 17 h. O nascer varia de 13/12 00h (TIM Academy) a 13/12 17h entre eles: a hora do nascer depende do relevo a dezenas de quilômetros, e o número de horas é mais estável que a hora do evento.
103. **O atraso explicado hora a hora, com a causa de cada hora perdida** (15/11/2026, às 4h; repositório 555). O Slip Impact Brief ([site](https://aryasira.github.io/nasa/), time Space City Ad Lunam, Houston) pega um atraso de pouso e escreve linhas como "Sun lost 69 h, the lunar day/night cycle (not terrain)", "Earth lost 117 h, the Moon's libration (not terrain)", "Earth gained 39 h, the site stands above the terrain toward az 131°" e "Sun lost 27 h, blocked by Mons Mouton at az 101° (E), 14 km". As linhas somam exatamente a mudança de horas, e o que é menor que meia hora fica de fora. É o mesmo Occluder com nome que nós temos, só que aplicado à diferença entre duas datas. O nosso painel de atraso (`phase4/slip`) diz quanto a Janela perde em cada dia de início e mostra o plano B, mas não diz por quê. Também deixa claro que nem toda perda é do relevo: num atraso de 10 dias no IM-1, 69 das 73 horas perdidas são do ciclo do dia.
104. **Quem vê a Terra às 00:00 de 01/12 no Connecting Ridge corta o relevo perto** (15/11/2026, às 4h, pela consulta de referência). O LunarX (303, time VoidX, [site](https://eres0045.github.io/lunar-landing-navigator/)) dá a Terra "VISIBLE" a −1,80° no CR1 às 00:00 de 01/12, com o horizonte a −2,51° no azimute 144°, e escreve na página Evidence que o horizonte só usa o relevo a até uns 10 km ("more distant massifs are not in the horizon"). Para nós, quem esconde a Terra nesse azimute é o Mons Malapert, a 134 e 140 km. É a primeira causa declarada para a divergência da lição 102: as ferramentas que veem a Terra nessa hora provavelmente cortam o horizonte antes do Malapert. Na mesma hora, o MoonSight (Tashkent), com o observador a 0 m e o relevo lido só no azimute do centro do disco, dá 57% de Sol no Connecting Ridge em janeiro de 2027, contra os nossos 96%: como o LUNA-RESOLVE às 3h, a altura do observador muda o Sol inteiro nessa crista. Para o pitch: "o morro que esconde a Terra está a 140 km" é um número que separa quem corta o horizonte cedo de quem não corta.
105. **Quatro ferramentas de fora dão o nascer da Terra no nosso ponto B a menos de 5 minutos do nosso** (15/11/2026, às 5h, pela consulta de referência). No ponto exato (89,4661°S 136,949°W, 2 m), o Earthset ([site](https://earthset.spaceapps-earthset.workers.dev/point), Faisalabad) dá 16:05 de 13/12, com o LOLA de 20, 80 e 240 m até 300 km e o SPICE no navegador; o Noctis Horizon (592, Pavlodar) dá 16:03 e 47% de Terra; o Lunar Window (364), agora com relevo de verdade em todo ponto, dá 16:00 e o pôr às 11:32 de 27/12 (nós: 11:29). Com o Zoriana (16:05, lição 98), são quatro cálculos independentes a até 5 min do nosso 16:05:27, e o time de Recife a 18 min. O Earthset ainda escreve a hora do pôr do Sol com uma faixa ("2027-03-18 03:19 UTC ± 1.4 h") e confere a altura do chão contra um pouso real ("IM-1 Odysseus: 2,579 m", 13 m de diferença). Para o pitch, o nascer da Terra no Connecting Ridge deixou de ser um número só nosso: é um número que quatro times chegam sozinhos. Na Prova, continuam fora como referência independente (não são publicados).
106. **A capa promete o relevo do LOLA, o arquivo servido diz "mock"** (15/11/2026, às 5h). O Odysseia (574) escreve "LOLA LDEM 20M/PX" e "0.0018° Sun elevation RMSE vs NASA JPL Horizons" na capa, mas o horizonte que o site baixa (`data/horizon/connecting-ridge.json`) traz `"demSource": "LOLA_POLAR_MOCK_80KM"` e `"source": "mock"`, e dá 46% de Sol no Connecting Ridge em dezembro, contra 100% em todas as ferramentas com relevo de verdade. O LUNA-LINK (588) promete "LOLA DEM (1024 PPD)" e calcula com fórmula analítica e um ângulo fixo; o SoloHorizon (580) promete o relevo com faixa de incerteza no README e escreve "Flat horizon assumed" no rodapé. Qualquer juiz que abra as requisições de rede vê isso em um minuto. Vale para nós também: cada frase da capa, do pitch e do vídeo precisa apontar para algo que a Prova ou as "Estatísticas para nerds" mostram.
107. **Um critério de aceite escrito antes da comparação, e a falha explicada pelo relevo** (15/11/2026, às 5h). O HORIZON do time VOID-X ([site](https://web-app-sand-kappa.vercel.app/), Trivandrum, enviado com vídeo) compara quatro sítios com o AVGVISIB do PGDA e escreve o critério ("|delta| ≤ 5 pp" ou o valor da NASA dentro da faixa 5 × 5 do próprio mapa); o Shackleton rim falha (15,23% contra 35,46%) e a tela explica: o mapa da NASA é uma aresta de faca ali, o DEM de 80 m alisa o entalhe, e acertar exigiria +1,1° de horizonte, "not a tunable parameter". No painel do dia, o mesmo sítio leva o aviso "Knife-edge site: the result is sensitive to position". É o que a nossa Prova já faz com o Wueller e o Blue Ghost 1, mais um aviso por sítio quando o resultado depende de poucos metros, que é a pergunta da #49.
108. **Duzentos metros na mesma crista tiram o Sol do pouso** (15/11/2026, às 6h; time Sharpai, Vilnius, [site](https://singular-croquembouche-443b7a.netlify.app/)). O Sharp Navigation tem dois pontos do mesmo mapa do PGDA (Site01) no Connecting Ridge: o do alto (89,439°S 137,144°W) e o "lower slope" (89,463°S 137,490°W), a uns 0,2 km do nosso ponto B. Em 01/12/2026 00:00, no de baixo, o Sol fica 0,3° abaixo do relevo e só nasce 1 d 5 h depois, a Terra fica 2,7° abaixo (contra 1,2° nas outras ferramentas) e só nasce em 14 d 21 h, e o mês tem 74% de Sol e 36% de Terra, contra os nossos 100% e 46,8% no alto. Não há referência para dizer quem acerta o ponto de baixo, mas o efeito é o da nossa história: a Athena tombou a poucas centenas de metros do alvo. É o argumento da nossa dispersão de 19 pontos, mostrado por outro time com outro DEM (5 m perto).
109. **O Gläser [período anterior] no Connecting Ridge, numa linha, e a média de Sol da Athena ao décimo** (15/11/2026, às 6h). O 171 (daniel27-space, time Galaxy1, Singapura) escreve "On the Shackleton connecting ridge we get 92.29% sunlight at 2 m; Gläser et al. ([período anterior]) published 92.27%", e o 2 (BroBYW) confere o Gläser [período anterior] e [período anterior] a menos de 1,5 ponto. É uma referência publicada para o nosso ponto B, que a Prova ainda não tem, e mais simples de pôr do que a Tabela 2 do Barker [período anterior] (lição 101). Na mesma hora, o 2 dá no IM-2 de 06 a [data anterior a 14/11/2026] o Sol em 97,6% em média, com 31% do disco às 00:00; a nossa fração média é 0,975. E no ponto B, o SiteLine (593) dá o pôr da Terra às 11:29 de 27/12 (nós: 11:28:58), o Darksight (187) 46,0% de Terra em 30 dias e o 2 46,1% (nós: 46,8%).
110. **O horizonte cortado em 60 km volta a mostrar a Terra no Connecting Ridge** (15/11/2026, às 7h, pela consulta de referência). O AstroNova ([site](https://shahdalshmaryaaa99-lang.github.io/astronova/), time Astronova_ar, Jidá) usa o LOLA LDEM_80S_80MPP_ADJ "±60 km @ 200 m", escrito no `status.json` que o site baixa. No ponto LOLA-01 (89,4735°S 137,437°W, a uns 0,2 km do nosso ponto B), às 00:00 de 01/12/2026, ele dá a Terra a −2,04° e o relevo naquela direção a −4,12°, "Earth is visible". Para nós, a Terra está atrás do Mons Malapert, a 140 km. É a mesma causa da lição 104 (o LunarX, com o relevo até 10 km), agora com 60 km. Para nós: o Occluder com nome e distância é a prova do que eles perdem; vale dizer no pitch que o morro que esconde a Terra está a 140 km.
111. **O mesmo nome em lugares diferentes** (15/11/2026, às 7h). Três sites desta hora chamam de Connecting Ridge um ponto que não é a crista: o LUNAR ([lunar.select](https://www.lunar.select/)) tem um "Connecting Ridge" em 89,35°S 65,2°W, a 600 m abaixo do nível de referência, que dá 0 h de Sol em dezembro, ao lado do "Site 01 · Connecting ridge" do PGDA, que dá 88%; o Lunar Atlas põe o "Shackleton Rim (Connecting Ridge)" em 89,9°S 0°; o LUNAR-X, em 89,70°S 120°E. Quem compara números entre ferramentas pelo nome compara lugares diferentes. Para nós: a fonte da coordenada ao lado do Site (já temos) é o que evita isso; nas comparações deste arquivo, sempre a coordenada, nunca só o nome.
112. **A regra do disco explica 3,8 pontos de Terra no ponto B** (15/11/2026, às 7h, pela consulta de referência). O LunarSims (time MODI, Stalowa Wola, [site](https://lunarsims.reachit.space/)) escreve no gráfico qual borda conta: o Sol pela borda de cima ("Disc visible 100.0% of time") e a Terra pelo disco inteiro acima dos morros ("Full disc above mountains 43.0% of time"). No nosso ponto exato, de 01 a 30/12/2026, isso dá 100% e 43,0%, contra os nossos 100% e 46,8% pela regra do centro. Os dois batem quando se diz a regra. Para nós: é o argumento da #245 com um número; vale dizer na tela que a Terra conta pelo centro.
113. **O centro da região do Connecting Ridge, a 0,1 km do nosso ponto, perde o Sol** (15/11/2026, às 7h, pela consulta de referência). O 608 (Neeka1214, Taipé, [site](https://neeka1214.github.io/lunar-navigator/)) usa o centro da região do Artemis III (89,463°S 137,490°W, 1.943 m) com o LOLA de 80 m: em 01/12/2026 00:00 o Sol a 1,76° fica "blocked", e o próximo dia lunar tem 71% de Sol e 35% de Terra, quase os 74% e 36% do Sharp Navigation no mesmo ponto (lição 108). O Moonset, no nosso ponto exato, dá a Terra nascendo 46 h depois do nosso nascer; o LULER, no mesmo centro de região, dá metade de janeiro de 2027 no escuro. Divergem, sem referência independente para decidir. Para nós: o ponto do Wueller e o centro da região do Artemis III não são o mesmo lugar, e a diferença decide o Sol; a nossa dispersão de 19 pontos mostra isso no app.

114. **Um satélite de retransmissão encurta o apagão da Terra de dias para horas** (15/11/2026, às 8h; repositório 623). O Earthrise Atlas ([site](https://earthrise-atlas.vercel.app/lab), time Sunvi) usa a órbita prevista do LRO, tirada do Horizons, e mostra no nosso ponto B, de 01/12/2026 a um dia lunar, "Earth or relay 51,0%" e o maior apagão caindo de 12,7 dias (só a Terra direta) para 1 h 49; o Gateway e o Queqiao-2 entram marcados como "MODEL". Também põe o selo "Fragile result" quando o Sol ou a Terra passam a menos de meio grau do relevo. Nós falamos só do link direto e da DSN. Para o Relevance, a retransmissão é a resposta natural ao "a Terra some por 12 dias" que a nossa contagem já mostra; o selo de resultado frágil conversa com a #49 e a #245.
115. **Mais duas ferramentas batem conosco no ponto B** (15/11/2026, às 8h, pela consulta de referência). O Earthrise Atlas dá no Connecting Ridge dele, de 01/12/2026 a 29,5 dias, 100,0% de Sol e **46,8% de Terra**, o nosso número. O LUNEX (619, [site](https://projeto analisado.vercel.app/workspace)), a 0,8 km do nosso ponto, dá Sol 100%, Terra 46% (13 d 20 h, nós 13 d 19 h) e o nascer da Terra às 15:48 de 13/12 "± 10 min", 17 min antes do nosso; no IM-2 bate conosco nas 48 h. Os dois usam o LOLA de 20 m perto do ponto e validam contra o PGDA (o LUNEX em 2.000 células do AVGVISIB, mediana 0,2 ponto). Somam-se ao Zoriana, ao Earthset, ao Noctis Horizon, ao Lunar Window e ao SiteLine, que já davam o nascer da Terra no ponto B a minutos do nosso (lições 98, 102 e 105).
116. **A incerteza do relevo como faixa ao lado do número** (15/11/2026, às 8h). O Ridgeline (213, [site](https://lunar-site-planner.vercel.app/), NTU Larpers, Singapura) escreve "Both hours 312 h (190–321)" com "Range across horizon and site shifts, 7 points"; o LUNARIS (618, [site](https://aryaergin.github.io/lunaris-spaceapps-2026/)) calcula o horizonte com limite de baixo e de cima e dá "Sun: at least 501 h 19 min", separando o tempo "unresolved"; o LUNEX dá a hora do nascer da Terra com "± 10 min". É a #49 (faixa de incerteza do DEM nos números) feita de três jeitos diferentes, e em nenhum dos três é difícil de ler. Ainda não achei isso no nosso código.
117. **O critério muda o nascer da Terra em mais de um dia** (15/11/2026, às 8h, pela consulta de referência). No nosso ponto exato, o site do time N0TH1NGC (624, Almaty) usa por padrão o Sol com metade do disco e uma máscara de 2° acima do relevo para a Terra, escritos nas opções: dá o nascer da Terra às 23:55 de 14/12 (31 h depois do nosso) e 38% de Terra, contra os nossos 46,8% pelo centro. O SIRIUS-X, a 0,5 km, dá 303 h e o nascer às 15:57 de 14/12; o LunarDestination, a 0,9 km e de hora em hora, 44% e 07:00 de 14/12. Quem deixa o critério à vista, e de preferência à escolha do usuário, deixa o juiz entender por que os números diferem. É a #245 (dizer que a Terra conta pelo centro).
118. **A hora de cada evento com a margem a 95%, tirada de 32 versões do chão** (15/11/2026, às 9h; repositório 642). O Earthrise do time Astroy/Ed ([site](https://earthrise-moon.vercel.app/validate), 912 commits) parte da diferença de 1,4 m entre duas gerações de mapas do LOLA do polo, faz 32 versões do chão por sítio e escreve a margem que cobre 95% dos eventos: no Connecting Ridge deles, pôr do Sol ±4,5 h, nascer ±2,5 h, pôr da Terra ±2 h, nascer da Terra ±3 h. A mesma página mostra que 3 de 20 imagens do LRO não batem com as sombras. É a #49 (faixa de incerteza do DEM) feita de um jeito que cabe numa linha ao lado da contagem; a nossa escada de 240, 80 e 20 m daria o mesmo tipo de faixa sem cálculo novo.
119. **Três referências publicadas do ponto B entram em sites novos, com a falha escrita** (15/11/2026, às 9h). O Penumbra (643, [site](https://penumbra-lunar.pages.dev/), Fractured Toes, Kuala Lumpur) confere a Tabela 2 do Barker [período anterior] (7 de 7 regiões passam) e o SP-01 do Mazarico [período anterior], onde falha ("our shortest night is 2.96 d vs his 2.75 d"), e marca o que não rodou ("not run"). O Lunar Navigator do SteppeX ([site](https://steppex.vercel.app/), Ulaanbaatar) põe o Gläser [período anterior] no Connecting Ridge C1: 76,8% contra 76%, e o C2 com 9 pontos de diferença, escrito. Com o 171, o 2 e o Earthrise (542), já são cinco times com uma referência publicada para o ponto que abre o nosso app; a nossa Prova ainda não tem (sugestão 4).
120. **A grade sítio × dia de pouso responde o atraso de uma vez** (15/11/2026, às 9h). O Four Lights ([site](https://fourlights.gcsa.space/), Make it So, Gold Coast, enviado) abre numa tabela em que cada célula é "dias úteis" para um pouso naquele dia, de −2 d a +11 d, com ● works, ▲ marginal e ✕ no power, e a frase "6 of 12 sites work". O assistente dele só traduz a pergunta em controles ("the answer is computed by the planner"). O nosso `phase4/site-windows` e o plano B dizem a mesma coisa em duas telas; a grade é uma forma de juntar as duas na comparação da fase 2 (#46).
121. **A regra do disco e a folga da Terra como escolha do usuário** (15/11/2026, às 9h, pela consulta de referência). O Gnomon ([site](https://gnomon.infolutio.com/dashboard), Lagrange Point, Iligan City) deixa escolher se o Sol conta pelo centro ou pela borda de cima e quanto a Terra precisa passar o relevo; o 129 (Moussa-dme) oferece qualquer parte, metade ou o disco inteiro e uma folga de 0,5° para a Terra, e com qualquer parte bate conosco no ponto B (Sol 100%, Terra 48% contra 46,8%, nascer da Terra 43 min depois). O Penumbra usa 2° de folga e põe o nascer da Terra 1 d 8 h depois do nosso. Reforça a #245: o juiz que comparar ferramentas vai ver diferenças de um dia que só vêm da regra.

122. **O começo da Janela A depende de centésimos de grau, e as ferramentas se dividem pela regra do disco** (15/11/2026, às 10h, pela consulta de referência). Às 00:00 de [data anterior a 14/11/2026], no ponto final do IM-2, o Sol está a 1,73° e o relevo a leste, conforme o mapa de cada time, fica entre uns 1,72° e 1,82°. O Long Shadows ([site](https://hvozdzvera.github.io/long-shadows/), Sol pela metade do disco, LOLA de 240 m) diz que o Sol volta em 1 h 20 min; a Janela Polar (673, 0 m de altura) diz 1 h; o Lunar Horizon do K2 ([site](https://k2-lunar-horizon.vercel.app)) dá 37 min de escuro. O LunaWindow (676, qualquer pedaço do disco, LOLA de 5 m) diz "25% of disc visible", o LUNA de Sydney "Sun 30 % in view" e o 677 mostra o Sol "Sunlit" com folga de 0,01°. Nós contamos qualquer pedaço do disco e damos as 48 h com fração média de 0,975. Para nós: a primeira hora da consulta A é um caso de fronteira e serve de exemplo na tela de "por que a regra importa"; não é erro de ninguém.
123. **No mapa de 5 m, um ponto publicado pode cair num buraco** (15/11/2026, às 10h). O Lunar South Pole Mission Planner do Major Tom to Brown Control ([site](https://lunar-mission-planner-alpha.vercel.app/?layer=planner)) usa o LOLA de 5 m perto dos sítios e mostra que o ponto publicado do Site 004 tem 0% de Sol e uma crista a 54 m, 10,5 m mais alta, tem 100% em 01/12/2026. No Connecting Ridge deles (89,450°S 137,310°W) o Sol cai para 82% e a Terra para 35% em 30 dias, contra os nossos 100% e 46,8% sobre o LOLA de 20 m. O time explica pelos artigos: os pontos 001 e 004 vêm do Bussey [período anterior] e do Mazarico [período anterior] sobre um mapa de 240 m, e "a 240 m pixel holds over 2,000 of our 5 m cells". Para nós: é o mesmo argumento da cratera de 20 m da Athena, agora num sítio do Artemis, e é um limite da nossa escada de resolução (para em 20 m) que vale escrever na Prova.
124. **A incerteza do relevo pelo erro de cada pixel, não só pela resolução** (15/11/2026, às 10h). O Lunaris do time aris ([site](https://lunaris-demo.vercel.app)) mostra "With terrain height error": sobe e desce o chão pelo erro publicado de cada pixel da NASA e refaz Sol e Terra; o LineOfSight ([site](https://bergaltay.github.io/LineOfSight/)) põe o 1σ do mapa ao lado da inclinação ("2.2° ±2.1°", "97% com +1σ"). É o caminho da #49 (antes no `PENDENCIAS.md` do app) com dois exemplos prontos, além da margem a 95% do Earthrise (lição 118).
125. **Plano A contra plano B, com o melhor de cada linha marcado** (15/11/2026, às 10h). O LineOfSight compara dois planos (sítio e data cada um) nos 30 dias depois do pouso, marca com ★ o melhor de cada linha, conta como iguais diferenças menores que 0,5 ponto, 0,5 h ou 0,05°, e resume numa frase ("Plan B's longest radio gap is 7.7 d shorter, but plan A's longest darkness is 6.7 d shorter"). O Lunar Horizon do K2 faz o mesmo em "Head to head". Para nós: é a forma mais curta da comparação lado a lado que ainda não temos.
126. **Um time brasileiro em português e mais um enviado** (15/11/2026, às 10h). A Janela Polar (673, The Myths, Nova Iguaçu) está no ar em português, com DSN e elevação mínima, contagens, melhor data, cenários guiados e um par de contraste a 3 km; no site estático a efeméride é analítica. O LunarSight do Nota Maxima (São Paulo) foi enviado às 13:20 UTC. O português deixa de ser diferencial entre os brasileiros (o ViaLunae, de Fortaleza, já tinha).

127. **Um horizonte cortado em 100 km perde o morro que esconde a Terra no ponto B** (15/11/2026, às 10h, pela consulta de referência). O Cosall ([site](https://cosall.onrender.com)) usa o LOLA de 80 m "out to 100 km" e, no nosso ponto exato às 00:00 de 01/12/2026, diz "Earth up (−2.0°) — direct-to-Earth link possible". No nosso cálculo a Terra só nasce às 16:05 de 13/12, atrás do Mons Malapert, a 134–140 km. O Tanaw (previsão com Horizons e LOLA de 5 m) e outros cinco times dão o nascer em 13/12, como nós. Para nós: o alcance do horizonte é uma premissa que muda a resposta no ponto que abre o app, e vale dizer na tela até onde o nosso vai.

128. **A faixa do relevo pelos 100 clones do PGDA, ao lado do número da capa** (15/11/2026, às 14h). O Peak of Eternal Light (518, Kyiv; [site](https://peak-of-eternal-light.pages.dev)) roda cada resultado nas 100 versões do relevo de 5 m que a NASA publica para oito sítios e mostra, logo abaixo dos quatro números grandes, "TERRAIN ±": Sol 85–89%, noite 4,3 a 10,2 d no Connecting Ridge em 2027. Na consulta A ele bate conosco no décimo de grau (Sol a 1,73° com 31% do disco às 00:00, Terra a 10,84°). Para nós: é a forma mais curta da issue #30 (faixa no Sunset e no Earthset), que tem o PR #48 aberto; a noite que varia em dias é o argumento para a bateria.
129. **Dizer o que cada checagem prova e o que ela não prova, e testar a convergência do horizonte** (15/11/2026, às 14h). O Outliers (705; [site](https://lunar-landing-site-nav-outliers.pages.dev)) escreve "SHOWS / DOES NOT SHOW" embaixo de cada checagem e roda o horizonte de novo com metade do passo em azimute e metade em distância (maior mudança 0,0064°, alvo 0,01°), mostrando o perfil antigo que falhou com 0,0104°. A comparação com o mapa da NASA fica com as diferenças (+18,8 pontos no Site 01) e "Still under investigation". Para nós: a nossa Prova já diz o que cada checagem não cobre; o teste de convergência é uma checagem que não temos e que responde "o passo de amostragem muda a resposta?".
130. **O tipo de missão como primeira escolha, que transforma os números em metas** (15/11/2026, às 14h). O site do time LunarExplorers (717, Oslo; [site](https://birgit-ct.github.io/lunar-landing-site-navigator/)) pede antes de tudo rover solar, lander científico ou posto de comunicação, cada um com metas (Sol ≥ 50%, Terra ≥ 50%, escuro ≤ 72 h), e pinta o calendário com quantas metas cada dia cumpre. No nosso ponto B, em 28 dias, dá Terra 49%, como nós (49,3%). Para nós: uma forma de ligar o número de aula e a bateria a um "sim ou não" sem dar nota única.
131. **O nome do sítio não garante o ponto** (15/11/2026, às 14h). O AetherRidge (400) chama de "Shackleton Crater Rim (Connecting Ridge)" um ponto em 89,686°S 197,37°E, a uns 7 km do Connecting Ridge do Wueller (89,4661°S 136,949°W); o Peak of Eternal Light usa 89,439°S 222,90°E (a ~0,8 km) e dá o nascer da Terra 15 h antes do nosso. E o time zenon (716) chama o produto de "Sunchaser", o mesmo nome do 125. Para nós: na consulta de referência, comparar só quando a coordenada bate; no pitch, citar time e endereço, não só o nome do produto.

## Repositório por repositório

### 1. MdAhbab/PolarWindow

- **Arquitetura em camadas (ADR-1):** a máscara é pré-calculada por sítio, e as linhas do tempo são calculadas na hora com passo de 900 s e guardadas em cache. Uma tabela anual pré-calculada foi abandonada porque calcular na hora custa 12,5 ms.
- **Resolução justificada pela física:** perto do polo o Sol anda 0,51° de azimute por hora. Uma faixa de 0,25° equivale a 29 min de movimento do Sol, a mesma ordem do erro que o DEM já impõe. Passo de 900 s é meia faixa, então nenhuma passagem escapa. Depois, bissecção até ~1 s.
- **Validação contra o que voou:** compara com o arquivo SPICE do CLPS no NAIF (instante do pouso com 1 s de diferença, posição a menos de 100 m) e diz onde a validação não serve. Nenhum dos três pousos foi um pôr do Sol causado pelo relevo.
- **Quatro números sempre juntos e nenhuma nota única.** A comparação ordena por um número de cada vez e mostra empates como empates.
- **IA que não pode inventar número:** o assistente só responde com resultados das ferramentas, e uma trava recusa números que não vieram delas.
- **O que evitar:** o escopo é enorme (trajetória, radiação, clima no lançamento). Em 36 h, isso é impossível e dilui a mensagem.
- **[data anterior a 14/11/2026]:** continua crescendo (lição 35). A elipse de pouso com inclinação e iluminação em cada amostra (ADR-22) é uma boa referência para o nosso "dentro de 100 m".
- **[data anterior a 14/11/2026]:** 409 commits. É do time Sagittarius A\* (Dhaka, 6 membros). A pasta de submissão com roteiros por falante é a referência da lição 38.

### 2. BroBYW/CLPS-Lunar-Mission-Website

- **O PROMPT.md e o PLAN.md** (lição 2) e o **AI_USAGE.md**, um registro datado do que a IA fez e do que o time decidiu. É o formato que vamos precisar para declarar o uso de IA.
- **As propostas técnicas do PLAN.md:** geometria esférica exata em vez de d²/2R (a aproximação erra 0,012° a 300 km), raios a cada 0,1°, horizonte até 300 km, métricas num grid interpolado de 10 min, eclipses lunares tirando o Sol e balanço de energia da bateria além de "carga × maior noite".
- **Validação variada:** Horizons, terreno sintético (esfera e platô com resposta exata), "subir o observador nunca levanta o horizonte" em 50.400 valores, Gläser na mesma altura, mapas do PGDA, eclipses contra o catálogo da NASA, WCAG e 1.022 fotos do LRO.
- **Pino livre com aviso:** fora dos sítios, usa uma grade de 480 m e chama o resultado de "primeira olhada". O pior caso é Malapert, com 15 pontos a mais porque a grade arredonda o pico.
- **Roteiro de demo pronto:** vídeo de 30 s plano a plano com legenda, links que reproduzem cada tomada exatamente e 7 slides de reserva.
- **Uma frase de comparação que fica:** "o cume mais ensolarado perde a Terra, e Haworth equilibra os dois".
- **Ideias de produto:** o "cartão-postal da Terra" (o momento mais bonito da Terra acima da crista), jogos e "olhar em volta" com a bússola do celular.
- **O que evitar:** depois que o núcleo ficou pronto, a IA "sugeriu nove funcionalidades e construiu sem aprovação passo a passo", e o produto inchou.

### 3. WarRinOP/sightline

- **Mastro exato:** para cada azimute, o arquivo guarda as retas `A − h·B`, e a máscara para qualquer altura h é o envelope superior delas. A primeira versão interpolava 13 alturas e errava de 0,1° a 0,7°.
- **Fórmula estável:** a elevação do relevo foi escrita para não subtrair dois números perto de 1,7 milhão de metros, o que perdia dígitos.
- **Armadilha numérica:** `acos(u·v)` não resolve ângulos abaixo de 8,5e-7°. O certo é `atan2(|u×v|, u·v)`.
- **Detalhes do Horizons:** no máximo 25 instantes por requisição (com 50 a URL fica longa e dá erro 502), 1 s entre pedidos e conferir o "eco" de como o Horizons leu o sítio.
- **Contratos de dados com zod e um motor falso** marcado como SIMULATED, para a interface andar antes do motor real.
- **Registro de decisões (D-001 a D-034),** com contexto, decisão e consequência. Útil para o nosso ai-memory.
- **AI_DISCLOSURE.md:** separa a IA usada para construir da IA dentro do produto. Princípio: a IA nunca calcula resultado científico.
- **Números que dá para conferir:** no Shackleton Rim (crista), 85,8% de disco médio visível em 2026 a 2 m. A estação pesa: o Sol fica metade do ano acima do horizonte e metade abaixo, e a maior noite chega a 185,8 dias.
- **O que evitar:** monorepo grande com seis semanas de cronograma e três devs. Não serve para 36 h.

### 4. EmanuelAbasto/CLPS-Lunar-Mission-Browser

- **Botão "horizonte plano × relevo real",** que "muitas vezes inverte o ranking". É a melhor forma de mostrar por que o relevo importa.
- **Validação barata e boa:** 50 pixels do mapa de sombra permanente (PSR) do LOLA. Os 25 de sombra nunca foram iluminados e os 25 iluminados foram, todos.
- **Regra de "Sol nasceu" pela borda superior do disco,** conferida com a marcação de dia do próprio Horizons.
- **Modo simples, com frases como "cerca de 9 dias de Sol por mês", e modo especialista,** além de um link que guarda o cenário inteiro.
- **O que evitar:** sítios de exemplo no lugar dos reais. Fizeram a engenharia antes dos dados.

### 5. Hamzaslam1996/lunarwindow

- **Detalhe que pega muita gente:** no mapa polar estereográfico, o "para cima" não é o norte. O azimute verdadeiro é o da grade menos a longitude.
- **Reproduziu um número publicado:** o pior dia lunar na borda de Shackleton do Fincannon [período anterior] (0,71). Ficou a 0,015 com o observador a 10 m e a 0,48 nas coordenadas impressas no artigo. De novo, a coordenada manda.
- **"Relatório de garantia"** exportável, com os kernels, o DEM, a versão do método e o commit usados. Isso é reprodutibilidade.
- **Lista honesta do que não modela:** escurecimento do limbo, curvatura do horizonte dentro do disco do Sol e modelo térmico.

### 6. Klauscreates/lunar-south-pole-explorer

- **Avisos de escopo em linguagem clara:** "visibilidade geométrica não é qualidade de enlace" e "geração modelada não é carga garantida".
- **Um "Test Site A" neutro para validação,** separado dos sítios reais.
- **O que evitar:** período fixo (out a dez/2026) e 5 pontos. O usuário bate no limite logo.

### 7. kaizarmerchantt-git/clps-lunar-mission-browser

- **A ideia de usar as 13 regiões do Artemis III** é boa e ainda livre de execução séria.
- **O que evitar (o mais didático da lista):**
  - coordenadas arredondadas (89,90°S 0,00°E; 88,00°S 30,00°E);
  - duas linhas com os mesmos números ("Connecting Ridge" e "Connecting Ridge Extension");
  - notas de janela todas 100/100, que não separam nada;
  - nota final que vai de 92 para 18 entre sítios quase iguais.
  
  Um juiz técnico desconfia na hora.

### 8 e 9. rafaa-sf/L-SEA e lunar-horizon-clps-browser

- **Demo em Streamlit:** é o caminho mais rápido para ter algo no ar em Python.
- **README em dois idiomas.** No nosso caso o enunciado pede inglês, mas a apresentação local pode ser em português.
- **O que evitar:** promessa de "motor autônomo de decisão" e "cockpit tático". Prometer decisão autônoma num problema em que a NASA quer ver a evidência soa mal. E dois repositórios iguais confundem.

### 10. partofcosmos-site/lunarsite-compass

- **Achado útil:** o mesmo ponto pode ter Sol e Terra por muitos dias seguidos em Mons Mouton, porque a altitude levanta a Terra no céu. Vale conferir com o Wueller 2026.
- **O que evitar:**
  - efemérides do Meeus em fórmula fechada em vez de SPICE;
  - pesos arbitrários (35/25/25/10/5) sem justificativa;
  - jargão teatral ("Flight Decision Seal", "GO FOR TOUCHDOWN" com hash SHA-256).
  
  Se usarmos TOPSIS, os pesos têm que vir de um requisito (Artemis III) ou ficar na mão do usuário.

### 11. dundaryusuf566-maker/clps-lunar-browser

- **Previsão registrada antes do evento:** publicaram com data marcada uma previsão de quando e onde o Griffin-1 pode pousar, antes do lançamento. Uma ideia equivalente para nós: "a próxima noite em Mons Mouton começa em tal data".
- **"Uma checagem que falhou continua falhando":** o critério fica escrito no código antes de ver os dados, e as falhas aparecem no placar (12/13, 5/6, temperatura no polo reprovada). Mostrar uma falha aumenta a confiança.
- **Pergunta invertida:** "quero pousar aqui entre estas datas, com pelo menos N dias de Sol". Encaixa no nome "Navigator".
- **Temperatura do solo** conferida contra o Diviner. Fica de fora do nosso núcleo.

### 12. Nxmmy-Na/CLPS-Lunar-Mission-Browser

- **API simples e documentada** (`/api/sites`, `/api/site-analysis`), com parâmetros de painel e bateria.
- **Interface bilíngue** com troca na tela.
- **O que evitar:** "fator de sombreamento do terreno de 0 a 1" como parâmetro manual e estação do ano como "latitude subsolar ±1,54°". É física de enfeite: o relevo tem que vir do DEM.

### 13. taimashard0/spice1

- **Mapas de calor diários** e zoom por ano, mês e dia: é um jeito bom de mostrar meses de dados de uma vez.
- **Limiares editáveis** (o usuário define o que conta como "ter Sol").
- **O que evitar:** subir o projeto como um zip de 7.474 arquivos com dependências instaladas. Os juízes não vão baixar.

### 14. suhaslord/clps-lunar-browser

- **Formato JSON combinado antes** (sítio, hora, Sol e Terra com azimute, elevação e "visível") para o front e o back trabalharem em paralelo. Em 36 h, isso é essencial.
- **Divisão do time por área** escrita no README.
- **O que evitar:** o exemplo põe o Sol a 3,7° de elevação a 89,5°S, o que não acontece. Até dados falsos precisam ser plausíveis, porque alguém tira print.

### 15. shrestha-droid/clps-lunar-mission-browser

- **O mínimo viável:** uma página estática com dados do Horizons e só a biblioteca padrão do Python. Ficou no ar no GitHub Pages em um commit.
- **Lista honesta de "próximos passos",** com a máscara do LOLA como prioridade 1. É exatamente o que nos separa de um projeto raso.

### 16. friendlyfoe241-cyber/CLPS-Lunar-Mission-Browser

- **Pacote Python organizado por domínio** (efemérides, iluminação, terreno, sítios, coordenadas) e um docs/DATA_SOURCES.md. É uma boa estrutura de pastas para o nosso backend.
- **O que evitar:** README vazio com demo no ar. Ninguém entende o que é.

### 17. platonicHunter/CLPS-Lunar-Mission-Browser

- **O que evitar:** README padrão do create-next-app. É o primeiro arquivo que o juiz abre.

### 18. polcxw/clps-lunar-mission-browser

- **O que evitar:** colar o HTML inteiro dentro do README.

### 19. EAZYCODER2415/clps_lunar_mission_browser

- Componentes de interface separados (carta do céu, linha do tempo, barra de ferramentas). É uma divisão de telas parecida com a que vamos precisar.

### 20. kaveen-git12/nasa-clps-lunar-mission-browser

- Páginas de missões e planejador num React simples. Nada novo além da confirmação de que o "catálogo de missões" é a leitura mais comum do nome antigo do desafio.

### 21. joahan77/clps-lunar-mission-browser

- **"Documento mestre de contexto"** para trocar de assistente de IA sem perder nada. O nosso ai-memory faz isso, mas um arquivo no repo ajuda o resto do grupo.
- **O que evitar:** Shackleton em −89,9°S 0°E e dados de dezenas de missões sem foco no polo sul.

### 22. DinithMadushan/CLPS_Lunar_Mission_Browser_2026

- **O que evitar:** reaproveitar um projeto antigo (um mapa de sismos lunares) e trocar o nome. A falta de foco aparece no critério de Relevância.

### 23. nitrimandylis/space-apps-mockup

- **"O problema inteiro numa imagem":** a página inicial põe a Lua embaixo, o Sol afundando atrás dela e a Terra pendurada no alto. É uma ótima abertura de vídeo.
- **Honestidade com humor:** um selo "ephemeris: toy (for now)" e "not to scale (on purpose)".
- Usa os modelos 3D da NASA em glTF.

### 24. 0Aaheed0/SeleneSight

- Só a ideia. Mostra que muitos times ainda estão no começo.

### 25 a 27. yeskendir-sailau, ZCarlosZNica, quadruple-t

- Vazios. A única coisa a notar é que já usam o nome novo, "projeto analisado". O yeskendir fala em "segurança dos vizinhos" (neighbour safety), talvez a distância entre landers. Vale ficar de olho se o enunciado novo trouxer isso.

### 28. localizedprojects/CLPS-MOON-BROWSER (Lunar Horizon)

- **Núcleo em Dart (Flutter) compartilhado entre web e Android,** com pipeline Python que gera dados compactos e um arquivo `validation.json` que o próprio README usa para citar os números.
- **Busca da melhor janela:** o usuário escolhe a duração da missão (1 a 30 dias) e recebe o primeiro intervalo em que o Sol e a Terra ficam acima do horizonte durante a missão toda, mais um pouso sugerido. A regra do time é manter 0,25° de folga.
- **Eclipses lunares** tiram o Sol da fração visível, e o mastro (2 ou 10 m) é controle.
- **Embalagem de submissão:** `docs/submission.md`, `docs/judge_one_pager.md`, vídeo de 30 s e de 3:16 como arquivos de release, QR para instalar, nota de uso de IA no README (o time diz que usou o Claude Code e que escolheu e revisou tudo).
- **O que evitar:** a v1.14.0 a cinco dias do evento (lição 22) e um README com mais de 600 linhas.

- **[data anterior a 14/11/2026]:** versão 1.14.1, que mexe nos nomes de lugares da "Whole Moon" e põe o APK no repositório. Um arquivo de pesquisa dele diz que o Wueller 2026 (130 sítios) não pôde ser lido por causa do bloqueio da Wiley, o que confirma que os 130 sítios como base pronta seguem livres.

### 29. Mozahid-DIU/LunaHorizon

- **Horas douradas, elipse de pouso, replay de pousos reais e relatório de missão em A4 com QR** (lições 16 a 18).
- **Uma tela por pergunta:** Atlas, Sky, Dates, Power, Compare, Ellipse, 3D, Proof e Brief. Cada página tem uma lição curta ("modo sala de aula").
- **IA que não calcula:** o assistente só responde com números do motor, e há um registro de uso de IA (`docs/ai-use.md`).
- **O que evitar:** são nove telas. Em 36 h, não dá.

### 30. Arairo/NASA_lunarmoon (Lunar Site Planner)

- **Tudo em funções puras em `src/core/`,** usadas pela interface, pelos testes e pelas ferramentas offline.
- **Definições explícitas:** "tempo de Sol" e "Terra visível" contam qualquer pedaço do disco (como o mapa do Goddard), e o enlace direto exige o centro da Terra acima do horizonte com folga configurável (2° por padrão).
- **Limites conhecidos escritos:** a grade de 240 m suaviza o que tem menos de 0,5 a 1 km, e nas cristas o Sol pode mudar vários pontos percentuais.
- **Lição 19** (scripts de conferência ainda fora do repositório).

### 31. ziyadell/projeto analisado (LunaNav)

- **Cenários na URL** (`região,data,dias`), com dias fixos em 7, 14, 30, 60, 90, 180 ou 365.
- **Vista de superfície a 2 m do chão** separando camadas medidas de camadas só visuais (três presets).
- **O que evitar:** uma função de servidor com chave de voz (ElevenLabs) para o guia em áudio. Sem a chave, vira legenda. Mais uma coisa que pode falhar na demo.

- **[data anterior a 14/11/2026] (LunaNav):** passou a mostrar o tempo até o pôr do Sol e da Terra. Entra na lista da lição 13.

### 32. rodneymora94965/lunar-site-navigator

- **Calendário de janelas:** cada dia de chegada contra missões de 1 a 28 dias, em cores. Não dá veredito sobre a data e deixa de fora temperatura, poeira e risco de pouso.
- **Teste fixado antes:** cinco quadros do LROC escolhidos sem abrir a imagem, separados por limiar de Otsu e comparados com o modelo em 6.400 pontos (MCC por quadro).
- **Controle de seleção:** compara os 10 candidatos com 40 outros bolsões planos e 40 células aleatórias para ver de onde vem o viés de +7 pontos.
- **Imagens ilustrativas marcadas** como feitas com IA, com o aviso de que o lander, as pedras e os continentes são inventados.
- **9 pontos do Wueller et al. 2026,** numa seção à parte, fora do ranking. Dado e DOI citados no README.
- **O que evitar:** README longo duplicado em dois idiomas.

### 33. RootVandal/lunar-ops

- **Sem nota composta** e com a causa da falha classificada pelo dado: libração, uma crista a 37 km, buraco na DSN.
- **Demo guiada em 8 passos,** cada tela com URL que se compartilha.
- **Limites honestos:** a robustez ao DEM só aparece onde a NASA publica clones de erro, e a incerteza do pouso é uniforme.
- **Lição 20** (status e data declarados).

### 34. SammamMahdi/Penumbra

- **"Planeje para onde você pode cair, não para onde mira."** O ponto mais claro não é o mais seguro para mirar.
- **Validação e procedência dentro do app,** com os arquivos ligados por SHA-256.
- **O que evitar:** instalação com vários passos e pré-cálculo de 5 minutos em 16 threads. O README mostra o caminho offline, que é bom, mas não dá para o juiz rodar.

### 35. AshKareeem/Psut_Solaris

- **Para cada direção, o horizonte e também a distância e a identidade do relevo que bloqueia** (`horizon.npy`, `blocker.npy`, `complete.npy`). Serve para explicar "por que" o Sol sumiu.
- **Contrato de arquivos entre etapas** e um PDF do algoritmo inteiro. Útil para um time dividido por etapas.

- **[data anterior a 14/11/2026] (Psut_Solaris):** o commit mais novo fala em um app web "LunarWindow" com pontuação v4. Reforça que ele é o mesmo projeto do repositório 5.

### 36. Abrar5510/lunar-horizon

- **Ciência primeiro, interface depois:** o pipeline Python foi validado antes de portar para C++ e Unreal. O app em Unreal ainda não compilou, o que mostra o risco de escolher a interface mais pesada cedo.
- **Aviso de que o resultado vale para uma janela de 30 dias,** não para uma média anual.

### 37. gmrafi/cfsbr-selensync

- **O que evitar:** README enorme com selo de nomeação em [período anterior] e modelo de custo de missão. Não é o que o enunciado pede, e a alegação não está conferida.

### 57 a 64 (nível 2, [data anterior a 14/11/2026])

- **57, Clearway:** modo simples e Planner sobre o mesmo resultado (lição 24), Monte Carlo com intervalo de Wilson e a ressalva escrita de que é "uma medida de fragilidade, não uma probabilidade calibrada de sucesso". Essa frase vale copiar em espírito. O que evitar: README gigante e um commit só, que não deixa o juiz ver o histórico.
- **58, LunaMission:** solver de eventos com refinamento por Brent até 1 s, enlace da DSN com difração do relevo e uma página de metodologia. Declara 1.578 testes. O que evitar: o app exige Bun, Python e vários pacotes, difícil para o juiz rodar.
- **59, Sylesh29:** "atrasar B 72 h" (lição 25), dois modelos de terreno (lição 26), CSV de todos os casos checados e link que reabre o mesmo cenário. A tabela de validação traz limite e resultado lado a lado. Tudo em 5 commits no dia da criação.
- **60, Lunar Horizon Wheel:** faixas P10–P90 (lição 27), RMSE contra o Goddard (lição 28) e a "roda do horizonte". Está no ar.
- **61, CHANDRA:** bloqueia o que falha na validação (lição 30) e deixa claro que não é um produto da NASA.
- **62, pythonhack000:** contagem regressiva ao lado do panorama, erro máximo de 0,006° contra o Horizons em dois anos. Está no ar e segue o enunciado de perto.
- **63, Echo-Path:** simulação de pouso 3D com desvio no voo, mais uma comparação de sítios. Ficou com dois enfoques e começou antes do evento (lição 34). O que evitar: a mistura dilui a pergunta.
- **64, Edge of Light:** testa 11.844 sítios candidatos para cada dia de pouso, bilíngue (inglês e árabe). Mostra que dá para pré-calcular uma grade inteira e responder "onde?" sem digitar coordenadas.

### 65 (Ridgeline, [data anterior a 14/11/2026])

- **De 19 para 27 commits:** cliente do Horizons com validação e página inicial. O README ainda marca como "planned" o buscador de janelas, o quadro de cenários e o painel de validação. Lição 40.

### 76. Kayseve/projeto analisado-416 (lido em [data anterior a 14/11/2026], sumiu em 12/11)

- **Um servidor FastAPI e front sem build** (módulos ES e Three.js por CDN). Um `run.sh` baixa ~80 MB de dados NASA uma vez e sobe tudo. Simples de rodar.
- **Horizonte e Sol como disco:** ray-marching em 360 azimutes até 250 km, com curvatura, Sol de 0,53° e Terra visível quando o centro passa do terreno (com máscara de antena opcional).
- **Mapa polar de Sol e Terra por pixel** para o instante escolhido, que mostra quais cristas estão iluminadas e quais veem a Terra.
- **Nota de comparação escrita como auxílio e não como veredito:** 0,45 × % de Sol + 0,35 × % de Terra + 20 × (1 − maior noite / 14,77 d).
- **Limites escritos:** coordenadas das regiões aproximadas; a 240 m o horizonte erra pedras e crateras pequenas; fora do polo, o DEM de 1,9 km suaviza.
- **O que evitar:** um commit só e nenhuma demo pública. Quem avalia não vai instalar Python e baixar 80 MB.

### 57. devadd2105-max/clearway (o que a leitura de [data anterior a 14/11/2026] anotou a mais)

- **A pergunta completa:** luz → potência → aquecedores → bateria → sobrevivência, e Terra acima do relevo → enlace. A resposta é sítio **e** data, o fator que limita e quanto confiar.
- **Seção "quanto confiar":** separa o que é modelado, o que é suposto e o que não é modelado, refaz o ranking com o horizonte subido e descido, com outra margem de enlace e com a Lua lisa, e compara com os mapas de média de 18,6 anos da NASA, mostrando a diferença por sítio.
- **Três níveis de "enlace":** visibilidade geométrica, linha de visada pelo terreno e cobertura da DSN. Reforça a lição de separar geometria de sobrevivência (10).
- **Modos Simples, Planner e Explain** (notas de sala de aula) e um desafio "Landing Director" com GO, HOLD e SCRUB.
- **O que evitar:** o escopo (lançamento, transferência, páginas de autor, jogo). Em 36 h, impossível.

### 38 a 56 (resumo)

- **38 (LuminaLuna), 43 (MoonSight):** usam o Horizons sem relevo e dizem isso no README. É a versão "mínimo viável" que a lição do shrestha-droid (15) já descrevia.
- **39 (M9nx), 40 (xiangen-coder):** dizem no README que os cálculos validados ou o DEM ainda não estão ligados. Honestos, mas incompletos.
- **41 (Lunar-portal):** em árabe, com 44 fontes citadas e 130 termos no glossário.
- **47, 48, 51, 52:** README padrão do template, vazio ou ausente (ver "o que evitar" do 17).
- **49 (KaranDev316):** dados de mentira declarados no README.
- **53 a 55:** só README ou vazio.
- **56 (Marwane-Haddane):** outro tema (dinâmica de descida), não compara sítios.


### 65 a 111 (resumo, [data anterior a 14/11/2026])

- **65 (Ridgeline):** o README é um plano muito parecido com o nosso (contagem regressiva em janela, quadro de cenários, buscador de janelas, painel de validação) e declara o que ainda é "planned". É um aviso de que a ideia da arquitetura proposta não é exclusiva. Já tem o pipeline do horizonte (marco M3).
- **67 (SUNFYRE), 68 (LUNA-OPS), 79 (nahsed7):** motores com procedência e incerteza, mas com um commit só ou dois. O 68 separa em tabela o que é real, o que precisa baixar e o que é sintético, e é um bom modelo de README.
- **70:** README em português com um "deep dive" de desempenho (lição 33).
- **75:** maquete de mesa com horizonte impresso (lição 32).
- **66, 69, 71 a 74, 76 a 78, 81 a 83:** protótipos com dados sintéticos ou sem validação. Alguns (69, 74) avisam isso no README (lição 31).
- **84, 85, 91, 92, 80:** só plano, site do time ou quadro de tarefas. O 91 tem login e quadro de tarefas funcionando e nenhum cálculo ainda.
- **86 e 66:** README com contas de teste para o juiz e documentação enorme. É o oposto do que queremos: o primeiro arquivo que o juiz abre devia dizer o que o app faz.
- **87 a 90, 93 a 111:** catálogos de missões, README de template ou vazio, e outros temas (detecção de perigo por IA no 94 e no 96, simulador de descida em 56). Mostram, de novo, que a leitura do nome antigo, "navegador de missões CLPS", ainda é comum.


### 112 a 124 (resumo, [data anterior a 14/11/2026])

- **112 (Lunar Site Intelligence):** score aberto com intervalo de 90% por Monte Carlo e mapas RMS do Barker (lição 40). Outro enfoque, sem Sol e Terra.
- **115 (Skepticallii):** Streamlit com modelos de energia, enlace direto e terreno, e um script de validação contra o SPICE. README de uma linha: o juiz abre e não entende (ver "o que evitar" do 17).
- **117 (DesertStar):** lição 37. O README também pede crédito a quem reaproveitar o código, o que é um bom lembrete de que os nossos créditos de dados e de IA têm de estar escritos.
- **120 (Moonfix):** 72 h de 14 a 16/11 já calculadas num HTML offline, com margens de 0° a 3° e um relatório para imprimir. É a maior prova de que dá para entregar bem uma janela curta, e também o exemplo de pré-trabalho para os dias do evento (lição 34). Nós só começamos em 14/11.
- **121 (Lunar Landing Navigator):** lição 39. Feito e publicado em 12/11 no GitHub Pages.
- **113, 114, 116, 118, 119, 122, 123, 124:** protótipos, outro enfoque ou vazios. O 123 é só o nome do desafio num repositório vazio.
- **48, 71, 76, 84, 105:** sumiram em 12/11 (404). As demos do 47, do 78 e do 89 caíram. Ter demo no ar até a hora do julgamento é um risco real: vale um plano B (vídeo e link estático).


### 125 a 169 (resumo, [data anterior a 14/11/2026])

- **125 (Sunchaser, Eternal Light, Cairo):** regra de aprovação escrita antes de cada conferência e falhas mantidas no registro, como nós. Declara o Connecting Ridge contra o Barker [período anterior] (91,26% contra 91,11%), um número de referência para conferir no artigo antes de usar. O endereço do README deu 404 em 13/11.
- **126 (Lunar Mission Planner):** tabela "objetivo do enunciado → onde está no app" no README (lição 53 para a introdução). 118 commits num repositório criado em 13/11, então o trabalho veio de outro lugar.
- **127 (404 agents, Naryn):** veredito e onze conferências (lição 51); o ponto usado é o mais iluminado e plano dentro de 500 m, e a tela diz a distância (lição 3).
- **128 (Black Lotus, Dhaka):** cada prompt de IA guardado na íntegra em docs/ai_log.md. É a declaração de uso de IA mais completa que vi.
- **129 (Moussa-dme):** Blue Ghost 1 e 14 pousos históricos na validação (lição 54); API com OpenAPI e .ics.
- **130 (LUNAR-P/OPS):** estende o 4 com crédito e marca todo resultado como "COMPUTED_UNVERIFIED". Reaproveitar código de outro time com crédito é legal pela licença; para nós continua valendo a implicação 6 de [concorrencia.md](concorrencia.md).
- **131 (Lunar Lighting Planner):** diz que não é submissão por ter sido feito em 13/11 (lição 55) e dá o motivo de cada falha em palavras (lição 50).
- **132 a 169:** estrutura de time, protótipos, dados ilustrativos, outro enfoque ou vazios. O 133 (Al Ostora) já tem o fluxo com dados de demonstração e entrega no sábado.

### 170 a 292 (resumo, 14/11/2026)

- **170 (Purple Haze, Surat):** lições 56, 57, 58 e 62. Também escolhe o melhor pixel em 60 m do ponto publicado e diz quanto moveu (lição 3), e chama a fração do disco e a visibilidade do Sol pelos nomes do Gläser, explicando a diferença de uns 5 pontos.
- **182 (Wasl, Cairo) e Orrery Space (sem repositório):** lição 61. O Wasl também mostra o ponto mais iluminado a 0,6–1,9 km do publicado, com um botão para voltar ao publicado.
- **125 (Sunchaser):** entrou no ar com tour de 90 s e "histórias de missão".
- **185 (LunaMap, Taipei):** usa a Tabela A1 do Wueller 2026 e confere cada coordenada contra a caixa do gazetteer do acidente. É o único que vi citar a tabela. A tela avisa que o relevo não é modelado.
- **194 (ViaLunae, Fortaleza):** lição 60.
- **189 (Bean Drift) e 170:** dizem que partiram de trabalho anterior. Lição 62.
- **171 a 183 e o resto:** o formato mais comum no primeiro dia é sítio + data, Sol e Terra sobre o LOLA, contagem e "e se escorregar?". Isso virou o básico do desafio.

## Números de referência que vieram junto

Segundo a tabela do BroBYW. **Conferir no artigo antes de usar.**

| Ponto | Altura | Fração média do disco | Algum pedaço do Sol | Maior escuridão |
|---|---|---|---|---|
| Gläser [período anterior] C1, Connecting Ridge | 2 m | 88,0% | 92,1% | 112 h |
| Gläser [período anterior] C2 | 2 m | 78,1% | 82,0% | 165 h |
| Gläser [período anterior], borda de Shackleton | 2 m | 85,5% | 89,4% | 66 h |
| Gläser [período anterior] CR1, ponto 2 | 2 m | 87,9% | 92,3% | 110,9 h |
| Gläser [período anterior] CR1, ponto 4 | 10 m | 91,9% | 95,66% | 76,1 h |

Inconsistências entre fontes, segundo o mesmo time:
- o Speyerer [período anterior] aparece com ~94% e com 92,1% para o mesmo conjunto;
- a maior escuridão na borda do Mazarico aparece como ~1,5 dia e como 141 h.

## O que entra no nosso plano

- [ ] Perguntar ao Local Lead: regras e prazos do evento local; se pode ter documento de conceito, dados baixados e templates antes de 14/11.
- [ ] Escrever o nosso PROMPT.md (visão, P0/P1/P2, métricas definidas, "o enunciado oficial vence"), para usar só em 14/11.
- [ ] Regra do ponto representativo: o ponto mais alto da região, ou dentro de 250 m da coordenada publicada.
- [ ] Plano de validação:
  - Horizons (no máximo 25 instantes por pedido);
  - terreno sintético;
  - mapa de PSR;
  - Gläser [período anterior]/[período anterior] na mesma altura;
  - PGDA 69;
  - pôr do Sol do Blue Ghost 1.
  
  Tolerâncias escritas antes, mais um controle negativo.
- [ ] Rever a [arquitetura proposta](arquitetura-proposta.md): a máscara calculada na hora é viável (~130 ms), e dá para ler janelas do DEM por HTTP range.
- [ ] Mastro como envelope de retas, se der tempo. Senão, poucas alturas fixas e o aviso de que é aproximado.
- [ ] AI_USAGE.md datado desde a primeira hora do hackathon.
- [ ] Roteiro do vídeo de 30 s com uma tabela fechada de números, sem logo da NASA.
- [ ] Contagem regressiva: mostrar como número grande, junto da causa (o relevo que esconde o Sol ou a Terra), já que ela não é mais exclusiva (lição 13).
- [ ] Escrever, antes de 14/11, a lista do que a validação cobre e do que não cobre, e guardar o script de cada número que formos citar (lições 14 e 19).
- [ ] Decidir se a tela principal responde "quando?" (janela), "onde?" (comparação) ou as duas, em uma pergunta no topo (lições 15 e 23).
- [ ] Declarar no app a data de início do código (14/11) e o status do repositório de estudo (lição 20).
- [ ] Conferir se o nosso time aparece na aba Teams do Guarulhos para o projeto analisado (em 09/11, 11/11 e [data anterior a 14/11/2026] não aparecia, ver [concorrencia.md](concorrencia.md)).
- [ ] Escolher uma frase de limite para a tela principal, no formato do Clearway: o que o número mede e o que ele não é ("uma medida de fragilidade, não uma probabilidade calibrada") (lição 24).
- [ ] Decidir se o "e se?" é a tela principal. O 59 já faz atrasar B em 72 h e a busca da data no entorno do ponto. Se for, mostrar qual restrição quebrou (lição 25).
- [ ] Pensar em uma frase de incerteza do relevo com a fórmula do Barker, que ninguém usa ainda, e conferir se dá tempo (lição 27).
- [ ] Perguntar ao Local Lead se projetos ou protótipos feitos antes de 14/11 valem no nosso evento, já que há times declarando isso (lição 34).
- [ ] Perguntar ao Local Lead de Guarulhos se há seleção de times, vagas ou prazos de vídeo e de entrega além do vídeo de 30 s ou dos 7 slides do guia global (lições 36 e 37).
- [ ] Criar a pasta de entrega com um arquivo por pessoa (quem fala, quem grava, quem edita) e o roteiro do vídeo, no formato do POLAR WINDOW, para usar em 14/11 (lição 38).
- [ ] Ter um plano B para a demo (vídeo e link estático), já que 3 demos de outros times caíram em um dia (ver "112 a 124").
- [ ] Tratar o "e se?" (data e sítio vizinho) como o mínimo, não como diferencial, e mostrar a causa da mudança junto (lição 41).
- [ ] Se compararmos sítios com números muito próximos, dizer quando não dá para separar, em vez de forçar um ranking (lição 42).
- [ ] Pôr a causa do pôr do Sol e da Terra (o Occluder) na tela inicial, porque é o único pedaço da tela central que nenhum site tem (lições 45 e 46, issue #24 do app).
- [ ] Abrir a página de prova com três números de resumo antes da lista (lição 47, issues #23 e #28 do app).
- [ ] Mostrar a fonte da coordenada ao lado do nome do sítio (lição 48, issue #21 do app).
- [ ] Medir no celular o tempo até a primeira resposta do deploy; dois sites fortes levam de 18 a 40 s (ver [sites-concorrentes.md](sites-concorrentes.md)).
- [ ] Pôr o Occluder com nome e distância na primeira frase do vídeo e da tela, agora que outros já dizem "escondido atrás do terreno" (lição 50).
- [ ] Pensar num selo de origem (calculado, publicado) ao lado dos números da tela principal (lição 52, issue #23 do app).
- [ ] Usar a ideia do controle de latitude (equador contra polo) nos primeiros segundos do vídeo (lição 53).
- [ ] Perguntar ao Local Lead como será lido um histórico com commits antes de 14/11 (lição 55).
- [ ] Tirar do pitch e do vídeo qualquer frase de que só nós nomeamos o relevo; o 170 também faz (lição 56).
- [ ] Pensar em mostrar a hora do pôr do Sol sem relevo ao lado da contagem (lição 57).
- [ ] Escrever na página de prova o critério do Blue Ghost 1 e por que ele falha, sem mexer na tolerância (lição 58, issue #75 do app).
- [ ] Usar os cenários com nome de história como roteiro do vídeo de 30 s (lição 61).
- [ ] Pensar num link "conferir no Horizons" ao lado do Sol e da Terra na resposta (lição 75).
- [ ] Dizer na tela que a Terra conta pelo centro, porque dois fortes dão 29 h a mais no Connecting Ridge (lição 76).
- [ ] Mostrar a contagem do Sunset e do Earthset como janela pela incerteza do relevo, numa frase (lição 77, #49).
- [ ] Usar a frase do 220 como modelo do plano B no atraso: "vira GO se pousar N dias depois" e o melhor sítio na nova data (lição 78, #246).
- [ ] Tirar "o único site em português" do pitch: o 166 também é (lição 80, #180).
- [ ] Pensar em mostrar no Cursor a parte do disco do Sol à vista (o `Sky` já tem o número e só o usa na luz), porque na Athena o Sol começa cortado (lição 83).
- [ ] Mostrar as horas de Terra com a faixa da regra do disco, do centro a qualquer pedaço, como o 453 (lição 84, #245).
- [ ] Usar no pitch o caso do ponto a 500 m da crista que perde o Sol por 4,6 dias como argumento da escada de resolução (lição 85).
- [ ] Mostrar na Prova, ao lado da falha do Wueller, a mediana e a correlação com o SunDays27, como o Fly Me to the Moon, sem mudar a tolerância (lição 87).
- [ ] Pôr na linha do LROC da Prova o mesmo teste com o horizonte plano, como o Ridgelight (lição 89).
- [ ] Escrever a faixa do DEM como "a escolha entre dois Sites vira ou não vira", como o SITE REGRET (lição 90, #49).
- [ ] Contar no pitch a bateria com os painéis fixos num azimute junto da Athena, que tombou com os painéis para o lado errado, como pergunta o LANDERPRINT (lição 95, #180).
- [ ] Abrir a Prova com uma lista curta do que ainda não conferimos, como o 490, sem mudar nenhuma tolerância (lição 96).
- [ ] Usar no pitch a concordância de outras ferramentas no nascer da Terra do Connecting Ridge (Zoriana às 16:05, Recife às 15:47), sem chamá-las de referência independente na Prova (lição 98, #180).
- [ ] Escrever a faixa do DEM em horas de Sol ou como intervalo da hora do pôr, de P10 a P90 ou com o ± da escada, como o LunarSync, o moonle e o CeyNova (lição 99, #49).
- [ ] Antes de enviar, abrir o link público de fora da rede do Luiz (celular no 4G) e conferir que ele responde (lição 100).
- [ ] Pensar em dizer, no painel de atraso, por que a Janela perde horas (o dia lunar, a libração ou o relevo com o Occluder nomeado), como o Slip Impact Brief (lição 103).
- [ ] Usar no pitch que o relevo que esconde a Terra no Connecting Ridge está a 134 e 140 km, e que ferramentas com horizonte curto a veem nessa hora (lição 104, #180).
- [ ] Atualizar no pitch a frase do nascer da Terra no Connecting Ridge: agora são quatro ferramentas de fora a até 5 min do nosso (Zoriana, Earthset, Noctis Horizon, Lunar Window), sem chamá-las de referência na Prova (lição 105, #180).
- [ ] Conferir, antes de enviar, que cada número da capa, do vídeo e do pitch aparece na Prova ou nas Estatísticas para nerds (lição 106).
- [ ] Pensar num aviso por Site quando a resposta vira com poucos metros, como o "knife-edge" do HORIZON (lição 107, #49).
- [ ] Pensar em pôr na Prova o Gläser [período anterior] no Connecting Ridge (92,27% de Sol a 2 m, como os dois times citam; conferir no artigo o período e o ponto exatos) como referência do ponto B, sem mudar nenhuma tolerância (lição 109).
- [ ] Usar no pitch o par do Sharp Navigation: o mesmo Connecting Ridge, 200 m mais baixo, perde o Sol no pouso (lição 108, #180).
- [ ] Pensar em pôr na tela, junto da #245, a regra do disco com o número: pela borda de baixo da Terra o ponto B dá 43,0%, como o LunarSims, e pelo centro 46,8% (lição 112).
