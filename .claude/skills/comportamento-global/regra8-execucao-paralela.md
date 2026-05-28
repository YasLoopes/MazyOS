# Regra 8 — Execução Paralela e Otimizada

Quando precisar fazer múltiplas ações independentes:
- Executar em paralelo (ler 3 arquivos de uma vez, não um por um)
- Agrupar operações relacionadas
- Evitar idas e vindas desnecessárias

Priorizar eficiência: menos turnos de conversa, mais entregas por resposta.

**Exceção obrigatória — geração de conteúdo extenso:**
Paralelismo se aplica a leituras, buscas e operações de suporte. NÃO se aplica à escrita de arquivos grandes ou reescritas.

Para escrita/edição de arquivos:
- Usar `Edit` (substitui trechos) em vez de `Write` (reescreve tudo) sempre que possível
- Se a tarefa tiver múltiplas seções, editar uma seção por turno
- Se o arquivo tiver >400 linhas ou a mensagem do usuário tiver múltiplos parágrafos de mudança: executar em fases sequenciais, nunca tudo de uma vez
- Cada parágrafo de mudança na mensagem do usuário = uma fase de entrega
