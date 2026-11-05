# Solução de problemas

> ver o [índice da documentação](../README.md#documentação) · problemas específicos de cada módulo estão nas páginas [PR Notifier](pr-notifier.md#solução-de-problemas) e [Direct SQL Server](direct-sql-server.md#solução-de-problemas)

## Instalação e abertura

| Sintoma | O que fazer |
|---|---|
| **"O Windows protegeu o computador"** (SmartScreen) ao executar o Setup | O instalador ainda não é assinado digitalmente. Clique em **Mais informações** e depois em **Executar assim mesmo**. |
| **Faixa "Sem administrador…" no topo** | Use **Reabrir como administrador**. As etapas do Ambiente de trabalho precisam disso. |
| **O Toolbox "não abre"** | Ele roda **uma instância por vez**; se ele estiver na bandeja (PR Notifier), o ícone fica perto do relógio (setinha **^**). Dê duplo clique nele. |
| **Não consigo habilitar um módulo** | Gerador de tasks, PR Notifier e Ambiente dependem da [conexão DevOps](conexao-devops.md) (e o Ambiente, da conta de domínio). Complete em engrenagem → **DevOps**. |

## Ambiente de trabalho

| Sintoma | O que fazer |
|---|---|
| **"MSBuild não encontrado"** ao compilar | Instale o Visual Studio com a carga de trabalho de desenvolvimento web ou desktop (etapa 3). |
| **A instalação do SQL Server falhou** | Consulte `C:\Program Files\Microsoft SQL Server\<versão>\Setup Bootstrap\Log\Summary.txt` (e a pasta `...\SSEI\LogFiles`). Confira se a senha do `sa` atende à complexidade e se há espaço em disco. |
| **O clone falhou** | Use **Testar PAT** na conexão DevOps e confira a rede/VPN até o servidor. A mensagem termina com o *Detalhe do Git*. |
| **A pasta de destino do clone não está vazia** | O módulo nunca sobrescreve nem atualiza um repositório existente. Escolha uma pasta vazia. |
| **A instância SQL já existe** | A instalação sobre o mesmo nome é bloqueada. Escolha outro nome ou instale só o SSMS. |
| **O IIS pede reinício** | A etapa informa e bloqueia novas alterações até reiniciar e consultar de novo. |
| **A atualização ou o aviso não aparecem** | Veja [Atualizações](atualizacoes.md#se-o-aviso-não-aparece). |

## Conexão DevOps

| Sintoma | O que fazer |
|---|---|
| **"Falha de autenticação"** | O PAT expirou ou não tem a permissão certa. Gere outro e cole em engrenagem → DevOps. |
| **Links do PR Notifier sem o nome do repositório** | Atualize o Toolbox (corrigido na 0.21.3). Você também pode preencher **Repositório** na conexão. |
| **Fonte NuGet ignorada** | O endereço do feed está em branco e não há conexão. Configure a conexão ou informe o endereço completo do feed. |

## Dados e logs

| O quê | Onde |
|---|---|
| Preferências, tema e módulos | `%APPDATA%\ElevorToolbox` |
| Logs de compilação e instalação | `%LOCALAPPDATA%\ElevorToolbox\logs` |
| Aplicativo instalado | `%LOCALAPPDATA%\ElevorToolbox` |
