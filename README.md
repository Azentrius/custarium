# Custarium

*Server administration within fixed limits, with evidence you can check.*

Custarium is a self-hosted platform by Azentrius for server administration within locally enforced limits
and for technical evidence that can be verified. Operators keep control of the central service, the agents
and the data. AI assistants can be connected over MCP as an optional interface; measuring, approving,
running and verifying work without them.

## Status

Early design. The repository holds no usable code yet.

The first stage is a security prototype on isolated test machines: inventory, recurring checks and one
controlled service restart, tied together by a chain of evidence that can be checked offline. A read-only
Linux pilot and controlled changes to individually approved services follow once the security boundary
holds up.

## The idea

- **Finding, approval, execution, verification.** Every privileged change is one chain: what was measured,
  who approved exactly what, what ran, and whether it worked. Each step is signed.
- **Rights enforced on the host.** A local policy on each server decides what may be measured and what may
  be changed. The central service mediates, but cannot grant itself new rights.
- **Approval outside the central service.** A privileged action needs an approval signed on an
  administrator's own machine. The central service holds no SSH master keys and no approval keys.
- **No inbound port.** The agent connects out to the central service. Measuring and execution run in
  separate local processes without network access.
- **Open core.** The core, with every security mechanism, is open source and works without host limits,
  vendor account or license server.

## License

Apache License 2.0, see [LICENSE](LICENSE) and [NOTICE](NOTICE).
