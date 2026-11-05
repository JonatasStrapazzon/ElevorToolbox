# Notas de versão

## 0.22.2

- **Editor conn.xml reinicia o aplicativo do ERP depois de salvar**, para o ERP ler o novo arquivo (ele guarda a conexão em memória). Usa o `Web.config` da pasta (vale para IIS e IIS Express, sem administrador) e, se não der, o `iisreset`. Veja [Editor conn.xml](docs/editor-conn-xml.md#depois-de-salvar-reinício-do-aplicativo).
- A janela de confirmação do salvamento mostra uma **barra de carregamento** durante o reinício e só libera o OK quando termina. Se falhar, mostra o motivo e pede o reinício manual do IIS.

## 0.22.1

- **Abrir o Toolbox de novo com ele na bandeja** voltou a funcionar quando a instância em segundo plano está como administrador: antes aparecia "O Toolbox já está aberto".
- **Atualização do ícone:** ao instalar ou atualizar, o Toolbox reaponta o ícone dos atalhos (Área de Trabalho, Menu Iniciar e barra de tarefas) e pede ao Windows que recarregue os ícones.
- Prints da documentação atualizados.

## 0.22.0

- **Novo módulo: Minhas tasks.** Lista as suas tasks ativas do Azure DevOps com **play/pause** do tempo (lança *Completed Work* e *Remaining Work* ao pausar), botões **Feature**, **Hotfix**, **Pull Request**, **Feature Retorno** e **PR Retorno** que copiam o nome para a área de transferência, e uma aba **Nome manual** que sugere, de uma vez, todos os nomes a partir de um texto digitado. Usa a conexão DevOps do Toolbox, sem campos próprios.
- **Extensão do navegador embutida**: o Toolbox prepara a extensão (Brave, Chrome ou Edge), abre a página de extensões e permite remover os arquivos. Veja [Minhas tasks](docs/minhas-tasks.md).
- **Novo ícone do aplicativo.**
- Documentação completa de todos os módulos, incluindo Direct SQL Server e PR Notifier.

## 0.21.3

- O link do Pull Request no PR Notifier mantém o repositório mesmo quando o campo *Repositório* da conexão está em branco.

## 0.21.2

- O Toolbox verifica atualização sempre que a janela reaparece (mesmo vivo na bandeja por causa do PR Notifier).

## 0.21.1

- O aplicativo não traz mais endereço de servidor fixo: o servidor e a fonte NuGet vêm da conexão DevOps configurada.

## 0.21.0

Primeira versão publicada como instalador.

- **Instalação automática** do ambiente em uma aba própria, com revisão completa antes de instalar, barra de progresso, tempo decorrido e parada no primeiro erro.
- **Instalação manual** mantida, agora com Git (detectar, localizar, baixar e instalar), Node.js (LTS ativa) e botão **Compilar solução**.
- **Atualização automática** via instalador (verifica ao abrir e a cada 6 horas).
- **Faixa de administrador** no topo, com *Reabrir como administrador*.
- **Módulos desativados por padrão** em instalação nova: só o Início aparece até você habilitar o que quiser.
- **Conexão DevOps** com campos em branco por padrão, Git sempre por PAT e conta de domínio com prefixo `elevor.local\`.
- Módulos que dependem do DevOps **exigem a configuração** para ativar e avisam quando ela falta.
- **Sem senha padrão embutida**: senha do `sa` e do domínio são digitadas manualmente.
- **Restauração de base** sugere o nome da base pelo nome do ZIP; no automático a auditoria vem como `auditoria`.
- Correção do clone por PAT com versões recentes do Git.
