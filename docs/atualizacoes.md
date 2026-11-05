# Atualizações

> ver o [índice da documentação](../README.md#documentação)

## Como o Toolbox se atualiza

Instalado pelo **Setup** (`ElevorToolbox-win-Setup.exe`), o Toolbox **procura versão nova sozinho**:

- cerca de **8 segundos depois de iniciar**;
- **toda vez que a janela volta a aparecer** (mesmo com o aplicativo vivo na bandeja por causa do PR Notifier), no máximo uma vez a cada 2 minutos;
- **a cada hora** enquanto estiver aberto.

Quando há uma versão nova, o número no cabeçalho vira um aviso clicável: `v0.22.1 → v0.22.2 — atualizar`. Ao clicar, o Toolbox confirma, **baixa a atualização** (com a porcentagem) e **reinicia já na versão nova**. Ele não atualiza durante uma operação em andamento nem com alterações não salvas.

As atualizações vêm das **Releases** deste repositório. Os módulos (Ambiente, Editor conn.xml, Gerador de tasks, Direct SQL Server, PR Notifier e Minhas tasks) são atualizados **junto**, no mesmo pacote.

## Observações

- **Só a versão instalada pelo Setup se atualiza.** Executar os arquivos de uma pasta (por exemplo, o `Portable.zip`) não recebe atualização automática; o cabeçalho informa isso na dica.
- As **atualizações são parciais (delta)** quando possível, então costumam ser pequenas.
- Suas **configurações e dados não são apagados** na atualização (ficam em `%APPDATA%\ElevorToolbox`).
- O Setup **não pede administrador** e instala por usuário em `%LocalAppData%\ElevorToolbox`.
- As notas de cada versão estão no [CHANGELOG](../CHANGELOG.md) e na página de **Releases**.

## Se o aviso não aparece

1. Confira a internet e se você abriu o Toolbox **instalado** (Menu Iniciar), não uma cópia solta.
2. Feche o Toolbox por completo (bandeja → **Sair**) e abra de novo: ele procura ao iniciar.
3. Instale a versão mais recente manualmente pela página de **Releases** (o Setup atualiza por cima).
