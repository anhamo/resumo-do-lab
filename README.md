# resumo-do-lab
Este repositório contém o resumo das lições aprendidas durante o desenvolvimento do lab na DIO sobre o MS 900.

Durante o lab aprendi:
1. Como criar uma conta no MS Azure;
2. Foi possivel dar um overview do ambiente do Azure;
3. Os servicos que ele suporta como banco de dados, redes, suporte a varias linguagens de programacao, docker etc...

   Em suma: esta sendo uma experiencia marravilhosa.


Beneficios da nuvem:
1. Disponibilidade
2. Escalabilidade
3. Elasticidade
4. Confiabilidade
5. Previsibilidade
6. Seguranca
7. Governanca
8. Gerenciabilidade

Tipos de servicos na Nuvem

1. IaaS (Infraestrutura como servico) - e o servico de nuvem mais flexivel em que o usuario configura e gerencia o hardware para o seu aplicativo;
2. Paas (Plataforma como servico) - focado no desenvolvimento de aplicativos. O gerenciamento da plataforma e realizado pelo provedor de nuvem;
3. SaaS (Software como servico) - modelo de preco de pagamento conforme o uso: os usuarios pagam  pelo software que utilizam em modelo de assinatura.

Nota: Nos tres tipos de nuvem descritos acima existe o modelo de responsabilidade compartilhada entre o provedor e usuario, porem sao diferentes por cada uma delas.


Arquitectura e Servicos do Azure
Existem varias contas no Azure conforme passo a descrever: 
1. Conta do Azure;
2. Conta gratuita do Azure;
3. Conta de estudante do Azure; e
4. Area restrita do Microsof Learn.

Outro ponto importante a destacar nesse resumo e que existem zonas de disponibilidade no Azure.
Zonas estas que fornecem protecao contra tempo de inatividade devido a falhas do datacenter.

E preciso tambem separar fisicamente os datacenters dentro da mesma regiao para evitar que caso um datacenter esteja inativo devido a queda de corrente por exemplo o outro possa assumir de modo que nao haja perda de sinal do servidor.

Salientar que cada datacenter e equipado com alimentacao, resfriamento e rede independente.

Pares de Regiao
Existem no minimo 300 milhas de separacao entre pares de regiao e a replicacao dos servicos e feita de forma automatica.
Ha recuperacao de regiao priorizada em caso de interupcao e as actualizacoes sao distribuidas sequencialmente para minimizar o tempo de inatividade.

Regioes Soberanas do Azure
As regioes soberanas do Azure atendem a necessidade de seguranca e conformidade das agencias federais, governos estaduais e locais dos EUA e seus provedores de solucoes.

A Azure foi o primeiro provedor de servicos na nuvem a oferecer esse servico a CHINA mas em conformidade com a Lei deles. Os dados la processados nao podem sair do pais conforme manda a Lei.

Recursos do Azure
Sao componentes como maquinas virtuais, contas de armazenamento, redes virtuais, servicos de aplicativos, banco de dados e funcoes.

Grupo de Recursos
Grupo de recurso e um conteiner que voce usa para gerenciar e agregar recursos em uma unica unidade.

Estes recursos podem existir em apenas unica unidade e podem existir em diferentes regioes.

Assinaturas
Existem tres tipos de assinaturas diferentes no Azure que sao
1. Assinatura de desenvolvimento;
2. Assinatura de teste; e
3. Assinatura de producao.

Armazenamento
Contas de armazenamento
- Deve ter um globalmente nome exclusivo;
- Fornecer acesso a internet;
- Determinar os servicos de armazenamento e as opcoes de redundancias.

Redundancia de Armazenamento
- LRS: nao indicado para producao pois as 3 copias sao feitas no mesmo local;
- ZRS: indicado para producao pois as copias sao feitas para tres zonas diferentes;
- GRS: Para regioes diferentes;
- GZRS: Para geografias diferentes.

Formas de armazenamento
1. Blob do Azure - otimizado para o armazenamento de quantidades massivas de dados nao estruturados.
2. Disco do Azure - fornece discos para maquinas virtuias, aplicativos e outros servicos acessarem e utilizarem.
3. Fila do Azure - servico de armazenamento de mensagens que fornece armazenamento e recuperacao para grandes quantidades de mensagens cada uma contendo ate 64KB.
4. Arquivos do Azure - configura um compartilhamento de arquivos de rede altamente disponivel que pode ser utilizado usando o protocolo bloco de mensagens do servidor.
5. Tabelas do Azure - fornece uma opcao de chave/atributo para o armazenamento de dados estruturados nao relacionais com um design sem esquema.

