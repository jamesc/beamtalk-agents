# agents

Agent backends for Beamtalk: `CodexClient` and `ClaudeBackend` subprocess
clients behind the `AgentBackend` seam, with `CodexError`/`ClaudeError`
taxonomies on a vendored `TaggedError` base.

## Building

```bash
just build
```

## Testing

```bash
just test
```

Unit tests run everywhere. Integration tests need the real CLIs and skip
without them: `codex` for `CodexClientIntegrationTest`, `claude` plus
`ANTHROPIC_API_KEY` for `ClaudeBackendIntegrationTest`.
