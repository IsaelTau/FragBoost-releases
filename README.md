# FragBoost: downloads e atualizações

Este repositório público guarda as versões do **FragBoost** e o arquivo que o app consulta para se atualizar.

## Baixar

**Versão atual:** [FragBoost-2.1.3.exe](https://raw.githubusercontent.com/IsaelTau/FragBoost-releases/main/FragBoost-2.1.3.exe)

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
2. Copie o arquivo para este repositório como `FragBoost-X.Y.Z.exe`.
3. Abra o **FragBoost-Keygen.exe**, escolha a opção **3) Preparar atualização** e informe:
   - o caminho do `.exe`;
   - a versão;
   - o link `https://raw.githubusercontent.com/IsaelTau/FragBoost-releases/main/FragBoost-X.Y.Z.exe`;
   - as novidades.
4. Substitua o `latest.json` por esse novo arquivo gerado.
5. Apague o `.exe` da versão anterior, para o repositório não crescer à toa, e faça o commit.

O código-fonte fica no repositório privado `IsaelTau/FragBoost`.
