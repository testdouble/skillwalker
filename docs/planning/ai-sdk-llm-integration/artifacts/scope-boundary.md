# Scope Boundary: AI SDK LLM Integration

## Work Item

No work item exists. The operator's request, typed when invoking `/han-planning:plan-a-change`, is the only boundary this run has.

## Stated Scope

> to implement https://ai-sdk.dev as the integration layer between skillwalker an the LLM. the initial goal is to set this up with Claude Code access only. as part of this, we're getting rid of the claude sandbox entirely and will rely entirely on API access

## Stated Exclusions

None stated. Implied by "the initial goal is to set this up with Claude Code access only": providers other than Claude Code are not part of this run.

## Operator-Stated Scope

> create a branch for this work to be planned and implemented. commit and push as you go. open a draft pr

## Direction of Travel

The Test Sandbox (`@testdouble/sandbox-integration`, the `skillwalker sandbox` subcommands, and the sandbox shell scripts in `@testdouble/claude-integration`) is being removed entirely, not deprecated: "we're getting rid of the claude sandbox entirely and will rely entirely on API access".

## Visual Material Received

None received

## Record Provenance

Established by `han-planning:plan-a-change` on 2026-10-14, from the operator's invocation text. Not inherited.
