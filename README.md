# Projeto de Dados

Este projeto foi desenvolvido com o objetivo de consumir dados da API do Spotify, armazená-los em tabelas na nuvem e permitir que usuários utilizem estes dados em análises.

## Descrição

1. **Consumo de Dados**: O Jupyter Notebook que está no repositório utiliza a API do Spotify para coletar dados e transformá-los em arquivos csv.
2. **Armazenamento**: Depois os arquivos csv são armazenados na AWS.
3. **Consulta**: Dentro da AWS os usuários podem utilizar SQL para realizar consultas nas tabelas criadas com os dados do Spotify.

## Configuração do Projeto

### Pré-requisitos

Certifique-se de ter instalado o Python 3.7 ou superior.

### Instalação de Dependências

- **pandas**: Para manipulação e análise de dados.
- **requests**: Para fazer requisições HTTP à API do Spotify.
- **boto3**: SDK da AWS para interagir com serviços como S3 (para armazenamento) e Athena (para consultas SQL).
- **matplotlib**: Para criação de gráficos e visualizações dos dados.

Você pode instalá-las utilizando o pip com o seguinte comando:

```bash
pip install pandas requests boto3 matplotlib

## Execução do Jupyter Notebook

1. Abra o Jupyter Notebook `spotify_data.ipynb`.
2. Execute cada célula sequencialmente para coletar dados do Spotify, transformá-los em CSV e configurar tabelas no AWS Glue e Amazon Athena.

## Consultas SQL no Amazon Athena

Você pode executar consultas SQL nas tabelas criadas no Amazon Athena para obter insights dos dados coletados do Spotify. Abaixo estão alguns exemplos de consultas que você pode executar:

### Consulta 1: Artistas mais Populares

SELECT name, popularity
FROM artists
ORDER BY popularity DESC
LIMIT 10;


### Consulta 2: Gêneros mais Comuns
SELECT genres, COUNT(*) as count
FROM artists
GROUP BY genres
ORDER BY count DESC
LIMIT 10;

### Consulta 3: Álbuns com Mais Faixas
SELECT album_name, total_tracks
FROM albums
ORDER BY total_tracks DESC
LIMIT 10;

### Consulta 4: Faixas mais Populares
SELECT track_name, track_popularity
FROM top_tracks
ORDER BY track_popularity DESC
LIMIT 10;

```
