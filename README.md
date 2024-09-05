# Usando a NIST Cybersecurity Framework para responder a um incidente de segurança
> Olá!! Bem vindo ao estudo de caso *"Resposta a um Ataque DDoS por Inundação de ICMP"*. A seguir você encontrará uma breve explicação de como aplicar o NIST CSF, um resumo sobre o estudo de caso e por fim o relatório de incidente.

## Summary
- [Aplicando o NIST CSF](#)
- [Estudo de Caso: Resposta a um Ataque DDoS por Inundação de ICMP](#)
- [Análise de relatório de incidente (pdf)]()
## `Aplicando o NIST CSF`

Existem cinco funções principais no framework NIST CSF: identificar, proteger, detectar, responder e recuperar. 

(imagem)

Essas funções principais ajudam as organizações a gerenciar riscos de cibersegurança, implementar estratégias de gerenciamento de risco e aprender com erros anteriores. Planos baseados nesse framework devem ser continuamente atualizados para se manterem à frente das ameaças de segurança mais recentes. As funções principais ajudam a garantir que as organizações estejam protegidas contra possíveis ameaças, riscos e vulnerabilidades. Cada função pode ser usada para melhorar a segurança de uma organização:

- **Identificar:** Gerenciar riscos de segurança por meio de auditorias regulares de redes internas, sistemas, dispositivos e privilégios de acesso para identificar possíveis lacunas na segurança.
- **Proteger:** Desenvolver uma estratégia para proteger ativos internos por meio da implementação de políticas, procedimentos, treinamentos e ferramentas que ajudem a mitigar ameaças de cibersegurança. 
- **Detectar:** Escanear possíveis incidentes de segurança e melhorar as capacidades de monitoramento para aumentar a velocidade e a eficiência das detecções. 
- **Responder:** Garantir que os procedimentos adequados sejam utilizados para conter, neutralizar e analisar incidentes de segurança, e implementar melhorias no processo de segurança. 
- **Recuperar:** Retornar os sistemas afetados à operação normal e restaurar os dados e ativos dos sistemas que foram afetados por um incidente. 

Alguns aspectos a serem abordados para cada uma das cinco funções principais incluem:

| Função  | Descrição |
|--|--|
| Identificar  | Crie um inventário dos sistemas, processos, ativos, dados, pessoas e capacidades a proteger. Identifique dispositivos e softwares afetados, rastreie o ataque na rede interna e avalie os processos de negócios impactados. Determine quem precisa de acesso aos sistemas comprometidos.|
| Proteger  |  Desenvolva e implemente salvaguardas com foco em controle de acesso, definindo quem precisa acessar os itens afetados e bloqueando fontes não confiáveis. Realize campanhas de conscientização e capacitação para informar sobre o ataque e como evitá-lo no futuro. Reforce a segurança dos dados impactados e revise ou crie novos procedimentos para proteger os ativos e garantir a continuidade dos serviços.|
| Detectar  | Projete um sistema com ferramentas como um SIEM para detectar anomalias e alertar a equipe de segurança em tempo real. Implemente soluções de monitoramento contínuo, como firewalls e sistemas de monitoramento de rede, para identificar eventos suspeitos. Use ferramentas de detecção de intrusões (IDS) e análise de comportamento para identificar ataques e responder rapidamente a incidentes de segurança. |
|  Responder | Crie planos de resposta, definindo ações específicas para lidar com ataques futuros, incluindo isolamento de recursos e contenção de danos. Estabeleça uma comunicação clara entre a equipe de TI, usuários finais e partes afetadas, garantindo que os procedimentos sejam conhecidos. Execute análises pós-ataque para identificar vulnerabilidades e falhas. Implemente medidas de mitigação imediata, como desconectar ou isolar recursos comprometidos. Promova melhorias contínuas nos processos de resposta, baseadas em lições aprendidas, para fortalecer a defesa contra futuros incidentes.|
| Recuperar  | Desenvolva um plano de recuperação que defina etapas claras para restaurar sistemas e dados afetados, incluindo a identificação de recursos críticos e processos de recuperação. Revise e melhore os sistemas e processos de recuperação existentes para aumentar a eficiência e reduzir o tempo de inatividade. Estabeleça um protocolo de comunicação para informar a equipe de TI, usuários finais e partes afetadas sobre os procedimentos de restauração, garantindo transparência e coordenação durante o processo.|

O NIST CSF e suas cinco funções principais fornecem um framework que abrange desde o planejamento proativo até a aplicação de medidas reativas contra ameaças de cibersegurança. Essas funções são essenciais para garantir que uma organização tenha estratégias de segurança eficazes em vigor. A organização deve ter a capacidade de se recuperar rapidamente de qualquer dano causado por um incidente para minimizar seu nível de risco.

## `Estudo de Caso: Resposta a um Ataque DDoS por Inundação de ICMP`

#### **Resumo do Incidente**
Recentemente, a empresa enfrentou um grave incidente de segurança cibernética quando todos os serviços de rede cessaram de responder abruptamente. A investigação revelou que a interrupção foi causada por um ataque de negação de serviço distribuído (DDoS), caracterizado por uma inundação de pacotes ICMP. A equipe de cibersegurança atuou rapidamente para mitigar o ataque, bloqueando-o e interrompendo serviços de rede não críticos para restaurar a operação dos serviços essenciais.

#### 1. Identificar
- **Descrição do Incidente:** Um ou mais agentes maliciosos direcionaram um ataque de inundação ICMP contra a infraestrutura de rede da empresa. O ataque afetou toda a rede interna, exigindo uma resposta imediata para proteger e restaurar os recursos críticos.
- **Ação:** A equipe de cibersegurança realizou uma análise para identificar a fonte e a natureza do ataque, determinando que a rede interna estava saturada com pacotes ICMP maliciosos.

#### 2. Proteger
- **Medidas Implementadas:** A equipe de cibersegurança adotou medidas para proteger a rede contra o ataque em curso e prevenir futuros incidentes:
  - **Regra de Firewall:** Foi criada uma nova regra para limitar a taxa de pacotes ICMP recebidos, ajudando a mitigar o impacto do ataque.
  - **Sistema IDS/IPS:** Foi implementado um sistema de Detecção e Prevenção de Intrusões (IDS/IPS) para filtrar pacotes ICMP com características suspeitas, aumentando a capacidade de defesa da rede.

#### 3. Detectar
- **Ações Realizadas:** A equipe configurou novas capacidades de detecção para identificar ataques semelhantes no futuro:
  - **Verificação de IP:** O firewall foi configurado para verificar endereços IP de origem, ajudando a identificar pacotes ICMP falsificados.
  - **Monitoramento de Rede:** Foi introduzido um software de monitoramento para detectar padrões anômalos de tráfego que pudessem indicar a presença de ataques.

#### 4. Responder
- **Plano de Resposta:** A equipe de cibersegurança elaborou um plano de resposta para gerenciar futuros eventos de segurança:
  - **Isolamento de Sistemas:** Sistemas afetados serão isolados para prevenir a propagação do ataque e minimizar a interrupção de rede.
  - **Restauro de Serviços:** Serviços e sistemas críticos foram restaurados com prioridade.
  - **Análise e Comunicação:** Logs de rede foram analisados para identificar atividades suspeitas e o incidente foi reportado à administração e, se necessário, às autoridades legais.

#### 5. Recuperar
- **Plano de Recuperação:** A recuperação do ataque envolveu os seguintes passos:
  - **Restabelecimento de Serviços:** Os serviços de rede foram restaurados progressivamente, começando pelos críticos e, posteriormente, pelos não críticos.
  - **Bloqueio Futuro:** Medidas foram estabelecidas para bloquear ataques de inundação de ICMP no firewall, minimizando o risco de futuros incidentes.
  - **Interrupção de Serviços Não Críticos:** Durante o pico do ataque, serviços de rede não críticos foram temporariamente desligados para reduzir o tráfego interno e facilitar a recuperação.

O NIST CSF oferece uma abordagem estruturada e abrangente para a gestão da cibersegurança, englobando as funções essenciais de identificar, proteger, detectar, responder e recuperar. O estudo de caso sobre o ataque DDoS demonstra a eficácia prática dessas funções na proteção de ativos críticos e na otimização da resposta a incidentes. A aplicação rigorosa e a adaptação contínua do NIST CSF são imperativas para assegurar a resiliência organizacional diante das ameaças dinâmicas e em constante evolução no cenário de segurança cibernética.