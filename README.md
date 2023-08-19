# 📚 Busca Semântica de Jurisprudências

Este repositório contém o código necessário para a criação das collections de acordo com o modelo de linguagem utilizado (LLM) e realiza a busca de jurisprudências no banco vetorizado Qdrant. Os dados de jurisprudências são processados previamente no repositório [jonas-elias/jurisprudencia-sc-processamento](https://github.com/jonas-elias/jurisprudencia-sc-processamento).

## 📋 Requisitos

- No arquivo "requirements.txt" estão listadas as dependências necessárias para a busca semântica das jurisprudências.
- É necessário utilizar o banco de dados vetorial <strong>Qdrant</strong> para armazenar e recuperar as informações requeridas.
```
docker pull qdrant/qdrant
docker run -p 6333:6333 qdrant/qdrant
```

## 📂 Criação da Collection

A criação da collection envolve armazenar os vetores com os pesos semânticos, juntamente com os dados de referência, no banco de dados vetorial Qdrant. Essa etapa é essencial para viabilizar a busca semântica posterior.

## 🔍 Busca Semântica

A busca semântica é realizada por meio do LLM, que recebe a pergunta/termo e gera o embedding específico. Esse embedding possibilita a busca a partir de um vetor enviado ao banco de dados vetorial Qdrant, permitindo assim uma busca contextualizada das jurisprudências.
