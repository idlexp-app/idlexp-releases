# Segurança do IdleXP

## Onde baixar

O único lugar oficial é este repositório:
**https://github.com/idlexp-app/idlexp-releases/releases/latest**

Um IdleXP baixado de outro site, grupo ou mensagem não é nosso. O próprio app só se atualiza a
partir daqui.

## Como conferir um instalador

1. **Selo Immutable.** Toda versão publicada é travada pelo GitHub e mostra o cadeado
   **Immutable** na página dela. Depois de publicada, o instalador não pode ser trocado. Para
   conferir o atestado assinado pelo GitHub, com o [GitHub CLI](https://cli.github.com/):

   ```
   gh release verify-asset v1.2.3 IdleXP-Setup.exe -R idlexp-app/idlexp-releases
   ```

   Troque `v1.2.3` pela versão que você baixou.

2. **Código de conferência (SHA-256).** As notas de cada versão trazem o código do
   `IdleXP-Setup.exe`. No PowerShell:

   ```
   Get-FileHash .\IdleXP-Setup.exe
   ```

   Se o resultado for diferente do publicado, não instale e nos avise.

## O aviso azul do Windows

O instalador ainda não tem assinatura digital paga, então o SmartScreen mostra "O Windows protegeu
o computador" na primeira vez. É o aviso de arquivo novo, não de arquivo perigoso. Clique em
**Mais informações** e depois em **Executar assim mesmo**.

## O que protege quem usa

- As quatro contas ficam isoladas umas das outras, e os logins só existem no seu PC.
- O app não tem servidor, cadastro nem telemetria. Veja a [nota de privacidade](PRIVACIDADE.md).
- A conexão do modo economia só lê. O programa não sabe enviar nenhuma ação de jogo.
- A atualização só instala o arquivo cujo código de conferência (SHA-512) bate com o publicado
  aqui; se não bater, o app abre na versão que você já tem.
- O instalador não pede administrador e desinstalar não apaga os logins.

## Relatar um problema de segurança

**Não abra uma issue pública.** Use
[Report a vulnerability](https://github.com/idlexp-app/idlexp-releases/security/advisories/new):
só nós vemos o relato até ele ser resolvido.

Conte a versão do IdleXP, o que acontece e como reproduzir. Se anexar o
`%APPDATA%\idlexp\diagnostico.log`, apague antes os nomes dos seus personagens.
