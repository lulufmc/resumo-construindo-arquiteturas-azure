# resumo-construindo-arquiteturas-azure
Este repositório contém um resumo sobre o módulo " Contruindo Arquiteturas no Azure"

# Passo a passo para criação de um grupo de recursos e uma rede virtual

Após fazer o login, vá na barra de pesquisa e pesquise por "Grupo de recursos" e clique em "Criar". Escolha uma assinatura, um nome, uma região e depois clique em "avançar" 2x. Após a validação ser aprovada, clique em "Criar". Após a criação do grupo de recursos, na barra de pesquisa, pesquise por "Redes Virtuais" e clique em "Criar". Escolha a assinatura, o grupo de recursos, o nome da rede virtual, a região, e depois em "Analisar e criar".

# Componentes de Arquitetura do Azure

- Regiões e Zonas de disponibilidade

Usar zonas de disponibilidade e regiões estrategicamente ajuda a garantir a resiliência, desempenho e segurança dos seus sistemas na nuvem.

REGIÕES: Uma região é uma localização geográfica onde os recursos de computação em nuvem são armazenados. Cada provedor de nuvem, como AWS, Azure e Google Cloud, tem várias regiões espalhadas pelo mundo, e essas regiões são compostas por zonas de disponibilidade. Escolher uma região próxima ao seu público ou usuários reduz a latência, e você pode distribuir recursos entre várias regiões para maior segurança e disponibilidade.

ZONAS DE DISPONIBILIDADE: É um data center dentro de uma região, com independência de energia, rede e recursos. Fornece proteção contra tempo de inatividade devido a falha do datacenter. Ao distribuir recursos entre múltiplas AZs, você pode garantir que um problema em uma AZ não afete seu serviço. Pode-se configurar também arquiteturas de failover, onde se uma AZ falhar, o tráfego é redirecionado para outra AZ.

- Pares de região e Grupos de Recursos

PARES DE REGIÃO: consiste em duas regiões geograficamente separadas dentro da mesma área global (exemplo: América, Europa ou Ásia). Essas regiões são conectadas por uma rede de alta velocidade e possuem mecanismos de sincronização para garantir backup, redundância e continuidade de negócios. Exemplo: No Azure, as regiões Brasil Sul e Sul dos EUA formam um par. Isso significa que, caso haja um desastre em Brasil Sul, os dados ou serviços podem ser transferidos para Sul dos EUA. Se você deseja alta resiliência, segurança e recuperação rápida de desastres, configurar seus serviços com base em pares de região é uma prática recomendada. Isso protege seus dados e garante a continuidade dos negócios mesmo em cenários extremos.

REGIÕES SOBERANAS: Existem apenas duas, a Região Governamental dos EUA e China. Ambos possuem seus recursos específicos que apenas eles tem, e de mais ninguém. Os recursos do Azure na China são operados pela 21Vianet, e todos os dados permanecem dentro do país para garantir a conformidade. Nos EUA, são atendidos serviços governamentais para atender às necessidades de segurança e conformidade das agências federais, governos estaduais e locais dos EUA e seus provedores de soluções.

GRUPO DE RECURSOS: Um grupo de recursos é um contêiner que você usa para gerenciar e agregar recursos em uma única unidade. Os recursos podem existir em apenas um grupo de recursos, e podem existir em diferentes regiões. Os grupos de recursos podem conter apenas recursos de uma mesma região.

- Assinaturas e Grupos de gerenciamento

ASSINATURAS: fornecem acesso autenticado e autorizado às contas do Azure. Uma conta pode ter várias assinaturas, mas uma assinatura só pode estar vinculada a uma conta. Uma melhor estratégia para refinar os custos dentro do Azure seria, para cada grupo de trabalho seja criado uma assinatura diferente.

GRUPOS DE GERENCIAMENTO: podem incluir várias assinaturas do Azure. As assinaturas herdam as condições aplicadas ao grupo de gerenciamento. Ou seja, os grupos de gerenciamento estão no topo da hierarquia da conta, e cada grupo pode conter várias assinaturas, e os recursos dentro dessas assinaturas herdam as políticas e configurações do grupo.
