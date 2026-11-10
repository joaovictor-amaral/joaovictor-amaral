# João Victor Amaral

Sou desenvolvedor full stack em Araruama (RJ). Passei pouco mais de dois anos cuidando de servidores, rede e backup antes de virar desenvolvedor em 2026. Hoje desenvolvo o ERP interno de uma empresa de turismo receptivo e transporte, em Java e Spring Boot, e coloco agentes de IA para trabalhar dentro dele.

Procuro um segundo contrato 100% remoto, CLT ou PJ. Meu LinkedIn: [linkedin.com/in/victoramrb22](https://www.linkedin.com/in/victoramrb22)

## O que construí (código privado da empresa)

**Atendente de manutenção no WhatsApp.** O motorista manda áudio, foto ou texto contando o problema do veículo. O agente (Gemini com tool calling) identifica o veículo, confere se já existe chamado aberto e registra tudo na API em Java. A primeira versão levava até 42 s para responder. O gargalo era o modo de raciocínio do modelo, desnecessário para uma tarefa tão direta. Reduzi esse modo ao mínimo e o tempo caiu para cerca de 3,8 s.

**Segurança de um agente que grava no sistema.** Uma auditoria interna mostrou que uma mensagem maliciosa poderia anotar "freio revisado" num chamado de freio ainda aberto. Tirei essa escolha do modelo: ele só enxerga apelidos como `chamado_1`, e quem decide em qual chamado gravar é o código. O sistema tem 137 testes automatizados, parte deles tentando exatamente esse tipo de ataque.

**Escritório Virtual.** Um MVP em que agentes de IA recebem pedidos da gestão e executam o trabalho, mas nenhuma entrega vale até uma pessoa aprovar. Cada passo fica registrado.

## Com o que trabalho

Java 21, Spring Boot, Spring Security, PostgreSQL, Flyway, JUnit e Mockito no back-end. React e TypeScript no front-end. Node.js e as APIs do Gemini e da OpenAI na camada de IA. Docker para empacotar e rodar.

---

English: full stack Java developer in Brazil. I build Spring Boot systems and the AI agents that work inside them. Open to remote work.
