# Carteira de Investimentos — CP2

## 1. Descrição do projeto

O projeto **Carteira de Investimentos** foi desenvolvido em linguagem C, com o objetivo de criar um sistema simples para cadastrar e acompanhar investimentos financeiros.

O programa permite registrar ativos, calcular a rentabilidade, verificar lucros ou prejuízos e consultar o valor total da carteira.

Nesta segunda etapa (CP2), foram utilizadas estruturas (`struct`), vetores, funções e manipulação de arquivos para organizar e armazenar as informações dos investimentos.

O sistema possui finalidade educativa e não realiza operações financeiras reais.

## 2. Público-alvo

O sistema é destinado a:

- Pessoas interessadas em compreender conceitos básicos de investimentos.
- Usuários que procuram uma ferramenta simples para simular uma carteira de investimentos.
- Iniciantes que desejam entender cálculos de rentabilidade, lucro e prejuízo.

## 3. Funcionalidades do sistema

O programa apresenta um menu interativo com as seguintes funcionalidades:

### 1. Cadastrar ativo
Permite cadastrar um investimento informando:
- Nome do ativo.
- Categoria do investimento.
- Quantidade adquirida.
- Preço de compra.
- Preço atual.

### 2. Listar ativos
Exibe todos os investimentos cadastrados, apresentando suas informações e rentabilidade individual.

### 3. Valor total da carteira
Calcula e apresenta o valor atual total dos investimentos cadastrados.

### 4. Rentabilidade geral
Apresenta:
- Valor total investido.
- Valor atual da carteira.
- Rentabilidade percentual.
- Lucro ou prejuízo total.
- Classificação didática do resultado.

### 5. Sair
Encerra o programa, salvando os dados cadastrados.

### Funcionalidades adicionais

- Armazenamento de até 100 ativos.
- Utilização de estruturas (`struct`) e vetores.
- Validação dos dados informados.
- Salvamento automático dos investimentos.
- Carregamento dos dados ao iniciar o sistema.
- Organização do código em diferentes arquivos e funções.

## 4. Tecnologias utilizadas no desenvolvimento

As tecnologias e recursos utilizados foram:

- **Linguagem C (C99):** desenvolvimento do sistema.
- **GCC:** compilação do código-fonte.
- **Bibliotecas padrão da linguagem C:** entrada, saída e manipulação de dados.
- **Structs:** organização das informações dos ativos.
- **Vetores:** armazenamento dos investimentos.
- **Funções:** modularização das funcionalidades.
- **Arquivos TXT:** armazenamento permanente dos dados.
- **Terminal/CMD:** interface de interação com o usuário.

## 5. Requisitos mínimos para execução

Para executar o sistema, são necessários:

- Computador com Windows, Linux ou macOS.
- Compilador compatível com C99, como GCC.
- Terminal ou Prompt de Comando.
- Permissão de leitura e escrita na pasta do projeto.

O sistema não exige conexão com a internet nem banco de dados.

## 6. Instruções para execução

### Passo 1 — Baixar o projeto

Baixe ou clone o repositório do GitHub e abra a pasta principal do projeto.

### Passo 2 — Acessar a pasta do projeto

Abra o terminal ou CMD dentro da pasta `meu-projeto-c`.

### Passo 3 — Compilar o programa

No Windows, utilizando o GCC, execute:

```bash
gcc -std=c99 -Iinclude src/main.c src/funcoes.c src/modulo.c -o carteira.exe
```

No Linux ou macOS:

```bash
gcc -std=c99 -Iinclude src/main.c src/funcoes.c src/modulo.c -o carteira
```

### Passo 4 — Executar o programa

No Windows:

```bash
.\carteira.exe
```

No Linux ou macOS:

```bash
./carteira
```

### Passo 5 — Utilizar o sistema

Após iniciar o programa, será apresentado o menu:

```text
===== CARTEIRA DE INVESTIMENTOS =====

1 - Cadastrar ativo
2 - Listar ativos
3 - Valor total da carteira
4 - Rentabilidade geral
5 - Sair
```

Selecione a opção desejada e siga as instruções exibidas na tela.

Os investimentos são armazenados no arquivo `data/carteira.txt`.

**Observação:** execute o programa a partir da pasta principal do projeto para garantir que o arquivo de dados seja localizado corretamente.

### Estrutura do projeto

```text
meu-projeto-c/
│
├── README.md
│
├── data/
│   └── carteira.txt
│
├── include/
│   ├── funcoes.h
│   └── modulo.h
│
└── src/
    ├── main.c
    ├── funcoes.c
    └── modulo.c
```

### Descrição dos arquivos

- **main.c:** contém o menu principal e controla a execução do sistema.
- **funcoes.c:** implementa as funções de cadastro, validação e cálculos.
- **funcoes.h:** declara as funções utilizadas pelo programa.
- **modulo.c:** gerencia os ativos e realiza a leitura e gravação dos dados.
- **modulo.h:** define a estrutura dos ativos e declara as funções do módulo.
- **carteira.txt:** armazena as informações dos investimentos cadastrados.

## 7. Desenvolvedores

Projeto desenvolvido por:

- **[Gustavo Mendonça Scharman]**
- **[Felipe Mansour Valvassori]**
- **[Vitor Muniz de Aguiar]**
- **[Luigi Masashi Matsushita]**
- **[Thiago Maiorino Grillo]**

**Disciplina:** Algoritmos e Pensamento Computacional

**Projeto:** Carteira de Investimentos (CP2)

**Linguagem utilizada:** C99

**Ano:** 2026
