ANOTAÇÕES DE AULA

EC2 = serviço de computação elástica da AWS (máquinas virtuais)

Tipos de instância: t2.micro (Free Tier), m5.large, etc.

AMI (Amazon Machine Image) define o sistema operacional e configurações iniciais

Acesso via SSH exige chave privada (.pem)

Grupos de segurança controlam tráfego de entrada/saída (ex: liberar porta 22 para SSH)

Elastic IP = IP fixo público que pode ser associado à instância

Instância pode ser parada, iniciada ou terminada (terminar = apagar tudo)

EBS – Armazenamento em Bloco
EBS = disco virtual que pode ser anexado à instância EC2

Tipos: General Purpose (gp2/gp3), Provisioned IOPS (io1/io2), Cold HDD (sc1), etc.

Pode ser montado como /dev/xvdf ou similar

Precisa ser formatado e montado manualmente após anexar

Persistência: adicionar ao /etc/fstab para montar automaticamente na inicialização

Snapshot = backup do volume EBS (pode ser restaurado ou duplicado)

S3 – Armazenamento de Objetos
S3 = serviço para armazenar arquivos (imagens, vídeos, backups, etc.)

Bucket = “pasta raiz” onde os objetos são armazenados

Cada objeto tem uma URL pública (se configurado)

Classes de armazenamento: Standard, IA (Infrequent Access), Glacier, Deep Archive

Lifecycle rules = regras para mover arquivos entre classes automaticamente

Versionamento pode ser ativado para manter histórico de alterações

IAM – Controle de Acesso
IAM = gerenciamento de usuários, permissões e políticas

Usuários podem ter acesso programático (via CLI/API) ou console

Políticas definem o que cada usuário pode fazer (ex: acesso ao S3, EC2, etc.)

Grupos facilitam atribuição de permissões em massa

MFA (autenticação multifator) recomendada para segurança

Conceitos Gerais de AWS
Região = localização geográfica (ex: us-east-1, sa-east-1)

Zona de disponibilidade = datacenter dentro da região

Alta disponibilidade = distribuir recursos entre zonas

Escalabilidade = aumentar ou reduzir recursos conforme demanda

Elasticidade = ajustar automaticamente conforme uso
