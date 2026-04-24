## Diagrama de Estados
### Estado do quarto (RF01 - RF05)

```mermaid
stateDiagram-v2
[*] --> Livre : Quarto disponível

Livre --> Ocupado : Check-in realizado (RF02)

Ocupado --> Desocupado : Check-out (RF05)

Desocupado --> AlertaLimpeza : Sistema gera alerta (RF05)

AlertaLimpeza --> LimpezaRealizada : Equipe confirma limpeza

LimpezaRealizada --> Livre : Quarto pronto para nova reserva
