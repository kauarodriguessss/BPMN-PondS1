![image](https://github.com/user-attachments/assets/60ce17a2-6310-4588-b5f7-0a81461705e0)# BPMN - Ponderada S1

### Introdução ao BPMN

A BPMN (Business Process Model and Notation) é uma notação padronizada para modelagem de processos de negócio. Seu principal objetivo é representar graficamente os processos de forma clara e compreensível tanto para analistas quanto para desenvolvedores, gestores e stakeholders.

A adoção da BPMN permite:

* Documentar com precisão os processos operacionais reais;
* Melhorar a comunicação entre equipe técnica e negócio;
* Identificar gargalos e oportunidades de automação;
* Alinhar tecnologia com as operações de negócio.

### Ferramenta Utilizada

A atividade original sugeria o uso da ferramenta **ARIS**, uma plataforma robusta e voltada especificamente para modelagem BPMN. Entretanto, devido à **incompatibilidade do ARIS com o sistema operacional macOS**, não foi possível sua instalação no dispositivo utilizado.

Como alternativa, foi utilizada a ferramenta **Lucidchart**, que oferece suporte completo à notação BPMN 2.0, é acessível via navegador (multiplataforma) e permite exportação em diversos formatos. Assim, atende os requisitos técnicos da modelagem com clareza e profissionalismo.

### Interpretação do Processo

A descrição fornecida representa o fluxo completo de uma compra no site **Mercado Livre**, incluindo pagamento, entrega e verificação da conformidade do produto.

Os seguintes participantes foram considerados no processo:

* Cliente
* Plataforma de pagamento (PayPal / Mercado Pago)
* Vendedor
* Correios
* Mercado Livre (intermediador e regulador)

### Elementos BPMN Utilizados

| Elemento BPMN     | Função                                                               |
| ----------------- | -------------------------------------------------------------------- |
| Evento de Início  | Dispara o início do processo (compra pelo cliente)                   |
| Tarefa            | Representa uma ação ou atividade executada por algum participante    |
| Gateway Exclusivo | Determina uma decisão no fluxo (ex: forma de pagamento, produto OK?) |
| Evento de Fim     | Conclui o processo                                                   |

### Representação Visual

![image](https://github.com/user-attachments/assets/39ad0967-e796-4dd1-9972-4144b596e10f)

> O diagrama da imagem anexada foi construído como uma **representação visual simplificada**, com o objetivo de **ir além** do solicitado na atividade. Ele resume graficamente os principais fluxos com foco em clareza e execução técnica precisa.

### Descrição do Processo (em formato BPMN textual simplificado)

```
[Início: Cliente realiza compra]
    ↓
[Escolher forma de pagamento]
    ↓
[Gateway: Método de pagamento?] -- PayPal --> [Processar pagamento com PayPal]
                               \-- Mercado Pago --> [Processar pagamento com Mercado Pago]
                                                       ↓
                                              [Vendedor posta produto]
                                                       ↓
                                       [Aguardar recebimento do produto]
                                                       ↓
                                  [Produto é entregue pelos Correios]
                                                       ↓
                            [Gateway: Cliente verifica conformidade?]
                                    |                           |
                                 Sim                          Não
                                  |                           |
     [Qualifica vendedor positivamente]     [Negociar com vendedor ou devolver o produto]
                                  |                           |
         [Libera pagamento ao vendedor]   [Restituir valor ao cliente]
                         \___________________________/
                                      ↓
                                     [Fim]
```

### Conclusão

A modelagem BPMN proposta documenta com clareza todas as etapas envolvidas na experiência de compra do cliente no Mercado Livre, desde a escolha do pagamento até a conclusão do processo com pagamento ou reembolso. A ferramenta Lucidchart permitiu criar uma representação técnica de alto nível mesmo sem o uso do ARIS, mantendo o padrão esperado para atividades de modelagem.

Com isso, a atividade não só cumpre os requisitos exigidos, como também demonstra iniciativa, profundidade e capacidade de interpretação do processo em um contexto realista de negócios online.
