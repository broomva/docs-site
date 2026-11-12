# Glossary

These are the terms used across the docs, in the sense Pocket Timer uses them.

## Session

A session is one focused stretch of work. `pocket start` runs a session. It lasts 25 minutes by default.
You can change the length with `session_minutes` in the [configuration](configuration.md#session-length) file.

## Break

A break is a rest between sessions. `pocket break` runs a 5-minute break. See
[taking a break](getting-started.md#taking-a-break) for how to start one. Breaks never count toward your daily goal.

## Daily goal

The daily goal is how many sessions make a full day. `daily_goal = 8` sets it to eight sessions. Read more in
[the daily goal](configuration.md#daily-goal). `pocket today` shows your progress toward it.

## History

History is the record of your sessions and breaks. Pocket Timer keeps one line per session or break in
`~/.pocket/history.jsonl`. See [where your history is stored](faq.md#where-is-my-history-stored) for details.

Back to [the index](index.md).
