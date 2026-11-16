# Histórico de versões

## FullPlay

### 0.3.0
- **Enviar para a PEN USB:** na Biblioteca do backoffice, **Enviar para › PEN USB** e a pasta (por omissão `FullPlay`). Em Android 11 ou mais recente é preciso autorizar **Acesso a todos os ficheiros** uma vez (botão **Autorizar na TV**, ou no menu da TV › Definições); sem isso, os ficheiros ficam na pasta da FullPlay na PEN (`Android/data/pt.eventuais.fullplay/files`).
- **Camadas do layout:** lista de camadas no editor de layout; arraste pela pega ⋮⋮ para subir ou descer (ou Alt + ↑/↓). A de cima fica à frente.
- **QR code personalizado:** o widget QR mostra o Mobile Control, um endereço, um texto ou uma rede Wi-Fi, com legenda e cores à escolha.
- **Reprodução ativa:** interruptor no Painel, no telemóvel e no menu da TV. Desligada, a TV fica em negro e sem som e a agenda não põe nada no ar; escolher um conteúdo volta a ligar. Também por OSC: `/fullplay/playback 0|1`.
- **Ao arrancar, retomar o que estava no ar:** nova opção em Ecrã e rede (ligada por omissão).

### 0.2.0
- **Licença:** licenças `FP1.…` emitidas pela app Licenças Eventuais, confirmadas sem Internet. Sem licença, tudo funciona com a marca de água "FullPlay · modo demonstração". Uma licença pode ficar presa a uma TV (ID da TV) e incluir ou não NDI e OSC. Ativa-se no backoffice, no telemóvel ou com o ficheiro `.fplicense` numa PEN USB.
- **Atualizações:** a TV procura versões novas ao arrancar e de 6 em 6 horas. **Atualizar** (backoffice, telemóvel ou menu da TV) descarrega a versão nova e abre o instalador do Android, que pede OK no comando. Depois de instalada, a FullPlay volta a abrir sozinha.
- Nova secção **Licença e versão** no backoffice, no menu da TV e no separador Ecrã do telemóvel.
- Novo logótipo e ícone, nas cores da Eventuais.

### 0.1.0
- Primeira versão: playlists, full screen e layout, agenda e horário, rotação, mira de testes, menu na TV, backoffice e Mobile Control com PIN, OSC.
