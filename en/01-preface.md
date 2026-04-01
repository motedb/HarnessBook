# Preface

Over the past few years, the most common question around artificial intelligence—and the one most likely to provoke strong emotions—has been this: will models replace programmers?

It is, of course, a compelling question, because it speaks directly to professional anxiety, industrial narratives, and our imagination of the age.

But it also has an obvious flaw: it focuses too early on whether people will be replaced, while overlooking how work itself is being reorganized. The deeper transformation usually begins with the latter.

Hold two scenes in your mind side by side.

In the first, OpenAI used Codex to build internal products within a matter of months under almost extreme constraints: no one hand-wrote application code, and code, tests, documentation, CI, and observability were all produced by agents.

In the second, METR invited senior open-source developers who were deeply familiar with their repositories to use early-2025 AI tools in real projects. The result was not faster development, but an average slowdown of `19%`.

If we ask only whether models can write code, these two scenes cannot be explained at the same time. But if we instead ask what kind of working environment these teams prepared for the model, the picture suddenly becomes much clearer (see References [1] and [11]).

A more precise question is this: when models can already read code, understand repositories, call tools, edit files, run verification, and produce results, what kind of shape will software engineering be reorganized into?

In other words, when a model that once merely answered questions begins to participate in work, what kind of working environment do we need to build for it?

That is the question this book attempts to answer.

In the earliest years, when people spoke about AI and engineering, the dominant language was that of assistance: assisting with functions, patching documentation, generating tests, explaining error messages.

At the time, how to prompt the model better was almost the whole discussion. That history was not false. It produced real breakthroughs and genuinely changed the way many people worked.

But by now, that language is no longer enough. The question is no longer just whether a model can help me do a little work. It is whether, if a model begins to truly do work, we know how to build a world for it.

That is precisely the background against which harness engineering becomes important (see References [1], [6], and [7]).

If I had to compress the entire matter into the most memorable metaphor, I would put it this way: getting an agent to work is less like posing problems to a genius and more like setting up a workstation for a new colleague.

You still need to explain the task clearly, of course. But you also need to give that colleague a desk, access control, a codebase, a test environment, an on-call manual, an approval path, and a clear person to contact when something goes wrong. A single instruction is not organizational work. It is more like throwing someone into the field to see whether they can figure things out on their own.

Many discussions today treat the current shift as a simple extension of prompt engineering, as though writing the prompt a little more precisely were enough to produce a stable agentic system.

Reality quickly proved otherwise. Whether an agent can reliably complete a task often depends less on whether the prompt is clever enough than on the environment in which the agent operates: what it can see, what it can call, what is allowed, what is forbidden, how completion is verified, how failure is recovered from, and how experience is sedimented into rules.

OpenAI's experience shows that once the environment is organized clearly, agent productivity undergoes a qualitative leap.

Anthropic's experience shows that even when the model is strong, long-running tasks still repeatedly lose continuity if there is no progress log, no initialization script, no feature list, and no session handoff.

LangChain's experiments go one step further by turning this change into measurable results: with the model held constant, changing only the harness can raise the score from `52.8` to `66.5`.

These materials matter not because they all support optimism, but because together they force a harsher judgment: a single expression still matters, but whether work can actually be brought to completion increasingly depends on the working system that surrounds that expression (see References [1], [9], and [10]).

That working system includes repository structure, knowledge organization, tool interfaces, execution boundaries, testing and evaluation, observability, planning mechanisms, rollback and escalation paths, and even the way a team allocates responsibility.

Harness engineering concerns this entire scaffold. It matters not because the term is new, but because it captures a real change: much of the infrastructure that once primarily served human collaboration is being rewritten into a production environment that agents can also enter (see References [1], [3], [9], and [10]).

This is what I care most about in writing this book. The most fashionable ways of talking about the present moment are often either too optimistic or too defensive.

