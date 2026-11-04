# Notas de versão

## 0.21.1

- **Nenhum endereço de servidor fixo no aplicativo.** Credenciais do Git, clone, listagem de repositórios e a fonte NuGet usam o servidor da **conexão DevOps** configurada por cada usuário.
- **Fonte NuGet:** com o endereço em branco (padrão), o app monta o link com o servidor da conexão; sem conexão, a etapa é ignorada com aviso. O endereço continua editável.
- O modelo de `conn.xml` embarcado não traz senha.

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
