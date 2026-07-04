# Engineering Thinking Checklist

Before making any engineering decision, walk through this checklist.

---

## 1. Understand the Problem

- [ ] What is the actual problem?
- [ ] Am I solving a symptom or the root cause?
- [ ] Can I explain the problem in one sentence?

---

## 2. Understand Requirements

### Functional Requirements

- [ ] What must the system do?

### Non-Functional Requirements

- [ ] Latency
- [ ] Availability
- [ ] Reliability
- [ ] Scalability
- [ ] Security
- [ ] Cost
- [ ] Maintainability

---

## 3. Identify Constraints

- [ ] Budget
- [ ] Timeline
- [ ] Team size
- [ ] Existing infrastructure
- [ ] Expected traffic
- [ ] Data size
- [ ] Compliance requirements

---

## 4. Gather Evidence

- [ ] What metrics do I have?
- [ ] What logs are available?
- [ ] What changed recently?
- [ ] Can I reproduce the issue?
- [ ] Am I making assumptions?

---

## 5. List Alternatives

Before choosing a solution, list at least three possible approaches.

Example

- Solution A
- Solution B
- Solution C

---

## 6. Evaluate Trade-offs

For every solution ask:

- What improves?
- What becomes worse?
- What new complexity is introduced?
- What operational cost is added?

---

## 7. Failure Analysis

Ask yourself:

- What happens if this component fails?
- Is there graceful degradation?
- Can users still perform critical operations?
- How is recovery handled?

---

## 8. Scaling

Think ahead.

- What happens at 10× traffic?
- What happens at 100× traffic?
- What becomes the bottleneck?
- Will this architecture still work?

---

## 9. Observability

How will I know if the system is unhealthy?

- Logs
- Metrics
- Traces
- Alerts
- Dashboards

---

## 10. Final Decision

Document your reasoning.

Problem

↓

Constraints

↓

Alternatives

↓

Chosen Solution

↓

Trade-offs

↓

Failure Handling

↓

Monitoring

↓

Future Improvements

---

## Golden Rule

Never answer:

> "Use Redis."

Instead answer:

> "Given these constraints, Redis is appropriate because it reduces database load while accepting the trade-offs of cache invalidation and operational complexity."

The reasoning is more important than the technology.