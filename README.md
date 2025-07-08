# Sistema de Gerenciamento de Exames - IF Diagnósticos

Este projeto visa atender às necessidades da IF Diagnósticos, oferecendo um sistema flexível, reutilizável e de fácil manutenção para gerenciamento de exames médicos, emissão de laudos e comunicação com pacientes. A solução foi desenvolvida com foco na aplicação de padrões de projeto para garantir extensibilidade e desacoplamento entre os componentes do sistema.

## Integrantes do Grupo

| Nome               | Matrícula     |
|--------------------|---------------|
| Alessandro Rodrigues de Souza Júnior | 20231370009 |
| Bruno Vinicius de Araujo Eneas | 20231370015 |
| Caio Batista da Silva Soares | 20231370010 |
| Douglas Emerson Ferreira Carneiro | 20231370002 |


## Estrutura da Solução

A arquitetura do sistema foi construída com base em diversos padrões de projeto. Cada requisito funcional foi analisado individualmente e resolvido com um ou mais padrões que melhor se aplicam ao cenário descrito.

---

## Diagrama de Classes
![Diagrama UML](https://uml.planttext.com/plantuml/png/hLZRRkCs47qFa7yWzgKs6kS3l6smsLns3UJMNDeN0mKjqGvHYHGeoarsww_fGp-Ww4jVysCTNaL9rAwqwG8BEvoPmndEyCpGxqg9XQpoR7yl8sk994U2RXubIgaWYQISxU_jxtttunV-WHZTKRR9YEHiZZuGWLCkK4hGuhJygcs1az_mXg0t7cB99W76rSk_EH5y-WPztjz3ACbmMRezhYebEdl2EJ5IX6O80f8qGPJ15vQGUKJPgJAzT2mhdCt1G9hrxz66o8Krdqpx0PIYm7PTALg8tVxURi2PdJnYoX1VerjI5foLT4KpAf-7drWF09pVppYZANxvw-LFVt3W6n5hd11aXEfuFxiujdf9JDHoEKUNk81eLfnd13EdKn9v8_WJpVbawn3cDHWOR3bDRVm8gVzuLKg14rbhlSSbyPag35m0ydRyPe7xpg8lYfqgPLT21Yl1VCa-afnl1CxnuFFOHN4W3ILdK3NqjKWF6PoR0bD-hSV1gOzOSEYmAWx_E6hcegKSH314lUqcEapvxonYLTkfiflDEWgxGInpINB291JCzQeaOgiA_1yoWcAiFLoG1a2JMwm80gmvHP8djUsT541IBXU9e5XOI7NxQqExw1G50IwfW2acUKHhsYdDMcN9h5BjYi9AExu0OvrfWNAa5ZLWFz9ISa4JG8t5Q82Xg2v0xuUEcqV-Qk9iYuNThJUWHjnMcRAKAa86AkexBkjmu9ygbiY1AAruG7mswpDemKRjXzRYEV0Q5yzGa_AHftEa-yA8McpQGqaQ05UBdZfDxbezBk4ftV2WPysWLPO9XpWX-LYIpVCSdRPMd2PmY2BJm1QSed16a9eR-wtHu4xiRlrzK12upfyWqMfnqcBdGf020up3dapVjks0kHEIKdkLl7XDMGFN2t2HqGGB5-74XfJoQfMHgVlIlG4TelystmBIxcNgLoF7kiatW-hhuZl1h2fcGD8-XHqURok4VQ4fYzJg2V0Yb8bMy9vhilJbuO4RwR66tIpr6xTCUxCn62685AW3RnY1ON8WbFfen-2EApoKGA_lv7lKUxsBsmMMXa0KwrdPC9PxBsYw0Lwum1Nq1aJGceiSIpw2w0m449p6W0CyDn0zJ6UqFDFP_UREIejzorAX13bGQzmpUTXY0kxh39CkiIIdaef927hGtjxtDZU8TRktzZ2Sks1s82orWewUhm1iA-3Bwl4AQ1ir1_xmwEgPtr8xQ5LcR0Z6zthRczFpW3_lBo_gl-xLK6HqGSlDY-qyAPi-cKQ82vNOEApwUTlGI6Pgsfm5DDLSRcQ_AQk7qNbT4mj6uLYpeNV3u1CefIikwHhIC7OUTGXmEPeGtKUR3QRnQcFM1kPAmaf0pDtirvVDNnwnB8-BOidSVW0u6i-XtUNb_mDqbcEQlGvAVKIZS-LL7w1IRRiUr-hw5TCBBejjoy5GhOSwErFhEZroeanJgXNfwZmAOl6rt_R9xp4BAx-nQg_9i2hkpejZVhEnnb30thfRk-r1jAxW16T9bOqVv9p-aW61RGcZF2PRmFbQAkaQk4p6fkGMHB-gBXBTMHLBnQ3glXkRddLGGvyRE8MsjF2d2kLn1wL3SZpgqG4ekXUlE3ZvyhUWhP_Mh0JUHH2-qQ_pLNAOkwbqyq_ttN2092rCTAw5mj1A0ItLxj_uxmV-nT9zgKmRFTrrPbtMpVOS7m-cyxfv-klKZKebfJrdzUcDkb8cIFcCVgf81RwUqsn4ZfhMa2jbhdu9RJuGJRQKRCdgKrqoerMd3CERcyB4O5D61gJ63pa5sQW71JmcgFc1iptj4bRbWQ7RzU7smzdL_Pdvu-RwuUJwryRIxVNzukhuA-dHvzuNdpBgZLtTnNhPtx9tC25LUVOV)

# Requisitos Funcionais e Padrões Aplicados

## Tabela Resumo: Requisitos e Padrões de Projeto

| Requisito | Descrição resumida                                                      | Padrão de Projeto Aplicado |
|-----------|-------------------------------------------------------------------------|-----------------------------|
| R2        | Geração de número sequencial único para exames                         | Singleton                   |
| R3        | Criação de laudos para diferentes tipos de exame                        | Factory Method              |
| R4        | Geração de laudos em múltiplos formatos (texto, HTML, PDF, etc.)       | Bridge                      |
| R5        | Validação extensível de exames                                          | Chain of Responsibility     |
| R6        | Notificação ao paciente (ex: WhatsApp, E-mail)                          | Observer                    |
| R7        | Aplicação de políticas de desconto (convênio, idoso, etc.)             | Strategy                    |
| R8        | Priorização de exames por urgência (URGENTE, POUCO URGENTE, ROTINA)    | Priority Queue **ou** State|
| R9        | Execução centralizada das funcionalidades do sistema                   | Facade                      |
| R10       | Versionamento das observações do laudo                                  | Memento                     |

---

## Requisito R2 - Gerar o número sequencial do exame, sem repetição

**Padrão de Projeto Aplicado:** Singleton

**Como será utilizado:**  
Será criada a classe `GeradorSequencial`, responsável pela lógica de geração de identificadores únicos. Essa classe seguirá o padrão Singleton, garantindo que apenas uma instância exista durante toda a execução da aplicação.

**Justificativa:**  
Garante unicidade na geração dos números de exame, evitando conflitos, duplicações ou inconsistências, especialmente em ambientes concorrentes.

---

## Requisito R3 - Emitir laudo dos seguintes exames: Hemograma, Ultrassonografia e Ressonância Magnética. Outros tipos de exames poderão surgir no futuro, como por exemplo a Tomografia. Os novos tipos de exames a serem adicionados não devem impactar o funcionamento do código já existente.

**Padrão de Projeto Aplicado:** Factory Method

**Como será utilizado:**  
Cada tipo de exame terá sua própria implementação e será instanciado por fábricas concretas que herdam de uma interface comum, `ExameFactory`. O sistema chamará os métodos da fábrica sem conhecer as classes concretas dos exames, como `Hemograma`, `Ultrassonografia`, etc.

**Justificativa:**  
Desacopla a lógica de criação dos objetos, permitindo adicionar novos tipos de exame sem modificar o código existente. Atende ao princípio Open/Closed (aberto para extensão, fechado para modificação).

---

## Requisito R4 - Gerar laudos para diferentes exames, inicialmente nos formatos texto, HTML e PDF. Outros tipos de formato poderão surgir no futuro, como por exemplo o JSON. Os novos formatos de exames a serem adicionados não devem impactar o funcionamento do código já existente. Qualquer tipo de laudo deve ser gerado em seu formato específico, inclusive em PDF (utilize a API de sua preferência)

**Padrão de Projeto Aplicado:** Bridge

**Como será utilizado:**  
Será criada a abstração `Laudo`, que conterá uma referência a um objeto da interface `Formato`. As classes concretas de formato (`FormatoPDF`, `FormatoHTML`, `FormatoTexto`) implementarão a lógica de geração no formato específico.

**Justificativa:**  
Permite variar independentemente o conteúdo dos laudos e seu formato de saída. Facilita a adição de novos formatos sem alteração nas abstrações principais.

---

## Requisito R5 - Adicionar as regras de validação de cada exame, de maneira extensível. A validação do Hemograma só analisa se os valores medidos não excedem 50% do valor máximo e do valor mínimo. Por exemplo, se para Hemoglobina os valores de referência são de 13.0 a 18.0 milhões/dl, os extremos não podem exceder 6.5 e 27 milhões/dl. No caso de uma ressonância magnética, há diferentes regras de validação que devem ser verificadas, não importando a ordem, como: (a) verificar a presença de implantes gerais.


**Padrão de Projeto Aplicado:** Chain of Responsibility

**Como será utilizado:**  
Cada regra de validação será encapsulada em uma classe que implementa a interface `Validador`. Esses validadores serão encadeados em uma cadeia, permitindo que cada um execute sua verificação e repasse o controle ao próximo.

**Justificativa:**  
Permite uma estrutura modular e flexível para validações. Novas regras podem ser adicionadas, removidas ou reorganizadas sem impactar o fluxo principal ou os validadores existentes.

---

## Requisito R6 - Notificar o paciente quando um laudo for emitido (inserido no sistema), por WhatsApp. Outros mecanismos de notificação serão adicionados futuramente (e.g. SMS ou E-mail) e não devem impactar o funcionamento do código já existente. Qualquer tipo de notificação deve ser gerado de maneira real.

**Padrão de Projeto Aplicado:** Observer

**Como será utilizado:**  
A classe `EmissorDeLaudo` atuará como sujeito (Subject), notificando observadores como `NotificadorWhatsApp`, `NotificadorEmail`, entre outros. Ao emitir um laudo, todos os observadores registrados são automaticamente notificados.

**Justificativa:**  
Facilita a adição de novos mecanismos de notificação sem alterar a lógica de emissão, promovendo baixo acoplamento e alta extensibilidade.

---

## Requisito R7 - O sistema deve permitir a realização de descontos para o custo de exames conforme política definida pelo laboratório. Inicialmente, serão concedidos descontos para convênio (15%) e desconto para idoso (8%). Outros tipos de descontos poderão surgir no futuro, como por exemplo, no mês de campanha do “Outubro Rosa” (prevenção de câncer de mama). Os novos tipos de exames a serem adicionados não devem impactar o funcionamento do código já existente.

**Padrão de Projeto Aplicado:** Strategy

**Como será utilizado:**  
A lógica de desconto será encapsulada em classes concretas que implementam a interface `Desconto`, como `DescontoConvenio` e `DescontoIdoso`. A classe responsável aplicará dinamicamente a estratégia adequada com base no perfil do paciente.

**Justificativa:**  
Encapsula políticas de desconto em componentes independentes e reutilizáveis. Facilita a manutenção e extensão da lógica de negócio sem impactar o sistema principal.

---

## Requisito R8 - Implementar a solução de priorização de exames usando fila de prioridade. As regras já foram indicadas anteriormente e considerar-se-á as prioridades URGENTE, POUCO URGENTE e ROTINA.

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

---

## Requisito R9 - Implementar o programa principal que simule a execução da aplicação e atendimento de todos os requisitos funcionais.

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