The optimistic version likes to say that AI can already write a million lines of code. The defensive version likes to use a single counterexample to prove that AI is fundamentally incapable. Both are too light.

What deserves discussion more is why some teams are beginning to accumulate compounding gains while others are held back by interaction friction, verification costs, and tacit knowledge. Only when we explain that clearly does harness engineering stop being a buzzword and become a long-term engineering perspective worth using.

This brings with it a subtle but profound shift in role. In the past, an excellent engineer was mainly distinguished by how complex a system they could write, how difficult a bug they could solve, or how much chaos they could refactor into order.

Today, those abilities still matter. But an engineer's value is increasingly expressed further upstream: in whether they can define goals clearly, externalize tacit knowledge, turn boundaries into rules, turn experience into default paths, and turn a single mistake into a mechanism by which the system does not make the same mistake again.

The work of engineers is increasingly shifting toward organizing the conditions under which tasks can be completed reliably.

This is not a decline in capability. It is a rise in the level at which capability is exercised. You still need to understand implementation, architecture, systems, and quality; it is just that these capabilities no longer serve only a piece of code you personally wrote, but begin to serve a larger working environment.

I did not write this book to deify a particular model, tool, or company's product.

On the contrary, I hope to pull the discussion out of product marketing and short-lived buzzwords, and return it to a more stable engineering question: how do we design environment, constraints, verification, observation, and feedback so that an intelligent system that is imperfect but powerful enough can reliably produce value in the real world?

For that reason, this book will not discuss only how to write prompts, nor will it focus mainly on feature checklists for a particular IDE or agent framework.

It is more concerned with methodology: what harness is, what layers it consists of, why it is becoming one of the most important pieces of engineering infrastructure in the agent era, and how it will rewrite software engineering, team collaboration, and organizational governance.

If you are a front-line engineer, this book will help you understand why more and more technical work is shifting toward building systems rather than merely patching implementations.

If you are a technical leader, it will help you judge that bringing agents into production is not simply a matter of adopting a stronger model, but of reconstructing part of the engineering environment itself.

The same is true for product leaders and organizational managers: an agent system is not just a simple automation plug-in, but a new way of organizing production.

This book holds a firm but restrained position: agents are indeed changing software production.

But the core of that change is not that AI can write a great deal of code. It is that engineering knowledge is, for the first time, being systematically rewritten into a form that machines can read, execute, verify, and improve (see References [1], [3], and [9]).

If the book is written well enough, readers should not come away merely remembering a few new terms. They should instead form a new habit of judgment: when they see an agent system perform brilliantly, they will ask about the knowledge structure, verification chain, and organizational division of labor behind it; when they see an AI project struggle in reality, they will not immediately attribute the failure to the model not being strong enough, but will instead examine how the repository, process, permissions, feedback, and responsibility are actually distributed.

The book also remains deliberately cautious. Any new concept can be mythologized in the course of being spread, and harness engineering is no exception.

It can easily be described as a universal key, as though once the scaffold is built, an agent will automatically become a reliable employee. That imagination is not responsible. The more complex the system becomes, the more important responsibility, boundaries, verification, and governance become.

The value of harness engineering lies not in promising a future that needs no management, but in recognizing that we must manage more seriously.

What I hope readers take away is not temporary enthusiasm for a particular tool, but a more stable framework of judgment: when faced with any agent system, they can ask how goals are defined, how context is organized, how tools are integrated, how boundaries are constrained, how verification is completed, how experience is accumulated, and how the system is governed.

In that sense, what will be scarcer in the future may not simply be people who know how to use agents better, but rather people who can organize the working environment well enough for agents to enter it reliably.

## Preface Summary

The starting point of this book is simple: AI's impact on software engineering lies not only in the model, but in how the working environment is reorganized. Whoever sees this earlier as an engineering problem rather than merely a tool problem will be more likely to build a stable advantage in the age of agents. The prologue begins by pinning this issue to several conflicts in reality that can no longer be avoided.
