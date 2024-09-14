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
