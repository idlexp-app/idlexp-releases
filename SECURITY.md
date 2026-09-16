# Segurança do IdleXP

<p>
  <img src="https://img.shields.io/badge/Portugu%C3%AAs-2ea043?style=flat-square" alt="Português">
  <a href="SECURITY.en.md"><img src="https://img.shields.io/badge/English-555?style=flat-square" alt="English"></a>
</p>

## Onde baixar

O único lugar oficial é este repositório:
**https://github.com/idlexp-app/idlexp-releases/releases/latest**

Um IdleXP baixado de outro site, grupo ou mensagem não é nosso. O próprio app só se atualiza a
partir daqui.

Cada versão traz três arquivos, um por sistema: `IdleXP-Setup.exe` (Windows), `IdleXP.dmg` (macOS,
Intel e Apple Silicon no mesmo arquivo) e `IdleXP.AppImage` (Linux 64 bits).

## Como conferir um download

1. **Selo Immutable.** Toda versão publicada é travada pelo GitHub e mostra o cadeado
   **Immutable** na página dela. Depois de publicada, os arquivos não podem ser trocados. Para
   conferir o atestado assinado pelo GitHub, com o [GitHub CLI](https://cli.github.com/):

   ```
   gh release verify-asset v1.2.3 IdleXP-Setup.exe -R idlexp-app/idlexp-releases
   ```

   Troque `v1.2.3` pela versão que você baixou, e o nome do arquivo pelo do seu sistema.

2. **Código de conferência (SHA-256).** As notas de cada versão trazem o código dos três arquivos.
   O comando muda com o sistema:

   | Sistema | Comando |
   | --- | --- |
   | Windows (PowerShell) | `Get-FileHash .\IdleXP-Setup.exe` |
   | macOS | `shasum -a 256 IdleXP.dmg` |
   | Linux | `sha256sum IdleXP.AppImage` |

   Se o resultado for diferente do publicado, não instale e nos avise.

## O aviso do seu sistema

O IdleXP ainda não tem assinatura digital paga, e cada sistema reage a isso de um jeito:

- **Windows.** O SmartScreen mostra "O Windows protegeu o computador" na primeira vez. É o aviso de
  arquivo novo, não de arquivo perigoso. Clique em **Mais informações** e depois em **Executar
  assim mesmo**.
- **macOS.** O Gatekeeper diz que não foi possível verificar o desenvolvedor. Vá em **Ajustes do
  Sistema › Privacidade e Segurança** e clique em **Abrir assim mesmo**. Pela mesma razão, no Mac o
  app **não** instala atualização sozinho: ele avisa que existe e leva você até esta página.
- **Linux.** Não há aviso nenhum, e a atualização é automática.

## O que protege quem usa

- As quatro contas ficam isoladas umas das outras, e os logins só existem no seu computador.
- O app não tem servidor, cadastro nem telemetria. Veja a [nota de privacidade](PRIVACIDADE.md).
- A conexão do modo economia só lê. O programa não sabe enviar nenhuma ação de jogo.
- A atualização só instala o arquivo cujo código de conferência (SHA-512) bate com o publicado
  aqui; se não bater, o app abre na versão que você já tem.
- No Windows, o instalador não pede administrador; no Linux, o AppImage também não. Remover o app
  não apaga os logins em nenhum dos três.

## Relatar um problema de segurança

**Não abra uma issue pública.** Use
[Report a vulnerability](https://github.com/idlexp-app/idlexp-releases/security/advisories/new):
só nós vemos o relato até ele ser resolvido.

Conte a versão do IdleXP, o seu sistema, o que acontece e como reproduzir. Se anexar o
`diagnostico.log` — que fica na pasta de dados do app, descrita na nota de privacidade —, apague
antes os nomes dos seus personagens.
