# GenLayer Consensus Spinner

An original animated loading spinner for the GenLayer Portal.

## Concept

Built directly from GenLayer's own consensus mechanism, Optimistic Democracy: a randomly selected leader proposes a state, independent validators (each connected to a different LLM) evaluate it asynchronously, and when a majority agrees, the state is finalized.

The spinner mirrors this:

- **Five validator nodes** orbit a fixed core, each pulsing on its own independent rhythm (different duration, easing, and phase) — never perfectly synced, since real validators don't think in lockstep.
- **One larger node** represents the randomly selected leader.
- **A fixed core square** at the center represents the state being evaluated. It only settles/highlights once per larger cycle.
- **Thin connecting lines** flash briefly from every node to the core at that same moment — the instant of majority agreement (a Schelling point) — then fade, and the validators return to their independent rhythms.
- The whole cluster drifts in a very slow orbit around the core, giving the piece a quiet sense of motion without ever feeling mechanical.

## Brand

Color is GenLayer's official Kinetic Cobalt (`#110FFF`), with a subtle radial gradient for depth rather than a flat fill. Chosen because it holds full contrast on both light and dark surfaces, so no separate light/dark variant is needed.

## Files

- `genlayer-spinner.svg` — the spinner, SMIL-animated (works cross-browser, including as a plain `<img src>`), infinite loop.
- `preview.html` — live preview on light and dark backgrounds at multiple sizes.

## Usage

```html
<img src="genlayer-spinner.svg" width="48" height="48" alt="Loading">
```

Respects `prefers-reduced-motion`.
