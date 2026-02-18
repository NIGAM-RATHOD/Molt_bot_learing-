# Search Optimization Framework

Multi-agent search strategy for maximum information retrieval.

## Search Brain Architecture

### Brain 1: Kimi (Primary)
- **Role**: Query understanding, intent classification, synthesis
- **Strengths**: Long context, reasoning, planning
- **Decides**: Which brain to task, how to combine results

### Brain 2: GLM5 (Deep Diver)
- **Role**: Deep research, technical analysis, validation
- **Strengths**: Focused depth, structured reasoning
- **Deploy when**: Technical depth, validation needed

### Brain 3: MiniMax (Quick Scanner)
- **Role**: Rapid sampling, broad coverage, fact extraction
- **Strengths**: Speed, efficiency, breadth
- **Deploy when**: Fast overview, breadth needed

## Search Strategy Matrix

| Query Type | Primary | Diver | Scanner | Combine |
|------------|---------|-------|---------|---------|
| Fact check | Kimi | - | MiniMax | Verify |
| Deep research | Kimi | GLM5 | - | Synthesize |
| Quick overview | - | - | MiniMax | Present |
| Technical analysis | Kimi | GLM5 | MiniMax | Merge |
| Comparison | Kimi | GLM5+MiniMax | Both | Contrast |

## Execution Protocol

1. **Classify** query type
2. **Route** to appropriate brain(s)
3. **Execute** in parallel if multiple
4. **Synthesize** before responding
5. **Cache** for reuse

## Tool Priority

1. `memory_search` - Check prior knowledge (fastest)
2. `web_search` - Current info (requires API key)
3. `web_fetch` - Deep content extraction
4. `browser` - Complex/interactive sites

## Delegation Triggers

- **Question > 50 words** → Spawn Deep Diver
- **"Compare" / "vs" / "best"** → Spawn Scanner + Diver
- **Technical/coding** → Spawn Diver
- **Urgent/simple** → Handle directly

## Meta-Optimization

- Prefer cached results < 24h
- Batch parallel subagents
- Abort redundant fetch
- Summarize before extending context
