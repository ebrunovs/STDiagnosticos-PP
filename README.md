# Sistema de Gerenciamento de Exames - IF Diagnósticos

Este projeto visa atender às necessidades da IF Diagnósticos, oferecendo um sistema flexível, reutilizável e de fácil manutenção para gerenciamento de exames médicos, emissão de laudos e comunicação com pacientes. A solução foi desenvolvida com foco na aplicação de padrões de projeto para garantir extensibilidade e desacoplamento entre os componentes do sistema.

## Estrutura da Solução

A arquitetura do sistema foi construída com base em diversos padrões de projeto. Cada requisito funcional foi analisado individualmente e resolvido com um ou mais padrões que melhor se aplicam ao cenário descrito.

---

## Diagrama de Classes
![Diagrama UML](https://uml.planttext.com/plantuml/png/lLZ9RkGs4BttLn1pcMwCDHyW9COuNYODU8kNvD90m9ReDX6952ZAiJCpNvD3FY389LV_M8eKLpNbbf59V33KLQ-AjQke3wt4GdPrDPEyGPAZDPUIrwYaWXIISZQRlVtsXR_PMtHDsQOYahCSVIG2broWag3bKRj3ii75BtX3q1kdOCNcWORpvxzh8lZY3VeqGwYeSDlQ0yuxnJb-n3NHJ8Go18v8MY3Au84L94zW3P9foe7iS9K3NchoExGXScc4vujHSOKJs90LhbVmPVPbTwHES26vU49dHDxpCaTQw-GmnT8GgrxSn0UlMoa0OG8LnmPqKC8a1ENIF1bV1C4L_GqB3LVUF71QQdTSoBydDTy8N6D7kQtWfBRbJD7lg6TS4KM5008DY4uIPLsJVTv7Def31KD-e2TcZVXf8_F9U5K86hXajQPyCfAx1CSyVwLuuDUAdU4D8r2nhz0JnjJw7CR7q18HVXczowwa6CX5mSyocwK9dV2TeEK6ol4KToLl4K5tNDHOyidDq2k09j0Q86OdlO9qD_GWsmtchDpAQAxX4UM1ZxaYyNLBn0CkC4XSk6V3V83-ATMSoD6FzZ6kDQrznNmpa4T9M6aOGvXB73QjyI8wdRY130Z1Z2BY3XSaSjdrYvveXnn0G4rFWSkZ4zyzDsUdxiSD7ARF00HwtpNleKu6SLNu4PQMJl96aXYskZ5Sq-TXulPMJ6KjJ9SYfNArC3KuUo5ZAnRqvrS-T4Vw_yUZqxNqNne06aT3ZRAI_yhKq0dJxYL60xLBS8UR8-9Mtg9ubWrBEUBtMlmRBScCXaaIuQA6SX_C9QDWV3Lbp1xUOmgPkLCJlk6ifMjQKVaqTSYEYCFKxGrx_kFvTpjn_OZnHjlvqfikveeAHNA66wY2DUSLmSn0MY8l1N-aDP-FLCtsJEgv4BwWW5BCmLgI4hCZA9pXQGtRI0TLBcU3h3MzKrEIrPS30RVFkQHtK9KGtx-cxuTM7j8JAzZAa2cyC4NCI8XvJLWB-keSNKi1ctaoz3_TOzaUDCsAsQD0sUjqMLNNTViLj1pNc5R_GW_yI_faq-r31iYXoKdGjaK9c7-_chtS9GINqELGSyAZv-68LKqHxYp0EQMj_4PFd7t3gVHwPJXwmknRRzs1QfH5XZjE5WomYEW6-Cwh8GnfIJPFEJeYRG4BnlG5puf2DJlPhKAs70lsDm1S5Ls5XGMeeQ86IicxTKKMzY4kQWjUCTY57WYZFC5QGa3rThADjlaTMXM1jVmeqjUpYhjbkysr7E3pr5cwUffAbVn4z-F3L44arFOtIbSJ5X5n4dVc2LLoAIWNy5v1FtIaWvNYX5PuQfd4ib0iIbXzFOWkntrC5Ml5UWcOpu3kGTizrz-zeWq79hcLov7NiJ2YV0qrQTzWmqiROLqTo9ZpRgy-7f_V7EldoulRmukVGyhLnSto_C1g63KzxD5HaCge9q_yKg4TNRfMW-l2DKmHKazEJQz3Nz7M7Che-Kym8Kg8OO1TN2zWFZQm472eO2fjBhQ_OEmXIPk-o7RaQC_rpNQ_BCAxtZj4QYffQi5DNnhTCclIb7B8PIXSHTCmzt5cGeRE2BpEfB-IlcvNCDAGd4WyoevVJztyaUgwPb-VuSSAeqzLlXSpHFUfgPMu4-ezd00jub7i-R2azmXdXD9J3gtO47ciwSe4nma_-K3nGi0BK9XmhDTftvHRrktReiJL0rHaVz2O6v6p1aiPZ1QYFnQEX4YR6bYMHHS45mLrdKvw4hp61_Y1qgIughWFX9NgG_0_)


---

## Requisitos Funcionais e Padrões Aplicados

## Requisito R2 - Gerar o número sequencial do exame, sem repetição

**Padrão de Projeto Aplicado:** Singleton

**Como será utilizado:**  
Será criada uma classe `GeradorSequencial` que encapsula a lógica de geração de identificadores únicos. Essa classe seguirá o padrão Singleton, garantindo que apenas uma instância exista em toda a aplicação.

**Justificativa:**  
Garante unicidade na geração dos números de exame, evitando conflitos, duplicações ou inconsistências, especialmente em ambientes concorrentes.

---

## Requisito R3 - Emitir laudo dos seguintes exames: Hemograma, Ultrassonografia e Ressonância Magnética. Outros tipos de exames poderão surgir no futuro, como por exemplo a Tomografia. Os novos tipos de exames a serem adicionados não devem impactar o funcionamento do código já existente.

**Padrão de Projeto Aplicado:** Factory Method

**Como será utilizado:**  
Cada tipo de exame terá sua própria implementação e será criado por meio de fábricas específicas que herdam de uma interface comum. O sistema usará essas fábricas para instanciar os objetos corretos sem depender das classes concretas.

**Justificativa:**  
Desacopla a criação dos tipos de exame, facilitando a inclusão de novos exames sem a necessidade de alterar código existente, respeitando o princípio Open/Closed (aberto para extensão, fechado para modificação).

---

## Requisito R4 - Gerar laudos para diferentes exames, inicialmente nos formatos texto, HTML e PDF. Outros tipos de formato poderão surgir no futuro, como por exemplo o JSON. Os novos formatos de exames a serem adicionados não devem impactar o funcionamento do código já existente. Qualquer tipo de laudo deve ser gerado em seu formato específico, inclusive em PDF (utilize a API de sua preferência)

**Padrão de Projeto Aplicado:** Bridge

**Como será utilizado:**  
Será criado um desacoplamento entre a abstração `Laudo` e as implementações de formato (`FormatoPDF`, `FormatoHTML`, `FormatoTexto`). O laudo utilizará uma referência a um objeto que implementa a interface `Formato`.

**Justificativa:**  
Permite variar independentemente a estrutura do laudo e o seu formato de saída. Facilita a extensão futura com novos formatos sem modificar as abstrações já existentes.

---

## Requisito R5 - Adicionar as regras de validação de cada exame, de maneira extensível. A validação do Hemograma só analisa se os valores medidos não excedem 50% do valor máximo e do valor mínimo. Por exemplo, se para Hemoglobina os valores de referência são de 13.0 a 18.0 milhões/dl, os extremos não podem exceder 6.5 e 27 milhões/dl. No caso de uma ressonância magnética, há diferentes regras de validação que devem ser verificadas, não importando a ordem, como: (a) verificar a presença de implantes gerais.

**Padrão de Projeto Aplicado:** Chain of Responsibility

**Como será utilizado:**  
Cada regra de validação (como limites de hemograma, presença de implantes, detecção de metais, entre outros) será encapsulada em uma classe que implementa a interface `Validador`. Essas classes serão organizadas em uma cadeia de responsabilidade, onde cada validador executa sua regra e, se aplicável, repassa o controle para o próximo na cadeia.

**Justificativa:**  
O padrão Chain of Responsibility permite criar uma sequência flexível e desacoplada de verificações. Isso facilita a adição, remoção ou reorganização de regras de validação sem impactar o restante do código, promovendo extensibilidade e modularidade.


**Justificativa:**  
Facilita a criação de regras modulares e reutilizáveis, permitindo encadear validações específicas sem alterar o fluxo geral do sistema.

---

## Requisito R6 - Notificar o paciente quando um laudo for emitido (inserido no sistema), por WhatsApp. Outros mecanismos de notificação serão adicionados futuramente (e.g. SMS ou E-mail) e não devem impactar o funcionamento do código já existente. Qualquer tipo de notificação deve ser gerado de maneira real.

**Padrão de Projeto Aplicado:** Observer

**Como será utilizado:**  
A classe `EmissorDeLaudo` funcionará como o sujeito (subject), enquanto `Paciente`, `NotificadorWhatsApp`, `NotificadorEmail`, entre outros, agirão como observadores. Assim que um laudo for emitido, todos os observadores serão notificados automaticamente.

**Justificativa:**  
Permite adicionar novos canais de notificação sem modificar a lógica do sistema emissor, promovendo extensibilidade e baixo acoplamento.

---

## Requisito R7 - O sistema deve permitir a realização de descontos para o custo de exames conforme política definida pelo laboratório. Inicialmente, serão concedidos descontos para convênio (15%) e desconto para idoso (8%). Outros tipos de descontos poderão surgir no futuro, como por exemplo, no mês de campanha do “Outubro Rosa” (prevenção de câncer de mama). Os novos tipos de exames a serem adicionados não devem impactar o funcionamento do código já existente.

**Padrão de Projeto Aplicado:** Strategy

**Como será utilizado:**  
A lógica de aplicação de desconto será encapsulada em objetos que implementam a interface `Desconto`, como `DescontoIdoso`, `DescontoConvenio`. O sistema aplicará dinamicamente a estratégia mais adequada para o perfil do paciente.

**Justificativa:**  
Oferece flexibilidade e reutilização ao separar regras de negócio de desconto em componentes independentes.

---


## Requisito R8 - Implementar a solução de priorização de exames usando fila de prioridade. As regras já foram indicadas anteriormente e considerar-se-á as prioridades URGENTE, POUCO URGENTE e ROTINA.

**Padrão de Projeto Aplicado:** Priority Queue

**Como será utilizado:**  
Os exames serão armazenados em uma fila de prioridade que organiza automaticamente a ordem de processamento com base na prioridade associada a cada exame (Urgente, Pouco Urgente, Rotina). A fila garante que exames mais urgentes sejam processados primeiro, simplificando a lógica de controle e evitando condicionais complexas.

**Justificativa:**  
A fila de prioridade oferece uma maneira eficiente e natural de gerenciar o atendimento dos exames conforme sua urgência, centralizando a lógica de ordenação e facilitando a manutenção, evolução e legibilidade do código.

### ou

### Requisito R8 - Implementar a solução de priorização de exames usando fila de prioridade. As regras já foram indicadas anteriormente e considerar-se-á as prioridades URGENTE, POUCO URGENTE e ROTINA.

**Padrão de Projeto Aplicado:** State

**Como será utilizado:**  
Cada exame possuirá um estado que representa sua prioridade atual (`Urgente`, `PoucoUrgente`, `Rotina`). O comportamento do exame no momento do processamento será determinado pelo estado atual.

**Justificativa:**  
Evita uso de condicionais espalhadas no código e centraliza o comportamento por prioridade, facilitando manutenção e extensão.

---

## Requisito R9 - Implementar o programa principal que simule a execução da aplicação e atendimento de todos os requisitos funcionais.

**Padrão de Projeto Aplicado:** Facade

**Como será utilizado:**  
A classe `SistemaDeExames` atuará como uma fachada para o sistema, unificando as operações de criação de exames, validações, geração de laudos, notificações e descontos em uma única interface de alto nível.

**Justificativa:**  
Reduz a complexidade de uso do sistema, facilitando a integração com outras camadas, como interfaces gráficas, APIs, ou testes automatizados.

---

## Requisito R10 - Gerenciamento de versões das observações médicas em um exame

**Descrição do Requisito:**  
Durante a elaboração de um laudo, o sistema deve permitir que médicos adicionem ou editem observações clínicas sobre o exame. Para garantir segurança e controle de versões, o sistema deve armazenar automaticamente o histórico dessas observações. O médico deve ser capaz de desfazer alterações e restaurar versões anteriores das observações antes da emissão final do laudo.

**Padrão de Projeto Aplicado:** Memento

**Como será utilizado:**  
A classe `HistoricoLaudo` armazenará versões anteriores das observações do laudo. O sistema permitirá restaurar uma versão anterior a qualquer momento antes da emissão final.

**Justificativa:**  
Garante controle de histórico e possibilidade de desfazer ações, essencial em ambientes sensíveis como registros médicos.

---

## Conclusão

Este projeto demonstrou como o uso de padrões de projeto clássicos pode proporcionar uma arquitetura sólida, modular e preparada para futuras expansões. Cada requisito foi cuidadosamente mapeado a uma solução orientada a objeto, garantindo clareza, reutilização e facilidade de manutenção do código.

