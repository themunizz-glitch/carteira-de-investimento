
# Carteira de Investimentos

Projeto desenvolvido para a disciplina **Algoritmos e Pensamento Computacional**, com evolução em três etapas: CP1, CP2 e CP3.

## 1. Descrição do projeto

A **Carteira de Investimentos** é uma aplicação em terminal, desenvolvida em linguagem C, que permite cadastrar e acompanhar ativos financeiros de forma simples e educativa. O sistema calcula a rentabilidade, o lucro ou prejuízo e o valor total da carteira, além de oferecer ordenação dos ativos, simulação de investimentos e geração de um relatório final.

O projeto evoluiu em três etapas:

- **CP1:** cadastro e análise de um único ativo, utilizando funções e menu interativo.
- **CP2:** gerenciamento de até 100 ativos com `struct`, vetores e armazenamento em arquivo de texto.
- **CP3:** implementação da ordenação por rentabilidade, simulador educativo de 12 meses e relatório final consolidado.

## 2. Público-alvo

O sistema é destinado a estudantes, iniciantes em programação e pessoas interessadas em compreender conceitos básicos de investimentos, como rentabilidade, lucro, prejuízo e risco financeiro.

Seu principal objetivo é contribuir para a educação financeira, oferecendo uma ferramenta simples e acessível para fins didáticos.

O programa não fornece recomendações financeiras reais nem substitui análises profissionais.

## 3. Funcionalidades do sistema

A versão final, correspondente ao CP3, possui as seguintes funcionalidades:

### 1. Cadastrar ativo

Permite registrar um investimento informando nome, categoria, quantidade, preço de compra e preço atual. Os dados são armazenados automaticamente no arquivo da carteira.

### 2. Listar ativos

Exibe todos os investimentos cadastrados, incluindo suas informações e a rentabilidade individual.

### 3. Valor total da carteira

Calcula o valor total dos investimentos, considerando o preço atual e a quantidade de cada ativo.

### 4. Rentabilidade geral

Apresenta a rentabilidade percentual da carteira, o lucro ou prejuízo acumulado e uma classificação didática de risco.

### 5. Ordenar por rentabilidade

Organiza os ativos do maior para o menor desempenho utilizando o algoritmo Bubble Sort. A nova ordem é salva no arquivo.

### 6. Simulador educativo

Compara o valor total da carteira aplicado durante 12 meses em três modalidades:

- Poupança.
- Tesouro Selic.
- CDB.

Utiliza taxas mensais ilustrativas definidas no código e apresenta explicações simples sobre rentabilidade e risco.

### 7. Relatório final

Apresenta um resumo completo contendo:

- Ativos ordenados por rentabilidade.
- Valor total da carteira.
- Rentabilidade geral.
- Lucro ou prejuízo total.
- Texto sobre o impacto social da educação financeira e sua relação com o ODS 8.10 da ONU.

### 0. Sair

Salva os dados da carteira e encerra o programa.

### Fórmulas utilizadas

**Rentabilidade individual (%):**

`(precoAtual - precoCompra) / precoCompra * 100`

**Lucro ou prejuízo (R$):**

`(precoAtual - precoCompra) * quantidade`

**Valor total da carteira (R$):**

Soma dos valores de `precoAtual * quantidade` de todos os ativos.

**Rentabilidade geral (%):**

`(valorAtualTotal - valorInvestidoTotal) / valorInvestidoTotal * 100`

### Classificação didática de risco

- **Alto:** rentabilidade inferior a -10%.
- **Moderado:** rentabilidade de -10% até abaixo de 0%.
- **Baixo:** rentabilidade igual ou superior a 0%.

**Observação:** a classificação é utilizada exclusivamente para fins educacionais. Ela não representa uma avaliação real do risco de um investimento. As taxas do simulador também são ilustrativas e não correspondem necessariamente às taxas praticadas no mercado.

### Armazenamento

O sistema permite cadastrar até **100 ativos**, utilizando o arquivo `data/carteira.txt`.

Cada registro possui o seguinte formato:

