# FullPlay para Android TV

Leitor de sinalética para Android TV, Google TV e boxes Android ligadas por HDMI. Reproduz vídeos e imagens em playlist, em ecrã inteiro ou num layout com relógio, data, tempo, notícias RSS e logótipo. Controla-se pelo comando, pelo telemóvel ou por um backoffice no browser, e por OSC.

## Instalar

1. Na TV, instale a app gratuita **Downloader** e abra o link do APK da versão mais recente (ver [Releases](https://github.com/eventuais-software/fullplay/releases)). Ou copie o APK para uma PEN USB e abra-o num gestor de ficheiros. Da primeira vez, o Android pede para autorizar "instalar apps desconhecidas".
2. Abra a FullPlay. Na primeira vez, autorize o acesso a fotos e vídeos, para poder ler a TV e as PEN USB.
3. No menu (botão OK do comando) › **Ligar o telemóvel** aparece o endereço, por exemplo `http://192.168.1.40:8080`, e um QR code.

## Comando da TV

| Tecla | Menu fechado | Menu aberto |
|---|---|---|
| OK, Menu, Voltar, cima/baixo | Abre o menu | Navegar e escolher |
| Esquerda / direita | Item anterior / seguinte | Navegar |
| Play/Pausa | Pausa ou continua | Reproduz a seleção |
| Stop | Ecrã negro | — |
| Voltar | — | Sobe uma pasta ou fecha o menu |

## Menu na TV

- **Reproduzir já:** ficheiros da Biblioteca, desta TV, de uma PEN USB ou endereços de rede. OK marca as fotos e vídeos; "Reproduzir já" põe-nos no ar; "Guardar como playlist" grava a seleção.
- **Fontes programadas:** playlists já feitas, a um clique. Ficam no ar até ao próximo bloco da agenda, ou até alguém mudar.
- **Definições:** modo de saída (Full screen ou Layout), **Arrancar com a TV**, **Abrir logo em ecrã inteiro**, **PIN do controlo móvel**, rotação, ajuste da imagem, volume, nome do ecrã, porta OSC.
- **Mira de testes** e **Ligar o telemóvel**.
- **Licença e versão:** estado da licença, ID desta TV, ativar uma licença a partir de uma PEN USB e atualizar a app.

### Arrancar com a TV

Com esta opção ligada, a FullPlay abre quando a TV liga. Em Android 10 ou mais recente, o sistema só deixa a app abrir sozinha se tiver a autorização **"Mostrar sobre outras apps"**: o menu mostra o botão laranja **Autorizar abrir sozinha ao ligar**, que abre essa definição; ative a FullPlay na lista.

### PIN do controlo móvel

4 a 8 algarismos. Sem PIN, qualquer aparelho na rede comanda a TV. Com PIN, telemóveis e computadores podem ver o estado, mas só comandam depois de o introduzir. A própria TV nunca pede PIN.

## Telemóvel e backoffice

O mesmo endereço serve as duas coisas: num telemóvel abre o Mobile Control; num computador abre o backoffice (biblioteca, playlists, agenda, layout, ecrã e rede, OSC, licença e versão).

## Agenda e horário de funcionamento

- **Horário de funcionamento:** fora do horário, o ecrã fica negro.
- **Blocos:** cada bloco põe uma playlist ou endereço no ar num intervalo (dias da semana, ou uma data específica, que tem prioridade). Um bloco pode passar a meia-noite (ex.: 21:00–02:00).
- O que se escolhe à mão fica no ar até ao próximo bloco (ou até alguém mudar, se escolher essa opção). "Voltar à agenda" repõe o que a agenda manda.

## Mira de testes

A mesma do StageFlow e do VYTRIX Live: quadrados e círculos perfeitos (se ficarem ovais, a proporção está errada), diagonais, cruz, régua a cada 20/100 px, margens de segurança a 5% e 10%, barras de cor, cinzentos e uma linha dourada a 45° que atravessa o ecrã em 10 s (se parar, a imagem congelou). Ao centro: logótipo, nome do ecrã, link do servidor, resolução e hora. Respeita a rotação.

## OSC (UDP, porta 9000)

`/fullplay/play`, `/pause`, `/toggle`, `/next`, `/prev`, `/stop`, `/item <n>`, `/playlist <nome ou id>`, `/fullscreen <0|1>`, `/layout`, `/teste [0|1]`, `/black [0|1]`, `/volume <0–1>`, `/rotate <0|90|180|270>`, `/agenda`. Feedback opcional: `/fullplay/item`, `/fullplay/remaining`, `/fullplay/teste`, `/fullplay/black`.

## Licença

Sem licença, a FullPlay funciona em **modo demonstração**: tudo funciona, mas aparece a marca de água "FullPlay · modo demonstração" por cima da imagem. Uma licença que expire com a app aberta continua ativa até a app ser reaberta, para nunca parar um evento.

**Pedir uma licença:** no menu da TV › **Licença e versão** (ou no backoffice/telemóvel, na mesma secção) aparece o **ID desta TV**, no formato `XXXX-XXXX-XXXX-XXXX`. Envie esse ID à Eventuais; a licença fica presa a esta TV.

**Ativar:**
- No backoffice (computador) › **Licença e versão**, cole o código `FP1.…` e carregue em **Ativar licença**, ou escolha o ficheiro `.fplicense`. No telemóvel, separador **Ecrã** › Licença.
- Ou copie o ficheiro `.fplicense` para a raiz ou para a pasta Download de uma PEN USB, ligue-a à TV e, no menu da TV › **Licença e versão**, escolha o ficheiro e carregue em OK. Nota: em Android 11 ou mais recente (a maioria das Google TV atuais) o sistema não deixa as apps verem ficheiros que não sejam fotos ou vídeos, por isso a lista pode aparecer vazia; nesse caso use o backoffice ou o telemóvel (a TV mostra um QR para lá chegar).

A licença confirma-se sem Internet. Se a data da TV estiver atrasada, a licença não é aceite: acerte a data e a hora da TV.

## Atualizações

A FullPlay verifica sozinha se há uma versão nova ao arrancar e de 6 em 6 horas (precisa de Internet). Quando há, o backoffice mostra o aviso **Nova versão disponível**.

Para atualizar: **Licença e versão** › **Atualizar** (no backoffice, no telemóvel ou no menu da TV). A TV descarrega a versão nova e mostra o instalador do Android: **é sempre preciso carregar em OK no comando da TV** para confirmar (regra do Android). Durante a instalação, o que está no ar pára.

Depois de instalada, a FullPlay volta a abrir sozinha (com "Arrancar com a TV" ligado).

Da primeira vez, o Android pede para autorizar a FullPlay a **instalar apps desconhecidas**: a app abre essa definição na TV; ative a FullPlay, volte atrás e escolha **Atualizar** de novo.

## Ainda não incluído nesta versão

- **NDI:** precisa do NDI SDK para Android (download no site da NDI, com aceitação da licença). A interface já mostra a fonte NDI como indisponível.
- **Pastas partilhadas SMB** (NAS, PC da régie): nesta versão, "Rede" aceita endereços HTTP, HLS e RTSP.
- Painel central para várias TVs: cada TV tem o seu backoffice.
