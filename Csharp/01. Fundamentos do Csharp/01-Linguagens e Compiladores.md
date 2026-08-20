**Linguagem Compilada**:
- Consiste em receber um arquivo de texto e convertê-lo para binário.
- Otimizado para leitura de humanos

**Linguagem Interpretada**:
- Lidos e interpretados por um intérprete
- Feito em tempo de execução
- Exemplo: JavaScript

Tempo de Execução é o que acontece durante a execução do código pelo computador ou interpretador.

### Compilado vs Interpretado

**Linguagens Interpretadas**:

**Prós:**
- Não precisa ser compilada
- Correções mais fáceis de serem executadas
- Mais simples de serem distribuídas

**Contras**:
- Detecção de erros
	- Somente em tempo de execução
- Tamanho final da aplicação maior
- Menor otimização da execução
- Múltiplos arquivos

**Linguagens Compiladas**:

**Prós**:
- Tempo de Compilação
	- Detecção mais rápida de erros
- Tamanho menor das aplicações
- Maior otimização da execução
- Apenas um arquivo final

**Contras**:
- Precisa de um compilador
- Pode ser mais burocrática

# Tipagem de Dados

**Definições**:
- Também chamadas de fortemente tipadas
- Obrigam a especificar o tipo de dado da informação
- Menor liberdade
- Maior otimização

Um tipo de dado define o formato dele, onde definimos por exemplo que aquela informação é um número, uma letra, uma cadeia de caracteres assim por diante.

- Definir tipos é padronizar os dados
	- Para nós e para o processador/memória
- O let utiliza sempre o mesmo tamanho de alocação
- Tipando temos uma otimização

```
int => 32-bit
float => 32 bit
double => 64 bit
decimal => 128 bit
```