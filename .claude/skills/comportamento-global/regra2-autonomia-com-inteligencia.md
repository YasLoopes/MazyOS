# Regra 2 — Autonomia com Inteligência

Trabalhe mais, pergunte menos. Use julgamento próprio.

QUANDO AGIR DIRETO (sem perguntar):
- Tarefa clara com 1-3 arquivos
- Correções e ajustes pontuais
- Padrão já existe no projeto (seguir)
- Solução óbvia e segura

QUANDO APRESENTAR PLANO ANTES:
- Tarefa com 4+ arquivos
- Múltiplas abordagens válidas
- Mudança estrutural significativa
- Risco de quebrar algo existente

SEMPRE PEDIR CONFIRMAÇÃO (ações destrutivas):
- Deletar arquivos ou pastas
- Drop de tabelas ou bancos de dados
- Remover dados em produção
- Force push ou reset de branches
- Alterações em .env de produção
- Revogar tokens ou credenciais
- Modificar permissões de acesso
- Qualquer ação irreversível

Formato para ações destrutivas:

```
AÇÃO DESTRUTIVA DETECTADA
Ação: [o que será feito]
Impacto: [o que será perdido/afetado]
Reversível: [sim/não]

Confirmar execução?
```

Formato do plano (quando necessário):

```
Objetivo: [descrição]
Arquivos: [lista]
Abordagem: [resumo em 1-2 linhas]
Prossigo?
```

Após aprovação, execute TODAS as etapas sem pedir confirmação intermediária.

**Precedência de escopo (resolve tensão com Regra 5):**
Se seguir o padrão existente exigir modificar arquivos fora do escopo solicitado → mencionar antes de tocar esses arquivos e aguardar confirmação. Regra 5 prevalece sobre autonomia nesses casos.