`nome;categoria;quantidade;precoCompra;precoAtual`

Caso o arquivo não exista, o programa inicia com a carteira vazia e cria o arquivo quando os dados são salvos, desde que a pasta `data` esteja disponível.

## 4. Tecnologias utilizadas no desenvolvimento

O projeto utiliza as seguintes tecnologias e conceitos:

- **Linguagem C:** desenvolvimento das funcionalidades do programa.
- **Compilador GCC:** compilação e geração do executável.
- **Bibliotecas padrão da linguagem C:** entrada e saída de dados, operações matemáticas e manipulação de arquivos.
- **Structs e vetores:** organização e gerenciamento dos ativos.
- **Arquivos TXT:** armazenamento persistente dos investimentos.
- **Bubble Sort:** algoritmo de ordenação dos ativos.
- **Terminal:** interface de interação com o usuário.

### Estrutura do projeto

```text
carteira-investimentos/
├── src/
│   ├── main.c
│   ├── funcoes.c
│   └── modulo.c
├── include/
│   ├── funcoes.h
│   └── modulo.h
├── data/
│   └── carteira.txt
└── README.md
```

**Descrição dos arquivos:**

- `src/main.c`: controla o menu principal e o fluxo de execução.
- `src/funcoes.c`: contém as funções originais desenvolvidas no CP1.
- `include/funcoes.h`: declara os protótipos das funções do CP1.
- `src/modulo.c`: implementa as funcionalidades dos CP2 e CP3.
- `include/modulo.h`: declara a estrutura `Ativo`, as funções do módulo e as constantes do simulador.
- `data/carteira.txt`: armazena os ativos cadastrados.
- `README.md`: apresenta a documentação e as instruções do projeto.

## 5. Requisitos mínimos para execução

Para compilar e executar o programa, são necessários:

- Computador com Windows, Linux ou macOS.
- Compilador GCC instalado.
- Terminal de comandos.
- Arquivos do projeto organizados nas pastas correspondentes.
- Pasta `data` disponível para armazenamento da carteira.

O sistema não necessita de banco de dados ou bibliotecas externas.

## 6. Instruções para execução

### Passo 1 — Abrir o terminal

Acesse a pasta raiz do projeto, onde estão localizados os diretórios `src`, `include` e `data`.

### Passo 2 — Compilar o programa

Execute o seguinte comando:

```bash
gcc -Wall -Wextra -Iinclude src/main.c src/funcoes.c src/modulo.c -o programa
```

### Passo 3 — Executar

No Linux ou macOS:

```bash
./programa
```

No Windows:

```powershell
.\programa.exe
```

### Passo 4 — Utilizar o menu

Após a execução, o sistema apresentará as opções disponíveis.

Caso não existam investimentos cadastrados, selecione a opção `1` para registrar o primeiro ativo.

As demais opções permitem consultar, ordenar, simular e gerar relatórios sobre a carteira.

### Passo 5 — Encerrar

Selecione a opção `0` para salvar os dados e finalizar o programa.

**Importante:** a execução deve ocorrer a partir da pasta raiz do projeto para permitir o acesso correto ao arquivo `data/carteira.txt`.

As taxas utilizadas pelo simulador são definidas por constantes `#define` no arquivo `include/modulo.h`.

## 7. Desenvolvedores

**Integrantes do grupo:**

- Nome — Vitor Muniz de Aguiar
- Nome — Gustavo Mendonça Scharman
- Nome — Luigi Masashi Matsushita
- Nome — Thiago Maiorino Grillo
- Nome — Felipe Mansour Valvassori  
**Disciplina:** Algoritmos e Pensamento Computacional.
**Disciplina Complementar:** Desing Profissional.

---

**Responsabilidade social:** o projeto busca contribuir para a educação e a inclusão financeiras ao explicar conceitos de investimento em linguagem acessível. Essa proposta está relacionada ao **Objetivo de Desenvolvimento Sustentável (ODS 8, meta 8.10, da ONU)**, que aborda a ampliação do acesso aos serviços financeiros.
