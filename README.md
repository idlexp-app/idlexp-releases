<p align="center">
  <img src="imagens/goblin.png" width="136" height="128" alt="IdleXP">
</p>

<h1 align="center">IdleXP</h1>

<p align="center">
  <strong>Quatro contas do Huntera numa janela só — e o seu PC quase não sente.</strong>
</p>

<p align="center">
  <a href="https://github.com/idlexp-app/idlexp-releases/releases/latest/download/IdleXP-Setup.exe"><img src="https://img.shields.io/badge/Baixar_para_Windows-IdleXP--Setup.exe-2ea043?style=for-the-badge" alt="Baixar para Windows"></a>
</p>

<p align="center">
  <a href="https://github.com/idlexp-app/idlexp-releases/releases/latest"><img src="https://img.shields.io/github/v/release/idlexp-app/idlexp-releases?label=vers%C3%A3o&color=2ea043" alt="Versão"></a>
  <img src="https://img.shields.io/endpoint?url=https%3A%2F%2Fraw.githubusercontent.com%2Fidlexp-app%2Fidlexp-releases%2Finsignias%2Fdownloads.json" alt="Downloads">
  <img src="https://img.shields.io/badge/Windows-10_e_11-0078d4" alt="Windows 10 e 11">
  <img src="https://img.shields.io/badge/pre%C3%A7o-gr%C3%A1tis-555" alt="Grátis">
</p>

<p align="center">
  Grátis · sem cadastro · se atualiza sozinho
</p>

---

<p align="center">
  <img src="imagens/painel-economia.png" alt="O painel do modo economia: XP por hora, profit, preys e bestiário da caçada">
  <br>
  <sub>O painel do modo economia. Imagem ilustrativa, com dados de exemplo.</sub>
</p>

## Por que o IdleXP

Jogar com vários personagens no navegador é abrir várias abas, relogar toda hora e ver o
computador esquentar. O IdleXP junta as quatro contas numa janela, lembra os quatro logins e,
com o **modo economia**, fecha o navegador das contas que você não está olhando — sem parar
a caçada delas.

### O que muda no seu PC

Com as quatro contas em modo economia, comparado às mesmas quatro contas abertas normalmente:

| | Sem o modo economia | Com o modo economia | |
| --- | --- | --- | --- |
| **Processador** | 310% de um núcleo | 13% de um núcleo | **−96%** |
| **Memória** | 5,4 GB | 1,85 GB | **−66%** |
| **Placa de vídeo** | 6,5% de uso | 0,1% de uso | **−98%** |

E cada conta que sai da tela, sozinha: de **776 MB e 27% de um núcleo** para **64 MB e menos de
0,5%** — continuando a ganhar experiência.

<sub>Medido no PC do desenvolvedor em 04/09/2026: quatro telas, três contas logadas na mesma caçada
e uma deslogada, duas janelas de 60 segundos, a única diferença sendo o modo economia. Os números
do seu PC vão ser outros; a proporção é o que conta.</sub>

## O que ele faz

- **Quatro contas, quatro logins salvos.** Cada conta tem o seu próprio espaço: uma não enxerga a
  outra, e você não precisa entrar de novo toda vez que abre o app.
- **A tela do seu jeito.** De 1 a 4 telas lado a lado, ou uma grande com as outras ao lado.
  Zoom ajustável e tela cheia.
- **Modo economia.** A conta continua caçando, mas sem navegador aberto. No lugar do jogo fica um
  painel com o que importa: vida, mana, stamina, nível, **XP/h**, **Profit/h**, as **preys** ativas
  e o **bestiário** da caçada, com quanto falta para cada fase.
- **Economia automática.** Nos layouts de 1 a 3 telas, as contas que ficam fora da tela entram em
  economia sozinhas depois de 2 minutos.
- **Avisa quando algo dá errado.** Se o personagem morrer ou a stamina acabar, o cartão da conta
  mostra na hora.
- **Esconde os nomes para print e live.** Um clique tarja os nomes dos personagens no app e, dentro
  do jogo, no mapa, na party e no cabeçalho.
