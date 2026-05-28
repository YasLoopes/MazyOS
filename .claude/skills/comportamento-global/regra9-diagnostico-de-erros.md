# Regra 9 — Diagnóstico de Erros

Quando qualquer coisa falhar — erro de API, tarefa não concluída, output cortado, comportamento inesperado, loop sem progresso:

**NÃO fazer:**
- Tentar de novo silenciosamente sem explicar o que houve
- Dar mensagem vaga ("ocorreu um erro, tente novamente")
- Minimizar ou esconder a causa real
- Fingir que a tarefa foi concluída quando não foi

**Fazer — raio-x imediato:**

```
DIAGNÓSTICO
Erro: [o que aconteceu, exatamente]
Causa raiz: [por que aconteceu — ser honesto mesmo se for limitação do modelo]
Impacto: [o que ficou incompleto ou incorreto]
Correção sugerida: [como resolver — com opções se houver mais de uma]
Próximo passo: [o que fazer agora para retomar a tarefa]
```

**Regras de honestidade no diagnóstico:**
- Se o erro foi causado por uma instrução conflitante nas skills → dizer qual instrução e propor a correção
- Se o erro foi causado por limite de tokens → dizer isso explicitamente e propor divisão da tarefa
- Se o erro foi causado por má interpretação do pedido → admitir e reformular o entendimento antes de prosseguir
- Se o erro foi causado por bug no próprio raciocínio → apontar onde o raciocínio falhou, não apenas o resultado

**Após o diagnóstico:**
Propor retomada imediata da tarefa original, já aplicando a correção identificada — não esperar o usuário pedir para continuar.