---
title: Ruby's Potential in the LLM Era
description: When machine slop requires human review, prefer poetry
date: 2025-09-01
---
When working with LLM-generated code, one truth stands out: **you must read every line**. If you’re investing time to review code, wouldn’t you prefer it to read like poetry rather than a sprawling novel?

Ruby’s expressiveness—its ability to convey complex logic in fewer lines than most languages, except perhaps some functional programming alternatives—becomes a superpower when every line of generated code demands human scrutiny. Each unchecked line is technical debt, and Ruby minimizes this burden by keeping code concise yet readable.

Consider this example of processing a CSV file, transforming data, and sending notifications. This code requires no compilation and can be evaluated directly in a Ruby REPL (e.g., IRB), making it even more flexible for rapid prototyping:

```ruby
users = CSV.parse(file, headers: true)
  .select { |u| u['active'] == 'true' }
  .map { |u| User.new(u) }
  .each { |user| user.notify! if user.due_for_reminder? }
```

In Java, this same logic might balloon to 50+ lines, tangled in BufferedReader boilerplate, try-catch blocks, manual CSV parsing, stream collectors, lambda type declarations, and explicit null checks. Go fares even worse, with verbose error handling cluttering every operation. Ruby’s elegance reduces the cognitive load, letting you focus on the logic rather than the syntax.

The key question isn’t which language has the most libraries or the largest community. It’s: **which language maximizes the velocity of understanding for LLM-generated code?** As LLMs grow more sophisticated, languages prioritizing human comprehension over machine-centric verbosity are likely to lead the way.
