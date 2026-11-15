# Luna Investigation

Projeto de pesquisa para o **NASA Space Apps Challenge 2026** (14 e 15 de novembro de 2026), focado em investigação de sítios de pouso lunar.

## A ideia em uma frase

Uma ferramenta em que qualquer pessoa, seja engenheiro de missão, professor ou curioso, escolhe um **sítio de pouso na Lua** e uma **data** e vê na hora **onde estão o Sol e a Terra em relação ao horizonte real** daquele lugar: quanto tempo de luz para os painéis solares, quando dá para falar com a Terra e quanto falta para o pôr do Sol e para o "pôr da Terra".

## Por que isso é difícil hoje

As ferramentas que já existem (Moon Trek, LROC Quickmap, JPL Horizons) são feitas para análise detalhada por especialistas. Responder "e se a gente atrasar o pouso duas semanas?" ou "e se pousarmos 5 km ao lado?" exige navegar por várias interfaces e interpretar dados brutos.

No polo sul isso é crítico. O Sol fica rasante (±1,5°) e gira em volta do horizonte, então **o relevo decide tudo**. Em [período anterior], o lander IM-2 Athena pousou a algumas centenas de metros do alvo (250 m segundo a Intuitive Machines, mais de 400 m segundo a NASA), dentro de uma cratera, tombou, ficou sem Sol nos painéis e a missão acabou em menos de 13 horas.

## Estado atual

Este repositório registra a **pesquisa e a preparação científica** do time. A implementação do projeto deve começar a partir do hackathon, conforme a regra do Space Apps (ver [hackathon-referencias.md](docs/hackathon-referencias.md)). Até aqui, o repositório guarda física, artigos, dados de referência, regras, concorrência e o plano — não código do produto.

---

## Guia do repositório

### O que tem aqui

```
.
├── README.md                     este guia
├── .gitignore                    deixa de fora DEMs, kernels SPICE e outros arquivos grandes
├── docs/
│   ├── desafio.md                o enunciado e o briefing do grupo
│   ├── hackathon-referencias.md  julgamento, regras, vencedores, evento local e Connect
│   ├── fisica-polo-sul.md        Sol, Terra, horizonte e energia no polo sul
│   ├── glossario.md              DEM, LOLA, PDS, SPICE, DTE e outros termos
│   ├── artigos.md                os 18 artigos principais e os fatos conferidos
│   ├── leituras.md               notas da leitura completa, linha a linha
│   ├── fontes.md                 catálogo de dados, kernels, ferramentas e missões
│   ├── concorrencia.md           os 905 times do desafio e onde dá para se diferenciar
│   ├── repos-concorrentes.md     os 27 repositórios de outros times, com link e resumo
│   ├── licoes-concorrentes.md    o que aprender (e evitar) com cada um deles
│   ├── arquitetura-proposta.md   arquitetura e cronograma propostos (em discussão)
│   └── curso-otimizacao.md       onde o curso de otimização entra no projeto
└── sites/
    ├── README.md                 explica a tabela, os códigos das regiões e outros sítios
    └── artemis_sitios_wueller2026.csv   130 sítios do Artemis com dias de Sol e Terra ([período anterior]–2032)
```

### Por onde começar

Depende do que você vai fazer no time:

| Você é... | Leia nesta ordem |
|---|---|
| **Quem acabou de chegar** | [desafio.md](docs/desafio.md) → [glossario.md](docs/glossario.md) → [fisica-polo-sul.md](docs/fisica-polo-sul.md) → [concorrencia.md](docs/concorrencia.md) |
| **Quem vai programar o cálculo** (Sol, Terra, horizonte) | [fisica-polo-sul.md](docs/fisica-polo-sul.md) → [fontes.md](docs/fontes.md) (seções 1 a 3) → [licoes-concorrentes.md](docs/licoes-concorrentes.md) (lições 3 a 9) → [arquitetura-proposta.md](docs/arquitetura-proposta.md) |
| **Quem vai fazer a interface** | [desafio.md](docs/desafio.md) → [licoes-concorrentes.md](docs/licoes-concorrentes.md) (BroBYW, EmanuelAbasto, nitrimandylis) → [arquitetura-proposta.md](docs/arquitetura-proposta.md) |
| **Quem vai cuidar dos dados e da validação** | [sites/README.md](sites/README.md) → [fontes.md](docs/fontes.md) → [artigos.md](docs/artigos.md) → [licoes-concorrentes.md](docs/licoes-concorrentes.md) (números de referência no fim) |
| **Quem vai fazer o vídeo e a apresentação** | [hackathon-referencias.md](docs/hackathon-referencias.md) → [concorrencia.md](docs/concorrencia.md) (Implicações) → [licoes-concorrentes.md](docs/licoes-concorrentes.md) (lições 11 e 12) |

### Os documentos por assunto

**O desafio e as regras**

| Documento | O que tem | Quando usar |
|---|---|---|
| [docs/desafio.md](docs/desafio.md) | O texto do desafio, o que ele pede, as datas e o briefing do grupo | Para lembrar o que a NASA quer de verdade |
| [docs/hackathon-referencias.md](docs/hackathon-referencias.md) | Os 5 critérios de julgamento (mesmo peso), o funil local → global, o formato da demo (vídeo de 30 s ou 7 slides, em inglês), a regra de declarar uso de IA, a de não começar antes de 14/11 e os vencedores de [período anterior] e [período anterior]. Também o nosso evento local (Guarulhos, virtual) e o que o GO Team respondeu no Space Apps Connect, com os horários de início e de submissão | Antes de decidir escopo e antes de montar a apresentação |

**A ciência**

