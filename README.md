# Webscrapping das noticias recentes do TabNine

O script pega todas as notícias recentes do site TabNine e envia ao gemini para fazer um resumo.

## Como rodar sem docker

### Pre requisitos

- python >= 3.13
- [uv](https://github.com/astral-sh/uv)
- [gemini api key](https://aistudio.google.com/apikey)

### Instruções

Instale as dependências do projeto.

```bash
uv sync
```

Gere uma api key do gemini [aqui](https://aistudio.google.com/apikey). Após isso renomeie o arquivo `.env.test` para `.env` e adicione sua api `GEMINI_API_KEY=SUA_API_KEY`

Após isso basta rodar o projeto

```bash
uv run main.py
```

## Como rodar com docker

Gere uma api key do gemini [aqui](https://aistudio.google.com/apikey). Após isso renomeie o arquivo `.env.test` para `.env` e adicione sua api `GEMINI_API_KEY=SUA_API_KEY`

Rode os comando

```bash
docker compose up
```

## Considerações finais

O json gerado pela IA vai estar localizado no diretório `/output`.
O projeto não está pronto, pretendo organizar o código e adicionar uma IA de TTS.
