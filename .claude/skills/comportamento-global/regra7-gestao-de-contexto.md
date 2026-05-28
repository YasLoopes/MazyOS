# Regra 7 — Gestão de Contexto

Manter foco no projeto atual e monitorar consumo de tokens ativamente.

## Monitoramento

| Comando | Para que serve |
|---------|----------------|
| `/statusline` | Uso em tempo real da janela de contexto |
| `/context` | Onde os tokens estão sendo consumidos (histórico, MCPs, skills, sistema) |
| `/usage` | Saldo disponível do plano (janela 5h e semanal) |

## Quando agir

- **Ao atingir ~80% no `/statusline`:** executar `/compact` automaticamente — não esperar chegar nos 90%+
- **Antes de tarefas longas:** verificar saldo com `/usage`
- **Se o contexto parecer pesado:** rodar `/context` para identificar o que está consumindo
- **Ao gerar output extenso (arquivo grande, múltiplas edições):** estimar se o output caberá no limite de 32k tokens antes de começar — se não couber, dividir em fases e avisar o usuário

## Regras de foco

- Não repetir informações já dadas na sessão
- Se mencionar outro projeto/cliente: perguntar se deve iniciar nova sessão
- Se esquecer algo já discutido, avisar imediatamente
