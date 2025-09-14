# ScreenMatch Console 🎬

![Java](https://img.shields.io/badge/Java-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white)
![Spring](https://img.shields.io/badge/Spring-6DB33F?style=for-the-badge&logo=spring&logoColor=white)
![Maven](https://img.shields.io/badge/Maven-C71A36?style=for-the-badge&logo=apache-maven&logoColor=white)

## 🚀 Sobre o Projeto

O **ScreenMatch** é uma aplicação de console (terminal) desenvolvida em Java. Sua principal função é buscar e exibir informações sobre séries de TV utilizando a API externa [OMDb API](https.www.omdbapi.com).

Este projeto, inspirado em um popular desafio de aprendizado da Alura, foi desenvolvido para colocar em prática conceitos fundamentais do ecossistema Java, como o consumo de APIs, a desserialização de dados JSON, o uso de `Records`, `Streams` e a estruturação de uma aplicação de forma modular e coesa.

### Funcionalidades
- **Busca de Séries:** Permite ao usuário buscar por uma série pelo título.
- **Listagem de Temporadas:** Exibe todas as temporadas da série encontrada.
- **Listagem de Episódios:** Mostra os detalhes de todos os episódios de uma temporada.
- **Estatísticas:** Apresenta dados estatísticos, como o top 5 melhores episódios da série com base na avaliação.

## 💻 Tecnologias Utilizadas

O projeto foi construído sobre uma base sólida de tecnologias do ecossistema Java, focando em simplicidade e eficiência para uma aplicação de console.

- **Java (JDK 17+):**
  É a linguagem de programação principal do projeto, utilizando recursos modernos como `Records` para a criação de DTOs (Data Transfer Objects) imutáveis e a API de `Streams` para manipulação de coleções de dados.

- **Spring Boot:**
  Embora seja uma aplicação "sem-web", o framework é utilizado para facilitar a configuração e a **injeção de dependências**, tornando o código mais limpo, modular e fácil de manter. Ele gerencia o ciclo de vida dos componentes da aplicação sem a necessidade de um servidor web.

- **Maven:**
  É a ferramenta de automação de build e gerenciamento de dependências. O arquivo `pom.xml` define todas as bibliotecas necessárias, como Jackson e Spring Boot, e automatiza o processo de compilação do projeto.

- **Jackson Databind:**
  Biblioteca fundamental para a **desserialização** dos dados. Ela converte o texto em formato JSON, recebido da OMDb API, em objetos Java, permitindo uma manipulação de dados segura e orientada a objetos.

## 🏗️ Arquitetura e Estrutura

O código foi organizado seguindo princípios de separação de responsabilidades para garantir um software de fácil manutenção e escalabilidade.

- **`main.Principal`:**
  Ponto de entrada da aplicação (`main`). Responsável pelo loop de execução, exibição do menu de opções e por orquestrar as chamadas aos serviços com base na interação do usuário.

- **`service.ConsumoApi`:**
  Classe de serviço dedicada a fazer a chamada HTTP para a OMDb API. Sua única responsabilidade é buscar os dados externos e retorná-los como uma `String` no formato JSON.

- **`service.ConverteDados`:**
  Serviço que atua como um "conversor" genérico. Utiliza a biblioteca Jackson para transformar a `String` JSON obtida pelo `ConsumoApi` em objetos Java (DTOs).

- **`model` (Pacote):**
  Contém as classes ou `Records` que representam os dados da aplicação (`DadosSerie`, `DadosTemporada`, `DadosEpisodio`). Estes são os DTOs que mapeiam diretamente a estrutura da resposta da API.

## ▶️ Como Executar

#### Pré-requisitos
- Java (JDK 17 ou superior)
- Maven
- Uma chave da API OMDb

#### Passos

1. **Clone o repositório:**
   ```bash
   git clone [https://github.com/HenryPedro/screenmatch-sem-web.git](https://github.com/HenryPedro/screenmatch-sem-web.git)
   ```

2. **Navegue até o diretório do projeto:**
   ```bash
   cd screenmatch-sem-web
   ```

3. **Obtenha e configure sua chave da API:**
   - Acesse [OMDb API](http://www.omdbapi.com/apikey.aspx) para gerar sua chave gratuita.
   - Adicione a chave no local indicado no código, provavelmente na classe `ConsumoApi` onde a URL da requisição é construída.

4. **Compile e execute o projeto via Maven:**
   ```bash
   # Compila o projeto e empacota em um arquivo .jar
   mvn clean package

   # Executa o arquivo gerado (verifique a versão no nome do arquivo dentro da pasta /target)
   java -jar target/screenmatch-0.0.1-SNAPSHOT.jar
   ```
---
