# Aurora Studio

> Ambiente de produção audiovisual assistida por inteligência artificial.

**Estado:** exploração tecnológica / backlog P3 (prioridade proposta), 26/11/2026. Escopo exploratório, sem implementação.

## Visão
Construir um ambiente de criação, preparação, edição e produção audiovisual com IA, explorando ferramentas abertas para facilitar produção de vídeos curtos e conteúdo técnico. Studio não é a própria operação de conteúdo, nem pressupõe publicação automática. Validar manualmente processos antes de automatizá-los.

## Referência inicial
[Lemo-Opuscar](https://lemomo-ai.github.io/lemo-opuscar/) foi levantado como referência e objeto de estudo; há interesse em preservar e estudar seu código via fork. Funcionamento, licença, maturidade, custos e requisitos ainda não foram verificados. Um fork não garante direitos de uso/distribuição nem continuidade de serviços externos. Investigar documentação, origem, dependências, licença de código/modelos/assets, hardware, execução local, pontos reutilizáveis e alternativas.

## Escopo candidato (não fechado)
- Workspace de projetos de mídia, importação, biblioteca de fontes/assets, timeline/prévia, painel de sugestões e fila de renderização.
- Explorar transcrição, identificação de trechos e sugestões de cortes, com edição e revisão humanas.
- Legendas editáveis, proporções e presets de exportação de vídeos curtos/longos.
- Assistência a roteiro, títulos e metadados; sem postagem automática no MVP.
- Preservar originais e versões; fila, progresso, cancelamento, prévia e exportação.
- Priorizar processamento local quando viável; medir qualidade, velocidade e consumo. Provedores externos apenas com consentimento.

## Fronteiras Aurora
Studio é dono da experiência e do estado dos projetos audiovisuais. AI fornece inferência, catálogo e agentes; Nexus fornece conhecimento/contexto autorizado; Flow executa workflows genéricos autorizados; Control observa recursos; Central dá acesso. Lens captura/transmite vídeo, Transcriptions captura voz/notas. Evitar duplicação. Prova de conceito independente desses serviços.

## Arquitetura candidata
Avaliar Tauri 2 + React/TypeScript/Rust para desktop, FFmpeg/ffprobe para processamento, workers isolados com cancelamento e limites; adaptadores de IA separados do motor de mídia. Avaliar codecs, formatos, aceleração de GPU, transcrição local e licença de distribuição. Stack final após spike e benchmark reproduzível.

## Segurança e direitos
Validar arquivos/paths, não executar comandos vindos de mídia/metadados, argumentos estruturados em subprocessos, isolamento, limites de memória/disco/tempo, limpeza de temporários. Preservar originais, não sobrescrever sem confirmação. Usar conteúdo próprio/licenciado, verificar licenças de dependências, modelos e assets, respeitar consentimento de voz/imagem, direitos autorais e regras das plataformas. Não enviar mídia a terceiros ou publicar sem aprovação. Não registrar segredos/dados privados.

## Roadmap proposto
- Pesquisa 00: estudar Lemo-Opuscar e alternativas, inventariar licenças/dependências, executar isoladamente e documentar viabilidade.
- Ciclo 01: prova de conceito local: importar vídeo autorizado, inspecionar, selecionar trecho manual e exportar.
- Ciclo 02: transcrição e legendas revisáveis.
- Ciclo 03: sugestões de cortes e revisão visual.
- Ciclo 04: presets, fila e cancelamento.
- Ciclo 05: integrações opcionais AI/Nexus/Flow e avaliação de qualidade/custo.
- Ciclo 06: segurança, estabilidade, distribuição e decisões por uso real.

## Validação
Clipes próprios/licenciados; arquivos válidos/corrompidos, formatos e duração, falta de espaço, cancelamento, retomada, qualidade de cortes/legendas, desempenho CPU/GPU. Documentar evidências e limitações. Nenhuma adoção de tecnologia ou reutilização aprovada antes da pesquisa.
