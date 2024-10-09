# API de Operações

Esta é uma API de operações matemáticas desenvolvida em Java utilizando Spring. Ela fornece uma variedade de operações como cálculo de MDC, sequência de Fibonacci, verificação de números primos, ordenação, somatório, entre outros.

## Como utilizar a API

### Pré-requisitos

- [Java 17+](https://www.oracle.com/java/technologies/javase-jdk17-downloads.html)
- [Maven](https://maven.apache.org/)
- [Spring Boot](https://spring.io/projects/spring-boot)

### Instalação

1. Clone o repositório:
   ```bash
   git clone https://github.com/seu-usuario/operacoes-api.git
   cd operacoes-api

Compile o projeto usando Maven:

bash
Copiar código
mvn clean install
Execute a aplicação:

bash
Copiar código
mvn spring-boot:run
A aplicação estará disponível em http://localhost:8080/api/operacoes.

Endpoints Disponíveis
1. Contagem de Aprovados
Descrição: Calcula quantos alunos foram aprovados com base em suas notas.
URL: /api/operacoes/contagem-aprovados
Método: GET
Parâmetros:
quantidade (int): Número total de alunos.
notas (array de int): Notas dos alunos.
Exemplo de requisição:
bash
Copiar código
GET /api/operacoes/contagem-aprovados?quantidade=5&notas=60,70,80,40,55
Resposta:
json
Copiar código
{
  "message": "Total de alunos: 5, Aprovados: 4"
}
2. Sequência de Fibonacci
Descrição: Retorna a sequência de Fibonacci até o número de termos solicitado.
URL: /api/operacoes/fibonacci
Método: GET
Parâmetros:
termos (int): Número de termos da sequência.
Exemplo de requisição:
bash
Copiar código
GET /api/operacoes/fibonacci?termos=6
Resposta:
json
Copiar código
{
  "message": "0, 1, 1, 2, 3, 5"
}
3. Cálculo do MDC (Máximo Divisor Comum)
Descrição: Calcula o MDC entre dois números.
URL: /api/operacoes/mdc
Método: GET
Parâmetros:
a (int): Primeiro número.
b (int): Segundo número.
Exemplo de requisição:
css
Copiar código
GET /api/operacoes/mdc?a=20&b=30
Resposta:
json
Copiar código
{
  "message": "MDC: 10"
}
4. Verificação de Número Primo
Descrição: Verifica se um número é primo.
URL: /api/operacoes/numero-primo
Método: GET
Parâmetros:
numero (int): Número a ser verificado.
Exemplo de requisição:
bash
Copiar código
GET /api/operacoes/numero-primo?numero=7
Resposta:
json
Copiar código
{
  "message": "7 é primo"
}
5. Ordenação de Vetor
Descrição: Ordena um vetor de inteiros.
URL: /api/operacoes/ordenacao
Método: POST
Corpo da Requisição:
json
Copiar código
{
  "vetor": [5, 3, 8, 4, 1]
}
Exemplo de requisição:
bash
Copiar código
POST /api/operacoes/ordenacao
{
  "vetor": [5, 3, 8, 4, 1]
}
Resposta:
json
Copiar código
{
  "message": "Vetor ordenado: [1, 3, 4, 5, 8]"
}
6. Somatório de Números
Descrição: Soma todos os números de um vetor.
URL: /api/operacoes/somador
Método: POST
Corpo da Requisição:
json
Copiar código
{
  "numeros": [10, 20, 30]
}
Exemplo de requisição:
bash
Copiar código
POST /api/operacoes/somador
{
  "numeros": [10, 20, 30]
}
Resposta:
json
Copiar código
{
  "message": "Soma total: 60"
}
7. Troca de Variáveis
Descrição: Troca os valores de duas variáveis.
URL: /api/operacoes/troca-variaveis
Método: GET
Parâmetros:
a (int): Primeiro valor.
b (int): Segundo valor.
Exemplo de requisição:
css
Copiar código
GET /api/operacoes/troca-variaveis?a=10&b=20
Resposta:
json
Copiar código
{
  "message": "A: 20, B: 10"
}
Tecnologias Utilizadas
Java 17
Spring Boot
Maven
Contribuição
Contribuições são bem-vindas! Sinta-se à vontade para abrir uma issue ou pull request.

Licença
Este projeto está licenciado sob a Licença MIT. Para mais detalhes, veja o arquivo LICENSE.

perl
Copiar código

Você pode copiar e colar esse conteúdo diretamente no seu arquivo `README.md` no GitHub.