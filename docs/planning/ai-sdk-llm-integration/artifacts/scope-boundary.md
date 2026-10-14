# Scope Boundary: AI SDK LLM Integration

## Work Item

No work item exists. The operator's request, typed when invoking `/han-planning:plan-a-change`, is the only boundary this run has.

## Stated Scope

> to implement https://ai-sdk.dev as the integration layer between skillwalker an the LLM. the initial goal is to set this up with Claude Code access only. as part of this, we're getting rid of the claude sandbox entirely and will rely entirely on API access

## Stated Exclusions

- The community `ai-sdk-provider-claude-code` provider (operator, 2026-10-14).
- Otherwise none stated. Implied by "the initial goal is to set this up with Claude Code access only": providers other than Claude Code are not part of this run.

## Operator-Stated Scope

> create a branch for this work to be planned and implemented. commit and push as you go. open a draft pr

> since this is an experiment to understand how things would actually work, i want to build this out with AI-SDK only, and not use the community claude provider. that means we need to implement the skills and custom agents. in ~/dev/mxriverlynn/3pitor/ we built out an MCP server to handle these calls from inside of the 3pitor runtime. i'd like to do the same, here. i think this should give us much more fine-grained control and isolation, without the sandbox need.

Interpretation recorded with the operator's statement: "Claude Code access only" from the original request is superseded for provider choice. The community `ai-sdk-provider-claude-code` provider is excluded. The model is reached through AI SDK directly, and Skillwalker implements skill and custom-agent loading and invocation itself, through an MCP server modeled on the one in `~/dev/mxriverlynn/3pitor/`. The operator accepted that trigger results then measure Skillwalker's own harness rather than Claude Code's, framing the work as "an experiment to understand how things would actually work".

## Direction of Travel

The Test Sandbox (`@testdouble/sandbox-integration`, the `skillwalker sandbox` subcommands, and the sandbox shell scripts in `@testdouble/claude-integration`) is being removed entirely, not deprecated: "we're getting rid of the claude sandbox entirely and will rely entirely on API access".

## Visual Material Received

None received

## Record Provenance

Established by `han-planning:plan-a-change` on 2026-10-14, from the operator's invocation text. Not inherited. Updated 2026-10-14 with the operator's provider decision (AI SDK only, own MCP skill/agent server).
