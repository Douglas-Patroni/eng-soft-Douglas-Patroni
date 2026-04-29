# Cenário 1: Logística de E-commerce Global

```mermaid
flowchart TD
  subgraph SC["Sistema de Logística"]
  UC1["Gerenciar despacho de mercadoria"]
  UC2["Consultar estoque interno"]
  UC3["Consultar status da transportadora"]
  UC4["Enviar dados para a Receita Federal"]
end
  Operador["Operador de Despacho"]
  Estoque["Sistema de Estoque Interno"]
  Transportadora["Sistema da Transportadora"]
  Receita["Sistema da Receita Federal"]

  Operador --> UC1

  UC1 -->|<<include>>| UC2
  UC1 -->|<<include>>| UC3
  UC1 -->|<<include>>| UC4

  UC2 -.->|"consulta"| Estoque
  UC3 -.->|"consulta"| Transportadora
  UC4 -.->|"consulta"| Receita
```
---
# Cenário 2: Totem de Autoatendimento em Fast-Food

```mermaid
flowchart TD
  subgraph SC["Sistema de Autoatendimento"]
  UC1["Fazer pedido"]
  UC2["Realizar Pagamento"]
  UC3["Enviar pedido para cozinha"]
  UC4["Atualizar fidelidade"]
end
  Cliente["Cliente"]
  Cozinheiro["Cozinheiro"]

  Cliente --> UC1
  Cliente --> UC2
  Cozinheiro --> UC3

  UC1 -->|<<include>>| UC2
  UC1 -->|<<include>>| UC3
  UC1 -->|<<include>>| UC4
```
---
# Cenário 3: Sistema de Telemedicina (Monitoramento)

```mermaid
sequenceDiagram
  participant Sensor as ensor Cardíaco
  participant App as App Mobile
  participant Servidor as Servidor
  participant Medico as Tablet do Médico

  Sensor->>App: 1. Envia dados cardíacos
  App->>App: 2. Detecta alteração relevante
  App->>Servidor: 3. Solicita histórico do paciente
  Servidor-->>App: 4. Retorna histórico
  Servidor->>Medico: 5. Dispara alerta imediato
```
---
# Cenário 4: Sistema de Controle de Acesso Inteligente

```mermaid
flowchart TD
  subgraph Usuario["Usuário"]
    A1["Aproximar celular da fechadura"]
  end
  subgraph App["Aplicativo"]
    B1["Ler identificação do usuário"]
    B2{"Verificar reserva"}
    B3["Gerar comando de destrancar"]
    B4["Registrar acesso"]
    B5["Exibir mensagem: Acesso negado"]
  end
  subgraph Hardware["Fechadura Inteligente"]
    C1["Receber comando"]
    C2["Destrancar porta"]
  end

A1 --> B1
B1 --> B2

B2 -->|Sim| B3
B3 --> C1
C1 --> C2
C2 --> B4

B2 -->|Não| B5
B5 --> A1
```
---
# Cenário 5: Marketplace de Serviços Domésticos

```mermaid
flowchart TD
  subgraph SC["Sistema de Marketplace de Serviços Domésticos"]
  UC1["Buscar profissionais"]
  UC2["Filtrar por localização e disponibilidade"]
  UC3["Contratar serviço"]
  UC4["Realizar pagamento"]
  UC5["Avaliar profissional"]
  UC6["Realizar pagamento"]
end
  Cliente["Cliente"]
  Profissional["Profissional"]

  Cliente --> UC1
  Cliente --> UC3
  Cliente --> UC5
  Profissional --> UC6

  UC1 -->|<<include>>| UC2
  UC3 -->|<<include>>| UC4
  UC3 -->|<<include>>| UC6

  UC6 -.->|<<extend>>| UC5
```
