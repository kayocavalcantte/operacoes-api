Aqui está o arquivo README.md formatado para o seu projeto de API:

```md
# Operações API

Esta API foi desenvolvida utilizando Spring Boot para realizar diversas operações matemáticas, incluindo cálculo de números primos, Fibonacci, MDC, ordenação e mais.

## Endpoints

### 1. Contagem de Aprovados
Calcula o número de alunos aprovados com base em suas notas.

**Endpoint:** `GET /api/operacoes/contagem-aprovados`

**Parâmetros:**
- `quantidade` (int): Quantidade total de alunos.
- `notas` (int[]): Array de notas dos alunos.

**Exemplo de Requisição:**
```bash
GET /api/operacoes/contagem-aprovados?quantidade=5&notas=70,40,55,60,50
```

**Exemplo de Resposta:**
```json
"Total de alunos: 5, Aprovados: 4"
```

---

### 2. Sequência de Fibonacci
Gera uma sequência de Fibonacci com base no número de termos fornecido.

**Endpoint:** `GET /api/operacoes/fibonacci`

**Parâmetros:**
- `termos` (int): Número de termos da sequência a serem gerados.

**Exemplo de Requisição:**
```bash
GET /api/operacoes/fibonacci?termos=10
```

**Exemplo de Resposta:**
```json
"0, 1, 1, 2, 3, 5, 8, 13, 21, 34"
```

---

### 3. Cálculo do MDC (Máximo Divisor Comum)
Calcula o MDC de dois números.

**Endpoint:** `GET /api/operacoes/mdc`

**Parâmetros:**
- `a` (int): Primeiro número.
- `b` (int): Segundo número.

**Exemplo de Requisição:**
```bash
GET /api/operacoes/mdc?a=48&b=18
```

**Exemplo de Resposta:**
```json
"MDC: 6"
```

---

### 4. Verificar Número Primo
Verifica se um número é primo.

**Endpoint:** `GET /api/operacoes/numero-primo`

**Parâmetros:**
- `numero` (int): Número a ser verificado.

**Exemplo de Requisição:**
```bash
GET /api/operacoes/numero-primo?numero=7
```

**Exemplo de Resposta:**
```json
"7 é primo"
```

---

### 5. Ordenação de Vetor
Ordena um vetor de números inteiros.

**Endpoint:** `POST /api/operacoes/ordenacao`

**Parâmetros:**
- `vetor` (int[]): Array de números inteiros a serem ordenados.

**Exemplo de Requisição:**
```bash
POST /api/operacoes/ordenacao
Content-Type: application/json
Body: [3, 5, 1, 4, 2]
```

**Exemplo de Resposta:**
```json
"Vetor ordenado: [1, 2, 3, 4, 5]"
```

---

### 6. Soma de Vetor
Calcula a soma de um array de números inteiros.

**Endpoint:** `POST /api/operacoes/somador`

**Parâmetros:**
- `numeros` (int[]): Array de números inteiros.

**Exemplo de Requisição:**
```bash
POST /api/operacoes/somador
Content-Type: application/json
Body: [1, 2, 3, 4, 5]
```

**Exemplo de Resposta:**
```json
"Soma total: 15"
```

---

### 7. Troca de Variáveis
Troca os valores de duas variáveis.

**Endpoint:** `GET /api/operacoes/troca-variaveis`

**Parâmetros:**
- `a` (int): Valor da primeira variável.
- `b` (int): Valor da segunda variável.

**Exemplo de Requisição:**
```bash
GET /api/operacoes/troca-variaveis?a=5&b=10
```

**Exemplo de Resposta:**
```json
"A: 10, B: 5"
```

## Como Executar o Projeto

### Pré-requisitos:
- [Java 11+](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html)
- [Maven](https://maven.apache.org/download.cgi)
- [Spring Boot](https://spring.io/projects/spring-boot)

### Passos para rodar o projeto:

1. Clone o repositório:
   ```bash
   git clone https://github.com/seu-usuario/operacoes-api.git
   ```

2. Entre na pasta do projeto:
   ```bash
   cd operacoes-api
   ```

3. Compile e rode o projeto:
   ```bash
   mvn spring-boot:run
   ```

4. Acesse a API no seguinte endereço:
   ```
   http://localhost:8080/api/operacoes
   ```

## Tecnologias Utilizadas

- **Java 11**
- **Spring Boot**
- **Maven**

## Contribuição

Contribuições são bem-vindas! Para contribuir com o projeto, siga as etapas abaixo:

1. Faça um fork do projeto.
2. Crie uma nova branch (`git checkout -b feature/nova-funcionalidade`).
3. Commit suas mudanças (`git commit -m 'Adiciona nova funcionalidade'`).
4. Envie para o repositório remoto (`git push origin feature/nova-funcionalidade`).
5. Abra um Pull Request.

## Licença

Este projeto está licenciado sob a Licença MIT. Veja o arquivo [LICENSE](LICENSE) para mais detalhes.
```

Esse README inclui descrições dos endpoints da API, instruções sobre como rodar o projeto e informações sobre contribuição. Ajuste o conteúdo conforme necessário, como o URL do repositório GitHub, se houver.