- **Se atualiza sozinho.** Ao abrir, o IdleXP confere se há versão nova, baixa e instala antes de
  qualquer conta abrir. Você baixa uma vez só.

> O modo economia acompanha o personagem enquanto ele caça offline (VIP). Ele não mantém uma
> caçada que o jogo não manteria.

## Instalar

1. Clique em **[Baixar para Windows](https://github.com/idlexp-app/idlexp-releases/releases/latest/download/IdleXP-Setup.exe)**.
2. Abra o `IdleXP-Setup.exe`. Na primeira vez o Windows mostra um aviso azul (veja abaixo por quê):
   clique em **Mais informações** e depois em **Executar assim mesmo**.
3. Aceite a licença, escolha a pasta e pronto. No fim dá para abrir o app e criar o atalho.

Requisitos: Windows 10 ou 11, 64 bits. O instalador não pede senha de administrador e instala
só para o seu usuário.

## É seguro?

**Sim — e você não precisa acreditar só na nossa palavra.**

### Por que o Windows mostra um aviso azul

O aviso "O Windows protegeu o computador" aparece para todo programa novo que ainda não tem uma
**assinatura digital paga**. Ele quer dizer "o Windows ainda não conhece este arquivo", e não
"este arquivo é perigoso". Conforme mais pessoas baixam, o aviso tende a sumir.

### Como conferir que o arquivo é o original

- **Selo Immutable.** Cada versão publicada aqui é travada pelo próprio GitHub: depois de
  publicada, ninguém — nem nós — consegue trocar o instalador. Você vê o cadeado **Immutable**
  na página da versão, e o GitHub assina um atestado que qualquer pessoa confere com o
  [GitHub CLI](https://cli.github.com/):
  ```
  gh release verify-asset IdleXP-Setup.exe -R idlexp-app/idlexp-releases
  ```
- **Código de conferência (SHA-256).** As notas de cada versão trazem o código do instalador.
  No PowerShell, na pasta onde você baixou:
  ```
  Get-FileHash .\IdleXP-Setup.exe
  ```
  O resultado tem que ser igual ao das notas. Se for diferente, não instale.
- **O único endereço oficial é este repositório.** O IdleXP baixado de qualquer outro lugar não é
  nosso.

### O que o IdleXP nunca faz

- **Não guarda a sua senha.** Você entra na página do próprio Huntera, dentro do app, como faria no
  navegador. A senha vai para o Huntera.
- **Não manda nada para nós.** Não existe servidor do IdleXP, cadastro, telemetria nem anúncio. O
  app só conversa com o Huntera e com este repositório, para saber se há versão nova.
- **Não joga por você.** O modo economia só **lê** o que acontece com o personagem. O IdleXP não
  sabe mandar nenhuma ação de jogo: essa parte não existe no programa.
- **Não mexe nos seus logins ao desinstalar.** Eles ficam em `%APPDATA%\idlexp`, e reinstalar
  devolve as quatro contas logadas.
- **Não instala atualização sem conferir.** Ela só vem deste repositório, e só é aplicada se o
  código de conferência do arquivo baixado bater com o publicado aqui.

Os detalhes estão na [nota de privacidade](PRIVACIDADE.md) e na [política de segurança](SECURITY.md).

## Dúvidas comuns

**Funciona no Mac?** Ainda não. Por enquanto, só Windows.

**Onde ficam os meus logins?** No seu PC, em `%APPDATA%\idlexp`. Nada sai dali.

**Como desinstalar?** Em Configurações › Aplicativos, procure IdleXP. Os logins ficam guardados
para quando você voltar.

**Achei um problema.** [Abra uma issue](https://github.com/idlexp-app/idlexp-releases/issues/new/choose)
contando a versão e o que aconteceu. Problema de segurança, relate
[em particular](https://github.com/idlexp-app/idlexp-releases/security/advisories/new).

---

<sub>O IdleXP é gratuito e não é afiliado ao Huntera. Uso sujeito à [licença](LICENSE).
Huntera é marca de seus respectivos donos.</sub>
