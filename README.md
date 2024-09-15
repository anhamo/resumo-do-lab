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