| Documento | O que tem | Quando usar |
|---|---|---|
| [docs/fisica-polo-sul.md](docs/fisica-polo-sul.md) | Como o Sol e a Terra se movem vistos do polo, a receita da máscara de horizonte, a energia solar, as métricas (iluminação média, visibilidade solar, maior noite) e como validar | Base de todo o cálculo |
| [docs/glossario.md](docs/glossario.md) | O vocabulário do projeto em português simples | Quando aparecer uma sigla |
| [docs/artigos.md](docs/artigos.md) | Os 18 artigos principais: o que cada um diz, os números conferidos e as correções que fizemos | Para citar um número com segurança |
| [docs/leituras.md](docs/leituras.md) | As notas da leitura completa de 16 dos 18 artigos | Para ir ao detalhe de um artigo |
| [docs/curso-otimizacao.md](docs/curso-otimizacao.md) | As aulas do curso de otimização do Prof. Marcato (UFJF) e onde elas entram no projeto | Se formos otimizar ou ordenar sítios por vários critérios (o TOPSIS está na [arquitetura proposta](docs/arquitetura-proposta.md)) |

**Os dados**

| Documento | O que tem | Quando usar |
|---|---|---|
| [docs/fontes.md](docs/fontes.md) | Onde baixar cada coisa: DEMs do LOLA, mapas de iluminação do PGDA, kernels SPICE, JPL Horizons, coordenadas de sítios, histórico das missões, requisitos do Artemis, o arquivo SPICE do CLPS e as máscaras das antenas da DSN | Na hora de montar o pipeline de dados |
| [sites/README.md](sites/README.md) | O que significa cada coluna da tabela de sítios, os códigos das regiões, as datas do meio do verão lunar e outros sítios (Chandrayaan-3, Chang'e-7) | Antes de usar o CSV |
| [sites/artemis_sitios_wueller2026.csv](sites/artemis_sitios_wueller2026.csv) | 130 sítios dentro das regiões do Artemis III, com os dias seguidos de Sol e de Sol + Terra de [período anterior] a 2032 (Wueller et al. 2026, CC-BY 4.0) | Lista pronta de sítios e gabarito de validação |

**A concorrência**

| Documento | O que tem | Quando usar |
|---|---|---|
| [docs/concorrencia.md](docs/concorrencia.md) | Os 905 times do desafio por país e tema, quem já tem código, quem escreveu o desafio, as ferramentas que já existem e onde ainda dá para se diferenciar | Para decidir o que fazer diferente |
| [docs/repos-concorrentes.md](docs/repos-concorrentes.md) | Os 27 repositórios públicos de outros times em três níveis, com link, demo, linguagem, commits e resumo | Para olhar um concorrente específico |
| [docs/licoes-concorrentes.md](docs/licoes-concorrentes.md) | As 12 lições que mais mudam o plano, o que aprender e o que evitar em cada repositório, números de referência e um checklist | Para não repetir erros e aproveitar o que já se descobriu |

**O plano**

| Documento | O que tem | Quando usar |
|---|---|---|
| [docs/arquitetura-proposta.md](docs/arquitetura-proposta.md) | Uma proposta de arquitetura (o que pré-calcular, o que calcular no navegador), funcionalidades extras (modo Artemis III, porto seguro, ranking) e o cronograma até 15/11. **Ainda não foi aceita pelo grupo** | Para discutir com o time como vamos construir |

### O que não fica no repositório

- **Dados grandes:** DEMs (`.tif`, `.img`, `.jp2`) e kernels SPICE (`.bsp`, `.bpc`, `.tls`) ficam fora do Git pelo `.gitignore`. As instruções de download estão em [fontes.md](docs/fontes.md).
- **PDFs dos artigos:** não estão aqui por causa de direitos autorais. Os links estão em [artigos.md](docs/artigos.md).
- **Segredos:** `.env` e chaves nunca entram no Git.

### Como trabalhamos aqui

- **Tudo em português.** O código e a apresentação final vão ser em inglês, como o Space Apps pede.
- **Commits no padrão Conventional Commits** (`docs:`, `feat:`, `fix:`, `chore:`...), escritos como a gente fala.
- **Nada de código do projeto antes de 14/11.** O histórico anterior a essa data contém apenas estudo e documentação.
- **Uso de IA declarado.** O desenvolvimento após 14/11 deve manter um registro do que a IA fez, como o regulamento pede.
- **Números com fonte.** Todo número que for parar na ferramenta ou na apresentação precisa ter um artigo ou dado por trás. Quando a fonte é de segunda mão, o documento avisa.

---

## Datas

| Data | O que acontece |
|---|---|
| 06/11 a 27/11/2026 | Meio do verão lunar no polo sul: o período com mais Sol, e o hackathon cai dentro dele |
| [data anterior a 14/11/2026] | A NASA libera os Resources oficiais do desafio |
| 14/11/2026, 9h | Começa o hackathon e abre a submissão |
| 15/11/2026, 23h59 | Fecha a submissão (horário local) |

## Pendências antes do hackathon

- [x] Escolher o evento local: Guarulhos, virtual, da Comunidade Hackathon Brasil.
- [ ] Confirmar a inscrição do time em Guarulhos (em 04/11 a gente não aparecia na aba Teams).
- [ ] Mandar as perguntas ao Local Lead (estão em [hackathon-referencias.md](docs/hackathon-referencias.md#o-nosso-evento-local-guarulhos)).
- [ ] Escrever o PROMPT.md com a visão, as prioridades e as métricas, para usar só em 14/11.
- [ ] Fechar o time e os papéis.
- [ ] Ler os Resources em 13/11 e ajustar o plano. Ativar as Global Offers no mesmo dia.
- [ ] Reconferir o status das missões (Griffin-1 pode lançar perto do hackathon).
- [ ] Conseguir os PDFs do Mazarico [período anterior] e do Gläser [período anterior].
