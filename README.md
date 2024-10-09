# Operações API

Esta API foi desenvolvida em Java utilizando o framework Spring. Ela fornece diversas operações matemáticas e lógicas, que podem ser acessadas via endpoints HTTP.

## Endpoints

### 1. Contagem de Aprovados

- **Método:** `GET`
- **URL:** `/api/operacoes/contagem-aprovados`
- **Parâmetros:**
  - `quantidade` (int): Total de alunos.
  - `notas` (int[]): Array com as notas dos alunos.
- **Exemplo de uso:**
  ```
  GET /api/operacoes/contagem-aprovados?quantidade=5&notas=60,40,80,30,90
  ```
- **Resposta:** `Total de alunos: 5, Aprovados: 3`


### 2. Sequência de Fibonacci

- **Método:** `GET`
- **URL:** `/api/operacoes/fibonacci`
- **Parâmetros:**
  - `termos` (int): Número de termos da sequência a serem gerados.
- **Exemplo de uso:**
  ```
  GET /api/operacoes/fibonacci?termos=5
  ```
- **Resposta:** `0, 1, 1, 2, 3`

---

### 3. Máximo Divisor Comum (MDC)

- **Método:** `GET`
- **URL:** `/api/operacoes/mdc`
- **Parâmetros:**
  - `a` (int): Primeiro número.
  - `b` (int): Segundo número.
- **Exemplo de uso:**
  ```
  GET /api/operacoes/mdc?a=48&b=18
  ```
- **Resposta:** `MDC: 6`

---

### 4. Verificação de Número Primo

- **Método:** `GET`
- **URL:** `/api/operacoes/numero-primo`
- **Parâmetros:**
  - `numero` (int): Número a ser verificado.
- **Exemplo de uso:**
  ```
  GET /api/operacoes/numero-primo?numero=7
  ```
- **Resposta:** `7 é primo`

---

### 5. Ordenação de Vetor

- **Método:** `POST`
- **URL:** `/api/operacoes/ordenacao`
- **Corpo da Requisição:**
  ```json
  {
      "vetor": [5, 3, 8, 1]
  }
  ```
- **Exemplo de uso:**
  ```
  POST /api/operacoes/ordenacao
  ```
- **Resposta:** `Vetor ordenado: [1, 3, 5, 8]`

---

### 6. Somador

- **Método:** `POST`
- **URL:** `/api/operacoes/somador`
- **Corpo da Requisição:**
  ```json
  {
      "numeros": [1, 2, 3, 4]
  }
  ```
- **Exemplo de uso:**
  ```
  POST /api/operacoes/somador
  ```
- **Resposta:** `Soma total: 10`

---

### 7. Troca de Variáveis

- **Método:** `GET`
- **URL:** `/api/operacoes/troca-variaveis`
- **Parâmetros:**
  - `a` (int): Primeiro número.
  - `b` (int): Segundo número.
- **Exemplo de uso:**
  ```
  GET /api/operacoes/troca-variaveis?a=5&b=10
  ```
- **Resposta:** `A: 10, B: 5`

---

## Configuração

Para rodar a API, você precisa ter o [Java JDK](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) e o [Maven](https://maven.apache.org/download.cgi) instalados em sua máquina. 

### Executando a Aplicação

1. Clone este repositório:
   ```bash
   git clone <URL-do-repositório>
   ```

2. Navegue até a pasta do projeto:
   ```bash
   cd operacoes_api
   ```

3. Execute o comando Maven para iniciar a aplicação:
   ```bash
   mvn spring-boot:run
   ```

A aplicação estará disponível em `http://localhost:8080`.

## Contribuição

Sinta-se à vontade para contribuir com melhorias ou correções. Para isso, faça um fork do repositório e envie um pull request.

## Licença

Este projeto está licenciado sob a [MIT License](LICENSE).
```

Sinta-se à vontade para personalizar o README conforme necessário! Se precisar de mais informações ou ajustes, é só avisar.