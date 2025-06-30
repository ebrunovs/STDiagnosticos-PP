# Sistema de Gerenciamento de Exames - IF Diagnósticos

Este projeto visa atender às necessidades da IF Diagnósticos, oferecendo um sistema flexível, reutilizável e de fácil manutenção para gerenciamento de exames médicos, emissão de laudos e comunicação com pacientes. A solução foi desenvolvida com foco na aplicação de padrões de projeto para garantir extensibilidade e desacoplamento entre os componentes do sistema.

## Estrutura da Solução

A arquitetura do sistema foi construída com base em diversos padrões de projeto. Cada requisito funcional foi analisado individualmente e resolvido com um ou mais padrões que melhor se aplicam ao cenário descrito.

---

## Diagrama de Classes
![Diagrama UML](https://uml.planttext.com/plantuml/png/lLZ9RkGs4BttLn1pcMwCDHyW9COuNYODU8kNvD90m9ReDX6952ZAiJCpNvD3FY389LV_M8eKLpNbbf59V33KLQ-AjQke3wt4GdPrDPEyGPAZDPUIrwYaWXIISZQRlVtsXR_PMtHDsQOYahCSVIG2broWag3bKRj3ii75BtX3q1kdOCNcWORpvxzh8lZY3VeqGwYeSDlQ0yuxnJb-n3NHJ8Go18v8MY3Au84L94zW3P9foe7iS9K3NchoExGXScc4vujHSOKJs90LhbVmPVPbTwHES26vU49dHDxpCaTQw-GmnT8GgrxSn0UlMoa0OG8LnmPqKC8a1ENIF1bV1C4L_GqB3LVUF71QQdTSoBydDTy8N6D7kQtWfBRbJD7lg6TS4KM5008DY4uIPLsJVTv7Def31KD-e2TcZVXf8_F9U5K86hXajQPyCfAx1CSyVwLuuDUAdU4D8r2nhz0JnjJw7CR7q18HVXczowwa6CX5mSyocwK9dV2TeEK6ol4KToLl4K5tNDHOyidDq2k09j0Q86OdlO9qD_GWsmtchDpAQAxX4UM1ZxaYyNLBn0CkC4XSk6V3V83-ATMSoD6FzZ6kDQrznNmpa4T9M6aOGvXB73QjyI8wdRY130Z1Z2BY3XSaSjdrYvveXnn0G4rFWSkZ4zyzDsUdxiSD7ARF00HwtpNleKu6SLNu4PQMJl96aXYskZ5Sq-TXulPMJ6KjJ9SYfNArC3KuUo5ZAnRqvrS-T4Vw_yUZqxNqNne06aT3ZRAI_yhKq0dJxYL60xLBS8UR8-9Mtg9ubWrBEUBtMlmRBScCXaaIuQA6SX_C9QDWV3Lbp1xUOmgPkLCJlk6ifMjQKVaqTSYEYCFKxGrx_kFvTpjn_OZnHjlvqfikveeAHNA66wY2DUSLmSn0MY8l1N-aDP-FLCtsJEgv4BwWW5BCmLgI4hCZA9pXQGtRI0TLBcU3h3MzKrEIrPS30RVFkQHtK9KGtx-cxuTM7j8JAzZAa2cyC4NCI8XvJLWB-keSNKi1ctaoz3_TOzaUDCsAsQD0sUjqMLNNTViLj1pNc5R_GW_yI_faq-r31iYXoKdGjaK9c7-_chtS9GINqELGSyAZv-68LKqHxYp0EQMj_4PFd7t3gVHwPJXwmknRRzs1QfH5XZjE5WomYEW6-Cwh8GnfIJPFEJeYRG4BnlG5puf2DJlPhKAs70lsDm1S5Ls5XGMeeQ86IicxTKKMzY4kQWjUCTY57WYZFC5QGa3rThADjlaTMXM1jVmeqjUpYhjbkysr7E3pr5cwUffAbVn4z-F3L44arFOtIbSJ5X5n4dVc2LLoAIWNy5v1FtIaWvNYX5PuQfd4ib0iIbXzFOWkntrC5Ml5UWcOpu3kGTizrz-zeWq79hcLov7NiJ2YV0qrQTzWmqiROLqTo9ZpRgy-7f_V7EldoulRmukVGyhLnSto_C1g63KzxD5HaCge9q_yKg4TNRfMW-l2DKmHKazEJQz3Nz7M7Che-Kym8Kg8OO1TN2zWFZQm472eO2fjBhQ_OEmXIPk-o7RaQC_rpNQ_BCAxtZj4QYffQi5DNnhTCclIb7B8PIXSHTCmzt5cGeRE2BpEfB-IlcvNCDAGd4WyoevVJztyaUgwPb-VuSSAeqzLlXSpHFUfgPMu4-ezd00jub7i-R2azmXdXD9J3gtO47ciwSe4nma_-K3nGi0BK9XmhDTftvHRrktReiJL0rHaVz2O6v6p1aiPZ1QYFnQEX4YR6bYMHHS45mLrdKvw4hp61_Y1qgIughWFX9NgG_0_)

# Requisitos Funcionais e Padrões Aplicados

---

## Requisito R2 - Gerar o número sequencial do exame, sem repetição

**Padrão de Projeto Aplicado:** Singleton

**Como será utilizado:**  
Será criada a classe `GeradorSequencial`, responsável pela lógica de geração de identificadores únicos. Essa classe seguirá o padrão Singleton, garantindo que apenas uma instância exista durante toda a execução da aplicação.

**Justificativa:**  
Garante unicidade na geração dos números de exame, evitando conflitos, duplicações ou inconsistências, especialmente em ambientes concorrentes.

---

## Requisito R3 - Emitir laudo dos seguintes exames: Hemograma, Ultrassonografia e Ressonância Magnética. Outros tipos poderão ser adicionados futuramente, como Tomografia, sem impacto no código já existente.

**Padrão de Projeto Aplicado:** Factory Method

**Como será utilizado:**  
Cada tipo de exame terá sua própria implementação e será instanciado por fábricas concretas que herdam de uma interface comum, `ExameFactory`. O sistema chamará os métodos da fábrica sem conhecer as classes concretas dos exames, como `Hemograma`, `Ultrassonografia`, etc.

**Justificativa:**  
Desacopla a lógica de criação dos objetos, permitindo adicionar novos tipos de exame sem modificar o código existente. Atende ao princípio Open/Closed (aberto para extensão, fechado para modificação).

---

## Requisito R4 - Gerar laudos em diferentes formatos: Texto, HTML e PDF. Novos formatos, como JSON, poderão ser adicionados sem afetar o código existente.

**Padrão de Projeto Aplicado:** Bridge

**Como será utilizado:**  
Será criada a abstração `Laudo`, que conterá uma referência a um objeto da interface `Formato`. As classes concretas de formato (`FormatoPDF`, `FormatoHTML`, `FormatoTexto`) implementarão a lógica de geração no formato específico.

**Justificativa:**  
Permite variar independentemente o conteúdo dos laudos e seu formato de saída. Facilita a adição de novos formatos sem alteração nas abstrações principais.

---

## Requisito R5 - Adicionar regras de validação específicas para cada tipo de exame, de forma extensível.

**Padrão de Projeto Aplicado:** Chain of Responsibility

**Como será utilizado:**  
Cada regra de validação será encapsulada em uma classe que implementa a interface `Validador`. Esses validadores serão encadeados em uma cadeia, permitindo que cada um execute sua verificação e repasse o controle ao próximo.

**Justificativa:**  
Permite uma estrutura modular e flexível para validações. Novas regras podem ser adicionadas, removidas ou reorganizadas sem impactar o fluxo principal ou os validadores existentes.

---

## Requisito R6 - Notificar o paciente por WhatsApp quando um laudo for emitido. Novos canais, como SMS ou E-mail, podem ser adicionados sem impacto no funcionamento atual.

**Padrão de Projeto Aplicado:** Observer

**Como será utilizado:**  
A classe `EmissorDeLaudo` atuará como sujeito (Subject), notificando observadores como `NotificadorWhatsApp`, `NotificadorEmail`, entre outros. Ao emitir um laudo, todos os observadores registrados são automaticamente notificados.

**Justificativa:**  
Facilita a adição de novos mecanismos de notificação sem alterar a lógica de emissão, promovendo baixo acoplamento e alta extensibilidade.

---

## Requisito R7 - Aplicar descontos no custo do exame conforme políticas do laboratório.

**Padrão de Projeto Aplicado:** Strategy

**Como será utilizado:**  
A lógica de desconto será encapsulada em classes concretas que implementam a interface `Desconto`, como `DescontoConvenio` e `DescontoIdoso`. A classe responsável aplicará dinamicamente a estratégia adequada com base no perfil do paciente.

**Justificativa:**  
Encapsula políticas de desconto em componentes independentes e reutilizáveis. Facilita a manutenção e extensão da lógica de negócio sem impactar o sistema principal.

---

## Requisito R8 - Priorizar exames com base em níveis de urgência: URGENTE, POUCO URGENTE e ROTINA.

### Opção 1 - Priority Queue

**Padrão de Projeto Aplicado:** Priority Queue

**Como será utilizado:**  
Exames serão inseridos em uma estrutura de fila de prioridade (`PriorityQueue<Exame>`) com base em sua urgência. A fila garante o atendimento de exames mais críticos primeiro, sem necessidade de lógica condicional dispersa.

**Justificativa:**  
Abstrai a ordenação dos exames de acordo com a prioridade, tornando o sistema mais eficiente, legível e de fácil manutenção.

### Opção 2 - State

**Padrão de Projeto Aplicado:** State

**Como será utilizado:**  
Cada exame terá um estado associado (`EstadoPrioridade`) representando sua urgência. A lógica de comportamento durante o processamento dependerá do estado atual: `Urgente`, `PoucoUrgente`, ou `Rotina`.

**Justificativa:**  
Encapsula comportamentos específicos por prioridade, evitando condicionais espalhadas e centralizando a lógica de decisão.

> 💡 *Escolha entre Priority Queue (quando a preocupação for com ordenação de atendimento) ou State (quando há mudança de comportamento conforme prioridade).*

---

## Requisito R9 - Implementar o programa principal que simule a execução da aplicação e os requisitos funcionais.

**Padrão de Projeto Aplicado:** Facade

**Como será utilizado:**  
A classe `SistemaDeExames` atuará como uma fachada, unificando funcionalidades como criação de exames, aplicação de descontos, geração de laudos e notificações. Outras camadas do sistema (ex: UI ou testes) interagirão apenas com essa classe.

**Justificativa:**  
Fornece uma interface simplificada para operações complexas, reduzindo o acoplamento entre subsistemas e facilitando integrações.

---

## Requisito R10 - Controle de versões das observações médicas nos exames

**Padrão de Projeto Aplicado:** Memento

**Como será utilizado:**  
A classe `HistoricoLaudo` armazenará versões anteriores das observações feitas durante a edição do laudo. A classe `Laudo` poderá restaurar qualquer versão salva antes da finalização.

**Justificativa:**  
Oferece suporte à reversão de alterações e versionamento, o que é essencial em sistemas sensíveis como laudos médicos.

---

## Conclusão

Este projeto demonstra como a aplicação adequada de padrões de projeto proporciona uma arquitetura robusta, extensível e de fácil manutenção. Cada requisito foi implementado com foco em boas práticas de orientação a objetos, favorecendo reutilização, clareza e desacoplamento.

