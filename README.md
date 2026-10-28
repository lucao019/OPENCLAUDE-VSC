# OpenClaude + River AI

Guia rápido, em português, para configurar o OpenClaude com a API do River usando um modelo base — sem criar deployment e sem colocar credenciais dentro do projeto.

> **Importante:** este repositório não precisa de `.env`. Nunca salve ou envie sua chave de API em arquivos do projeto, README, prints, mensagens ou commits.

## O que você precisa

- OpenClaude instalado e aberto no terminal.
- Uma chave de API criada no [Console do River](https://console.river.ai/keys).
- Um modelo disponível na página **Inference → Base models** do River.

O exemplo deste guia usa:

```text
Modelo: deepseek-ai/DeepSeek-V4.1-Flash
URL da API: https://api.river.ai/v1
```

Os modelos e preços podem mudar. Confira as informações atuais no Console do River antes de usar.

## Configuração inicial

1. No OpenClaude, escolha **3rd-party platform**.
2. Selecione **Custom (OpenAI-compatible)** e pressione **Enter**.
3. Dê um nome fácil de reconhecer ao perfil, por exemplo **River**.
4. Preencha a URL base com:

   ```text
   https://api.river.ai/v1
   ```

5. Selecione **Chat Completions** como modo da API. O exemplo oficial do River usa `chat.completions.create`.
6. Quando o OpenClaude solicitar a chave, informe a chave do River diretamente no campo próprio. Não a inclua em comandos, arquivos do projeto ou mensagens.
7. Deixe os campos opcionais **Auth header**, **Auth header value** e **Custom headers** vazios.
8. Conclua a configuração e selecione o perfil **River** como provedor ativo.
9. Selecione ou informe o nome exato do modelo:

   ```text
   deepseek-ai/DeepSeek-V4.1-Flash
   ```

   Não acrescente prefixos de outro provedor, como `llama3.1:8b`.

## Teste rápido

Envie uma mensagem simples, por exemplo:

```text
Responda apenas: conexão funcionando.
```

Confirme no indicador do OpenClaude que o modelo ativo é `deepseek-ai/DeepSeek-V4.1-Flash`. Se aparecer outro nome, abra `/provider` para conferir o provedor ativo e `/model` para selecionar o modelo correto.

## Custos e limites

- As chamadas feitas com a chave do River são cobradas conforme o uso e os preços atuais do modelo.
- O saldo disponível é compartilhado entre as chaves da mesma conta River; criar outra chave não cria outro saldo.
- Confira o consumo e os limites de uso no Console do River. Tarifas e limites podem mudar.
- Se uma tarefa parar no meio, isso não significa necessariamente que o saldo acabou. Verifique a mensagem de erro, a conexão e o painel de uso antes de tentar novamente.

## Proteja sua chave

- Não publique sua chave, mesmo em um repositório privado.
- Não cole a chave em chats, issues, logs ou capturas de tela.
- Não crie nem envie `.env` para este tutorial.
- Se uma chave for exposta, revogue-a no Console do River e gere outra.