Camadas de acesso de armazenamento do Azure
1. Frequente - dados de acesso frequente;
2. Esporadico - dados acessados com pouca frequencia (30 dias)
3. Frio - dados acessados com pouca frequencia (90 dias)
4. Arquivo morto - dados acessados raramente e armazenados pelo menos 180 dias com requisitos de latencia flexiveis.

Migracoes para o Azure
1. Azure data box - servico de migracao fisica que pode levar ate 80TB de dados;
   - Proteje seus dados em uma caixa robusta durante o transito;
   - Move os backups de recuperacao de desastre para o Azure.
  
Opcoes de Gerenciamento de Arquivos
1. AzCopy
   - Utilitario de linha de comando;
   - Copiar blobs ou arquivos de ou para sua conta de armazenamento;
   - Sincronizacao em uma direcao.
  
2. Gerenciador de Armazenamento do Azure
   -Interface grafica do usuario (de modo semelhante ao windows explorer);
   -Compativel com o windows, Mac OS e Linux.

3. Sincronizacao de Arquivos
   - Sincroniza os arquivos do azure e locais de forma biderecional;
   - A camada de nuvem mantem os arquivos acessados com frequencia no local enquanto libera espaco.
  
Importante referir que o nome do armazenamento deve ter de 3 a 24 caracteres em letras minusculas, isto e, nao aceita letras maiusculas nem caracteres especiais.

Identidade, Acesso e Seguranca
Microsoft Entra ID e o servico de gerenciamento de identidades e acesso baseado em nuvem do Microsoft Azure

Responsabilidades
- Autenticacao (os funcionarios entram para acessar recursos);
- Logon unico (SSO);
- Gerenciamento de aplicativos;
- Negocios para negocios (B2B);
- Gerenciamento de dispositivos.

Benificios
- obtenha os beneficios dos servicos de dominio baseados em nuvem sem gerenciar os controladores de dominio;
- Execute aplicativos herdados (que nao podem utilizar padroes de autenticacao modernos) na nuvem;
- Sincronizar automaticamente a partir do Microsoft Entra ID.

  Autenticacao Vs Autorizacao
  Autenticacao
  - Identifica a pessoa ou servico buscando acesso a um recurso;
  - Solicita credenciais de acesso legitimo;
  - Base para criar principios  de identidade e controle de acesso seguros.
 
    
  Autorizacao
  - Determina o nivel de acesso de uma pessoa ou servico autenticado.
  - Define quais dados eles podem acessar e o que podem fazer com eles.
 
  Autenticacao Multi factor (MFA)
  - Fornece seguranca adicional para as identidades exigindo dois ou mais elementos para autenticacao completa.
 
  Acesso Condicional
  - Associacao de usuario ou grupo;
  - Local do IP;
  - Dispositivo;
  - Aplicativo;
  - Deteccao de risco

  Controle de Acesso baseado em funcao (RBAC)
  - Gerenciamento de acesso de granulidade fina;
  - Divida as tarefas dentro da equipe e conceda somente a quantidade de acesso de que os usuarios precism para trabalhar;
  - Habilite o acesso ao portal do Azure e o controle de acesso aos recursos.
 
  Confianca Zero
  * Protecao completa
    - Seguranca fisica;
    - Identidade fisica;
    - Permetro;
    - Rede;
    - Computacao;
    - Aplicativos; e
    - Dados.
     
 
A confianca zero e:
- Uma abordagem completa para proteger sistemas de computador;
- Fornecer varios niveis de protecao;
- Ataques contra uma camada sao isolados das camadas subsequentes.

Microsoft Defender for Cloud
- E um servico de monitoramento que fornece protecao contra ameacas nos datacenters do Azure e locais.
- Fornece recomendacoes seguras;
- Detectar e bloquear malware;
- Analisar e identificar ataques potenciais;
- Controle de acesso just-in-time para portas.

Gerenciamento e Governanca
Factores que afectam os custos:
1. Tipo de recurso - os custos sao especificos de recurso, portanto, o uso de um medidor rastreia o numero de medidores associados a um recurso, dependendo do tipo de recurso.
2. Consumo - com um modelo pago conforme o uso, o consumo é um dos maiores geradores de custos.
3. Manutencao - monitorar seu volume no Azure e manter seu ambiente pode ajudá-lo a identificar e reduzir os custos que sao necessarios, como ao desligar maquinas virtuais subutilizadas.
4. Area geografica - o mesmo tipo de recurso pode custar valores diferentes dependendo da area geografica, o que afecta os custos do Azure.
5. Trafego de rede - embora algumas transferencias de dados de entrada sejam gratuitas, o custo para dados de saida ou dados entre recursos do Azure é afectado por zonas de cobrança.
6. Assinatura - o tipo e a configuracao da assinatura também podem afectar o custo. Por exemplo: a avaliacao gratuita permite explorar alguns recursos do Azure gratuitamente.

