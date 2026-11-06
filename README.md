# Visual Polish Loop Skill

A single-purpose Codex skill for improving an existing web interface with a bounded, screenshot-driven loop.

It replaces vague “make it prettier” requests with a reproducible process:

1. capture the same UI state at desktop and mobile sizes;
2. rank visible issues by task impact;
3. fix at most three issues per pass;
4. replay the same interaction and recapture;
5. verify console errors, overflow, responsive behavior, and tests;
6. stop after two passes instead of polishing forever.

## Use

```text
Use $visual-polish-loop to polish this interface with before-and-after browser evidence.
```

The skill is intended for working interfaces that need visual or responsive refinement. It is not a replacement for new product design, rebranding, or feature development.

## Inspiration

The workflow was informed by:

- [BridgeMind’s step-by-step vibe coding workflow](https://www.youtube.com/watch?v=vBndrDoB_X4), especially its use of screenshots, browser automation, and task handoffs;
- [Meathill’s maintenance Skill write-up](https://x.com/meathill1/status/2036334114169823731), especially explicit negative constraints and verification after changes;
- the community shift toward [iterative loop engineering](https://x.com/i/trending/2063869701080437219) instead of relying on one large prompt.

Visual Polish Loop recombines those ideas around one narrow task: proving that an existing interface became visibly better without breaking its behavior. No third-party code is included.

## Validation

The package is validated with Codex `skill-creator` and contains no runtime dependencies.

## License

[MIT](LICENSE)
