# Nota de privacidade do IdleXP

Última atualização: 14/09/2026.

**O IdleXP não tem servidor, não tem conta e não envia nada para nós.** Tudo o
que ele guarda fica no seu computador, e a única coisa com que ele conversa é o
próprio Huntera — o mesmo site que você abriria no navegador.

Não existe cadastro, login no IdleXP, telemetria, analytics, anúncio nem
rastreador. Não existe do nosso lado nenhum banco de dados com você dentro,
porque não existe nenhum servidor nosso.

## O que o app guarda, e onde

Tudo o que é seu fica numa pasta só, no seu PC: `%APPDATA%\idlexp`. Dentro dela:

| Pasta ou arquivo | O que é |
| --- | --- |
| `Partitions\idlexp-account-{1..4}` | Os quatro logins do jogo — cookies e armazenamento que **o próprio site do Huntera** grava. O IdleXP não lê essas credenciais: ele só mantém as quatro separadas, para que uma conta não enxergue a outra |
| `settings.json` | Suas preferências de tela, e só isso: o zoom, quantas telas, o arranjo (grade ou principal), quais contas estão em economia e se o olho dos nomes está ligado |
| `sprites\` | Cache das imagens de monstro que o painel de economia mostra, baixadas do próprio Huntera |
| `diagnostico.log` | Registro técnico do que o app fez, para investigar um problema. Veja a seção abaixo |
| `Cache`, `GPUCache`, `Local Storage` e as outras pastas soltas | O que o navegador embutido grava por conta própria para a janela do app: cache de arquivos baixados e de desenho, e as preferências dele. Os logins do jogo não ficam nelas — ficam em `Partitions` |

Instalado, o IdleXP ocupa mais duas pastas, e nenhuma delas guarda nada seu:
`%LOCALAPPDATA%\Programs\IdleXP`, que é o próprio programa, e
`%LOCALAPPDATA%\idlexp-updater`, onde fica uma cópia do instalador que a
atualização usa para baixar só o que mudou.

Não guardamos senha, e-mail, forma de pagamento nem nada parecido — o IdleXP
nunca pede essas coisas. Sua senha do jogo você digita na página do Huntera
dentro do app, exatamente como faria no navegador, e ela vai para o Huntera.

## Com quem o app conversa

- **`huntera.com.br`** — a página do jogo, a conexão de leitura que acompanha
  o personagem em modo economia, e as imagens que o painel mostra.
- **O provedor de login que o próprio Huntera usar**, se o jogo mandar você a
  um serviço externo para entrar. Quem escolhe esse serviço é o jogo, não nós.
- **O GitHub, para perguntar se existe versão nova.** Acontece toda vez que o
  app abre, e só nessa hora. Esse pedido carrega o que qualquer download
  carrega — o endereço IP do seu acesso e qual versão foi pedida — e, quando há
  versão nova, também qual versão você tem instalada, para baixar só o que
  mudou. Quem eventualmente registra isso é o GitHub, nos termos dele. Nada
  disso chega até nós, e o app não manda junto nenhuma informação sua, do seu
  PC ou das suas contas — nem um número que identifique a sua instalação.

Nenhum outro endereço. O app não busca fonte, ícone, script nem propaganda de
lugar nenhum: a interface inteira é empacotada dentro do executável.

## Sobre o `diagnostico.log`

É o arquivo que a gente pede quando você relata um problema, e ele merece ser
descrito por inteiro:

- É escrito **sempre**, não só quando algo dá errado.
- Tem teto de 2 MB. Passou disso, o antigo vira `diagnostico.log.1` e o app
  recomeça — ele não cresce sem parar.
- Guarda o que o app fez: contas abrindo, entrando e saindo de economia, erros
  de conexão e mensagens de erro que o Huntera devolveu.
- **Não guarda** o corpo das respostas do jogo, nem senha, nem cookie, nem
  nada que sirva para entrar na sua conta.
- **Guarda o nome dos seus personagens.** Isso é de propósito: sem saber de
  qual conta é a linha, o arquivo não serve para investigar nada. Repare que o
  olho que esconde os nomes cobre a tela e o jogo, mas **não** cobre este
  arquivo — ele é para o suporte, não para a transmissão.
- **Ele nunca é enviado a lugar nenhum.** Fica no seu PC. Se você quiser que a
  gente veja, é você que anexa.

## O nome do personagem

O nome que aparece em cada cartão é lido do jogo, ao vivo. Ele não é escolhido
por você, não fica guardado em arquivo nenhum além do `diagnostico.log` (veja
acima) e some da tela junto com a sessão — é assim que o app sabe quais contas
estão no ar. O olho na barra tarja esse nome nos
quatro cartões, nos painéis de economia e também dentro da página do jogo, para
quem vai printar ou transmitir.

## Como apagar tudo

Feche o IdleXP e apague a pasta `%APPDATA%\idlexp`. Isso remove os logins, as
preferências, o cache e o log de uma vez — **e desloga as quatro contas.**
Desinstalar o app não apaga essa pasta, de propósito: quem desinstala para
reinstalar não deveria ter que logar quatro vezes de novo.

Desinstalar remove o programa (`%LOCALAPPDATA%\Programs\IdleXP`). A pasta
`%LOCALAPPDATA%\idlexp-updater` fica, e pode ser apagada à mão a qualquer
momento: na próxima atualização o app baixa o instalador inteiro.

No macOS a pasta equivalente é `~/Library/Application Support/idlexp`.

## LGPD

Não fazemos tratamento de dados pessoais seus, porque nada sai do seu
computador em direção a nós. O que o Huntera coleta enquanto você joga é
assunto entre você e o Huntera, e vale a política de privacidade deles.

O IdleXP não é afiliado ao Huntera — veja o `LICENSE`.

## Se esta nota mudar

Uma versão futura do app pode vir com uma nota diferente. A data no topo diz
qual é a atual, e a versão publicada junto de cada release é a que vale para
ela.

## Contato

Dúvidas sobre esta nota vão para as issues do repositório oficial do IdleXP:
https://github.com/idlexp-app/idlexp-releases/issues. Elas são públicas: não
escreva ali senha, e-mail nem o nome dos seus personagens. Um problema de
segurança se relata em particular, pela aba Security do mesmo repositório.