Azure Marketplace
- O Azure marketplace permite que os clientes encontrem, experimentem, comprem e provisionem aplicativos e serviços de centenas de provedores de serviços lideres, que sao todos certificados para execuçao do Azure.

Governanca e Conformidade
- Blueprints, politicas e bloqueios de recursos;
- Portal de confianca do servico.

Azure Policy
O Azure Policy ajuda a impor padroes organizacionais e a avaliar a conformidade em escala.
- Ele fornece governanca e consistencia de recursos com conformidade regulatoria, seguranca, custo e gerenciamento.
- Avalia e identifica os recursos do Azure que nao atendem as suas politicas;
- Fornece definicoes de politicas e iniciativas integradas, em categorias como armazenamento, rede, computacao, central de seguranca e monitoramento.

Bloqueios de recursos
- Protege os recursos do Azure de exclusao ou modificacao acidental;
- Gerenciar bloqueios na assinatura, grupo de recursos ou niveis de recursos individuais dentro do portal do Azure.

Tipos de bloqueio
Tipos de bloqueio      Ler      Actualizar      Excluir
Excluir                Sim      Sim             Nao
ReadOnly               Sim      Nao             Nao

Portal de confianca de servico
- Fornece regras e protocolos que a microsoft segue.

Ferramentas de Gerenciamento e Implantacao
Ferramentas de gerenciamento de recursos
- Portal, PowerShell, CLI e outros;
- Azure Arc e Azure Resource Manager (ARM).

Ferramentas para interragir com o Azure 
- Portal do Azure;
- Azure PowerShell;
- Azure Cloud Shell;
- CLI (Command line interface);

Azure Arc
E uma ferramenta nos moldes de multicloud, facilita o gerenciamento de recursos que nao estao dentro do Azure. Exemplo: Ambiente Onpremise, AWS e GCP rodando um script para tal.

O Azure Arc serve para administrar o que esta fora do Azure.

Azure Resource Manager (ARM)
FOrnece uma camada de gerenciamento que permite criar, actualizar e excluir recursos na assinatura do Azure.

Infraestrura como codigo
- Garanta consistencia na implantacao em todo o ecossistema de nuvem;
- Gerencie a configuracao em escala;
- Provisione rapidamente ambientes adicionais com base em uma configuracao e um build padrao.

Modelos ARM
Sao arquivos JSON (JavaScript Object Notation) que podem ser usados para criar e implantar a infraestrutura do Azure sem a necessidade de escrever comandos de programacao.

Pre-requisitos
- Sintax declarativa;
- Resultados repetitivos;
- Orquestracao;
- Arquivos modulares;
- Validacao integrada;
- Codigo exportavel.

Azure Bicep
E uma linguagem nativa do MS Azure para criar recursos para automatizacao e serve so para a Microsft.

Microsoft Purview
E uma familia de solucoes de governanca, risco e conformidade de dados que ajuda voce a obter uma unica exibicao unificada em seus dados.
O Microsoft Purview reune insights sobre seus dados locais, multinuvem e de software como servico (SaaS).

Faz com que a descoberta de dados seja automatizada;
Classificacao de dados confidenciais;
Linhagem de dados de ponta a ponta.


Ferramentas de Monitoramento
- Assistente do Azure: analisa recursos implantados do Azure e faz recomendacoes com base nas praticas recomendadas para optimizar as implantacoes do Azure baseados em confiabilidade, seguranca, desempenho, custo e excelencia operacional.

- Integridade do servico do Azure: e' uma colecao de servicos que mantem voce informado sobre status geral do Azure, status de servicos que podem afectar voce e o status de recurso especifico que esta afectando voce.

- Status do Azure: visao global da integridade de todos os servicos do Azure em todas as regioes do Azure.

- Integridade do servico: exibicao focada apenas nos servicos e regioes que voce esta usando. Se um servico estiver enfrentando um problema em uma regiao que voce nao esta usando, ele nao aparecera aqui.

- Resource Health: exibicao personalizada dos recursos reias do Azure. Ele fornece informacoes sobre integridade de seus recursos de nuvem individuais.

- Azure Monitor: Maximiza a disponibilidade e o desempenho de aplicativos e servicos colectando, analisando e tomando decisoes com base na telemetria da nuvem e de ambientes locais.
