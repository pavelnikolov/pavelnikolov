+++
title = "The Go Code You Didn’t Write"
subtitle = "Day-2 Engineering in a Post-Human Codebase"
date = "2026-06-14T15:13:00+10:00"
draft = false
event = "Sample meetup deck"
location = "Sydney"
duration = "30 min"
tags = ["go", "engineering", "ai"]
+++

## The Go Code You Didn’t Write

Day-2 Engineering in a Post-Human Codebase

---

## AI agents are everywhere
- We generate code fast
- Troubleshooting

---

## You can delegate the wriging of the code

---

## You can NOT delegate the ownership

---

## Prompt hygiene is now engineering hygiene

- Define constraints before asking for code.
- Write specs befire writing a prompt.
- Require invariants and edge-case handling.
- Keep prompts and specs versioned with code.

---

## The velocity trap

- Complexity
- Spaghetti code
- Tech debt

---

## How to reduce tech debt?
- holistic thinking
- deep modules (packages, types)
- design your interfaces
- consistent naming
- stick to the stdlib
- write tests (using Go testing pkg)

---

## Deep modules
- TDD allows for fast feedback loop
- Useful for both AI agents and humans

---

## Write tests first
- TDD allows for fast feedback loop
- Useful for both AI agents and humans
- avoid testing frameworks

---

## Design your interfaces
- TDD allows for fast feedback loop
- Useful for both AI agents and humans

---

## Use consistent names
- reduces cognitive load
- improves readability

---

## (Avoid) Dependencies
- Best code = no code. Best dep = no dep.
- A dependency is only imported from 1 package.


---

#### Go review checklist for generated code

```go {hl_lines=["6-6"]}
func Reconcile(ctx context.Context, in Input) (Output, error) {
	if err := validate(in); err != nil {
		return Output{}, fmt.Errorf("validate input: %w", err)
	}

	result, err := service.Run(ctx, in)
	if err != nil {
		return Output{}, fmt.Errorf("run service: %w", err)
	}

	return result, nil
}
```

---

## Managing tech debt

- Bad code compounds (so does good one)
- Ensure regular refactoring sessions
- Pay tech debt, before it grows out of the context window 

---

## AI is a multiplier
- AI is a multiplier when used correctly.
- Unfortunately, it is also a multiplier when used incorrectly.

---

## Final takeaway

AI can generate code.
Engineering teams must generate confidence.
