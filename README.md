# FragBoost: downloads e atualizações

Este repositório público guarda as versões do **FragBoost** e o arquivo que o app consulta para se atualizar.

## Baixar

**Versão atual (sempre a mais nova):** [FragBoost.exe](https://raw.githubusercontent.com/IsaelTau/FragBoost-releases/main/FragBoost.exe)

Requer Windows 10 ou 11 (64 bits).

## Como a atualização funciona

1. Ao abrir, o app lê o [`latest.json`](latest.json).
2. Se a versão listada for mais nova que a instalada, o app mostra o aviso **"Atualizar agora"**.
3. Antes de instalar, o app confere duas coisas:
   - a **assinatura digital** do `latest.json`, feita com a chave privada do vendedor;
   - o **SHA-256** do `.exe` baixado.

   Se qualquer uma não bater, a atualização é recusada.

## Como publicar uma versão nova

1. Gere o novo `FragBoost.exe`, com o número de versão maior em `FragBoost.csproj`.
2. Substitua o `FragBoost.exe` deste repositório pelo novo. O nome é sempre o mesmo, para os links de download não quebrarem.
3. Abra o **FragBoost-Keygen.exe**, escolha a opção **3) Preparar atualização** e informe:
   - o caminho do `.exe`;
   - a versão;
   - o link `https://raw.githubusercontent.com/IsaelTau/FragBoost-releases/main/FragBoost.exe`;
   - as novidades.
4. Substitua o `latest.json` por esse novo arquivo gerado.
5. Faça o commit dos dois arquivos juntos.

O código-fonte fica no repositório privado `IsaelTau/FragBoost`.

## Kit de divulgação

A pasta [`kit/`](kit) guarda os vídeos e imagens usados pelos afiliados (https://fragboost.com.br/afiliados).
