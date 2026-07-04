# How Senior Engineers Think

> "Technology is the last decision, not the first."

---

## The Biggest Mindset Shift

Junior engineers often think like this:

Problem
↓
Technology

Example

> Checkout is slow.

↓

Use Redis.

---

Senior engineers think differently.

Problem
↓
Understand
↓
Measure
↓
Identify Constraints
↓
Generate Alternatives
↓
Evaluate Trade-offs
↓
Choose Technology

Technology is almost always the final step.

---

## Layered Thinking

Every engineering problem exists at multiple layers.

Business Problem
↓

User Problem
↓

Engineering Problem
↓

Constraints
↓

Possible Patterns
↓

Technology

Example

Business:
Users complain videos buffer.

Instead of saying "Use CDN", ask:

- Which region?
- Mobile or desktop?
- Startup buffering or during playback?
- Is every video affected?
- Did traffic suddenly increase?
- Is the origin overloaded?
- What is the cache hit ratio?

Only after understanding the problem should a solution be proposed.

---

## Engineers Solve Root Causes

Symptoms are not problems.

Example

Symptom

API latency increased from 100ms to 2s.

Possible causes

- Missing database index
- Cache failure
- External API slowdown
- Network issue
- Lock contention
- N+1 query
- High CPU usage
- Connection pool exhaustion

The correct solution depends on identifying the root cause.

---

## Never Fall in Love With Technologies

Learning a new tool creates bias.

Example

Learn Redis

↓

Every problem looks like caching.

Learn Kafka

↓

Every problem looks asynchronous.

Good engineers recognise patterns before choosing tools.

---

## Pattern Recognition

Instead of asking

"What technology should I use?"

Ask

"What category of problem is this?"

Examples

Repeated reads
→ Caching

Long-running task
→ Asynchronous Processing

Duplicate requests
→ Idempotency

Traffic spikes
→ Rate Limiting

Large datasets
→ Partitioning / Sharding

Slow database reads
→ Indexes / Read Replicas / Caching

Notice that each problem has multiple possible solutions.

Choosing between them is the engineering decision.

---

## Measure Before You Decide

Avoid assumptions.

Collect evidence.

Questions to ask:

- What changed recently?
- Which users are affected?
- Is every endpoint slow?
- Is the database healthy?
- Is CPU high?
- Is memory high?
- Are retries increasing?
- Is one dependency failing?
- What do the logs show?
- What do the metrics show?

Engineering decisions should be evidence-driven.

---

## Every Decision Optimises Something

Every solution improves one aspect while sacrificing another.

Examples

Caching

+ Lower latency
- Stale data

Normalization

+ Better consistency
- More joins

Denormalization

+ Faster reads
- Data duplication

Queue

+ Better scalability
- Eventual consistency

There are no perfect solutions.

Only trade-offs.

---

## Mental Model

Whenever you face a backend problem, follow this sequence:

Problem
↓

Understand

↓

Measure

↓

Identify Constraints

↓

Generate Alternatives

↓

Compare Trade-offs

↓

Choose

↓

Plan for Failure

↓

Plan for Scale

---

## Key Takeaways

- Technology should never be the first answer.
- Solve root causes instead of symptoms.
- Evidence is more valuable than assumptions.
- Every engineering decision involves trade-offs.
- Good engineers choose tools.
- Great engineers justify why they chose them.