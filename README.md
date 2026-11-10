# João Victor Amaral

Sou desenvolvedor full stack em Araruama (RJ). Passei pouco mais de dois anos cuidando de servidores, rede e backup antes de virar desenvolvedor em 2026. Na IN Búzios, empresa de turismo receptivo e transporte, projetei e coloquei em produção o NÓDUNI, o ERP da empresa, e os agentes de IA que trabalham com ele.

Procuro um segundo contrato 100% remoto, CLT ou PJ. LinkedIn: [linkedin.com/in/victoramrb22](https://www.linkedin.com/in/victoramrb22)

## O que construí (código privado da empresa)

**NÓDUNI.** Monólito modular em Java 21 e Spring Boot 4.1 que junta frota e manutenção, RH/DP, SST e multas. Cada setor é um módulo com perfis de acesso e área própria no PostgreSQL. O núcleo não depende de IA: os agentes entram pela API como qualquer outro cliente, com credencial própria e permissão mínima. Roda numa VPS com Docker Compose e Caddy, com homologação e produção separadas, mais de 30 versões publicadas e backup diário cifrado.

**Agente de manutenção no WhatsApp.** O motorista manda áudio, foto ou texto contando o problema. O agente (Gemini com function calling) identifica o veículo, confere se o problema já foi relatado e abre o chamado. Quando um modelo falha, a chamada passa para o próximo da fila. A primeira versão levava até 42 s para responder. O gargalo era o modo de raciocínio do modelo; reduzi ao mínimo e o tempo caiu para cerca de 3,8 s.

**Limites para um agente que grava no sistema.** Uma auditoria interna mostrou que uma mensagem maliciosa poderia anotar "freio revisado" num chamado de freio ainda aberto. Tirei essa escolha do modelo: ele só enxerga apelidos como `chamado_1`, e quem decide em qual chamado gravar é o código. As conversas ficam cifradas e expiram sozinhas.

**Cariocão.** Agente de vendas que atende clientes 24 horas no WhatsApp, integrado à plataforma de reservas. Roda separado do ERP, com banco e Redis próprios. Quando volta de uma queda, responde o que ficou pendente sem mandar nada em dobro.

**Dados de colaboradores.** O módulo de RH guarda dados pessoais, então esses campos ficam cifrados no banco, aparecem mascarados conforme o perfil e cada acesso a uma ficha fica registrado. Os prazos de guarda e descarte seguem a LGPD.

## Com o que trabalho

Java 21, Spring Boot, PostgreSQL, Flyway, JUnit e Mockito no back-end. React, TypeScript e MUI no front-end. Node.js e as APIs do Gemini e da OpenAI nos agentes. Docker, Caddy e Redis na operação.

---

English: full stack Java developer in Brazil. I built and run my company's ERP and the AI agents that work with it. Open to remote work.
