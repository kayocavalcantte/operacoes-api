# Operações API

Esta API foi desenvolvida em Java utilizando o framework Spring Boot. Ela fornece uma variedade de operações matemáticas e lógicas acessíveis por meio de endpoints HTTP. Este documento irá guiá-lo através do processo de configuração, uso e exemplos de chamadas para cada operação.

## Índice

- [Visão Geral](#visão-geral)
- [Tecnologias Utilizadas](#tecnologias-utilizadas)
- [Endpoints](#endpoints)
  - [1. Contagem de Aprovados](#1-contagem-de-aprovados)
  - [2. Sequência de Fibonacci](#2-sequência-de-fibonacci)
  - [3. Máximo Divisor Comum (MDC)](#3-máximo-divisor-comum-mdc)
  - [4. Verificação de Número Primo](#4-verificação-de-número-primo)
  - [5. Ordenação de Vetor](#5-ordenção-de-vetor)
  - [6. Somador](#6-somador)
  - [7. Troca de Variáveis](#7-troca-de-variáveis)
- [Configuração](#configuração)
- [Executando a Aplicação](#executando-a-aplicação)
- [Testando a API](#testando-a-api)
- [Contribuição](#contribuição)
- [Licença](#licença)

## Visão Geral

A Operações API fornece operações matemáticas comuns e lógicas, como contagem de aprovados, cálculo do máximo divisor comum (MDC), verificação de números primos, geração da sequência de Fibonacci, ordenação de arrays e somatórios. Esses serviços podem ser usados em aplicativos web e móveis, facilitando cálculos comuns de maneira rápida e eficiente.

## Tecnologias Utilizadas

- **Java**: Linguagem de programação utilizada para desenvolver a API.
- **Spring Boot**: Framework utilizado para simplificar a configuração e o desenvolvimento da aplicação.
- **Maven**: Ferramenta de gerenciamento de dependências e build.

## Endpoints

### 1. Contagem de Aprovados

- **Método:** `GET`
- **URL:** `/api/operacoes/contagem-aprovados`
- **Parâmetros:**
  - `quantidade` (int): Total de alunos.
  - `notas` (int[]): Array com as notas dos alunos.
  
- **Descrição:** Este endpoint conta quantos alunos foram aprovados com notas iguais ou superiores a 50.
  
- **Exemplo de uso:**
  ```http
  GET /api/operacoes/contagem-aprovados?quantidade=5&notas=60,40,80,30,90
  ```

- **Resposta:**
  ```json
  {
      "mensagem": "Total de alunos: 5, Aprovados: 3"
  }
  ```


### 2. Sequência de Fibonacci

- **Método:** `GET`
- **URL:** `/api/operacoes/fibonacci`
- **Parâmetros:**
  - `termos` (int): Número de termos da sequência a serem gerados.
  
- **Descrição:** Gera a sequência de Fibonacci até o número especificado de termos.
  
- **Exemplo de uso:**
  ```http
  GET /api/operacoes/fibonacci?termos=5
  ```

- **Resposta:**
  ```json
  {
      "resultado": "0, 1, 1, 2, 3"
  }
  ```

---

### 3. Máximo Divisor Comum (MDC)

- **Método:** `GET`
- **URL:** `/api/operacoes/mdc`
- **Parâmetros:**
  - `a` (int): Primeiro número.
  - `b` (int): Segundo número.
  
- **Descrição:** Calcula o máximo divisor comum entre dois números.
  
- **Exemplo de uso:**
  ```http
  GET /api/operacoes/mdc?a=48&b=18
  ```

- **Resposta:**
  ```json
  {
      "resultado": "MDC: 6"
  }
  ```

---

### 4. Verificação de Número Primo

- **Método:** `GET`
- **URL:** `/api/operacoes/numero-primo`
- **Parâmetros:**
  - `numero` (int): Número a ser verificado.
  
- **Descrição:** Verifica se um número é primo ou não.
  
- **Exemplo de uso:**
  ```http
  GET /api/operacoes/numero-primo?numero=7
  ```

- **Resposta:**
  ```json
  {
      "resultado": "7 é primo"
  }
  ```

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
  
- **Descrição:** Ordena um vetor de números em ordem crescente.
  
- **Exemplo de uso:**
  ```http
  POST /api/operacoes/ordenacao
  ```

- **Resposta:**
  ```json
  {
      "resultado": "Vetor ordenado: [1, 3, 5, 8]"
  }
  ```

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

- **Descrição:** Calcula a soma de um array de números.
  
- **Exemplo de uso:**
  ```http
  POST /api/operacoes/somador
  ```

- **Resposta:**
  ```json
  {
      "resultado": "Soma total: 10"
  }
  ```

---

### 7. Troca de Variáveis

- **Método:** `GET`
- **URL:** `/api/operacoes/troca-variaveis`
- **Parâmetros:**
  - `a` (int): Primeiro número.
  - `b` (int): Segundo número.
  
- **Descrição:** Troca os valores de duas variáveis e retorna o resultado.
  
- **Exemplo de uso:**
  ```http
  GET /api/operacoes/troca-variaveis?a=5&b=10
  ```

- **Resposta:**
  ```json
  {
      "resultado": "A: 10, B: 5"
  }
  ```

---

## Configuração

Para rodar a API, você precisa ter o [Java JDK 17](https://www.oracle.com/java/technologies/javase/jdk17-archive-downloads.html) e o [Maven](https://maven.apache.org/download.cgi) instalados em sua máquina.

### Dependências do Projeto

O projeto utiliza as seguintes dependências no `pom.xml`:

```xml
<dependencies>
    <dependency>
        <groupId>org.springframework.boot</groupId>
        <artifactId>spring-boot-starter-data-jpa</artifactId>
    </dependency>
    <dependency>
        <groupId>org.springframework.boot</groupId>
        <artifactId>spring-boot-starter-web</artifactId>
    </dependency>
    <dependency>
        <groupId>org.springframework.boot</groupId>
        <artifactId>spring-boot-devtools</artifactId>
        <scope>runtime</scope>
        <optional>true</optional>
    </dependency>
    <dependency>
        <groupId>com.h2database</groupId>
        <artifactId>h2</artifactId>
        <scope>runtime</scope>
    </dependency>
    <dependency>
        <groupId>org.projectlombok</groupId>
        <artifactId>lombok</artifactId>
        <optional>true</optional>
    </dependency>
    <dependency>
        <groupId>org.springframework.boot</groupId>
        <artifactId>spring-boot-starter-test</artifactId>
        <scope>test</scope>
    </dependency>
</dependencies>
```

## Executando a Aplicação

1. Clone este repositório:
   ```bash
   git clone https://github.com/kayocavalcantte/operacoes-api.git
   ```

2. Navegue até a pasta do projeto:
   ```bash
   cd operacoes-api
   ```

3. Execute o comando Maven para iniciar a aplicação:
   ```bash
   mvn spring-boot:run
   ```

A aplicação estará disponível em `http://localhost:8080`.

## Testando a API

Você pode testar a API usando ferramentas como [Postman](https://www.postman.com/) ou [cURL](https://curl.se/). Aqui estão alguns exemplos de como fazer isso:

### Usando cURL

- **Contagem de Aprovados:**
  ```bash
  curl "http://localhost:8080/api/operacoes/contagem-aprovados?quantidade=5&notas=60,40,80,30,90"
  ```

- **Sequência de Fibonacci:**
  ```bash
  curl "http://localhost:808