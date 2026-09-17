# Function Word DNA Compressor — Technical Operational Dispatcher

**Framework Author**: William Fitzpatrick (*Writer Science*)  
**Source Lecture**: [How to write so well that readers stop scrolling](https://www.youtube.com/watch?v=IqPLeyTahLs)  
**Parent Collection**: [Master Collection](../../kirby-fitzpatrick-writers-collection/SKILL.md) | [Global Help](../../../kirby-help/SKILL.md)  

---

## 1. Cognitive Foundation: Lexical Density vs. Grammatical Glue

Every sentence consists of two classes of words:
1. **Content Words (Information Payload)**: Nouns, main verbs, domain adjectives, concrete technical parameters.
2. **Function Words (Grammatical Glue)**: Prepositions, articles (*the*, *a*), auxiliary verbs (*is*, *have*, *will*), pronouns (*it*, *this*), and conjunctions (*that*, *which*).

Amateur prose and untuned LLM output drown in grammatical glue, averaging only **35–40% content words**. High-signal technical writing and senior engineering RFCs tune the "DNA" of sentences to achieve **$\ge 55\%$ lexical density**.

```text
[Low Density / Glue Heavy: 38% Content (6/16 words)]
"It is the responsibility of the scheduler to ensure that all of the tasks are executed."
 -- -- --- -------------- -- --- --------- -- ------ ---- --- -- --- ----- --- --------
 Glue Glue  Content       Glue  Content    Glue  Content Glue Glue Content Glue Content

[High Density / Compressed: 75% Content (6/8 words)]
"The scheduler ensures all tasks execute reliably."
 --- --------- ------- --- ----- ------- --------
 Glue Content   Content Glue Content Content Content
```

---

## 2. Core Compression Protocols

### Protocol 1: The 55% Lexical Density Target
Calculate sentence density:
$$\text{Density} = \frac{\text{Nouns} + \text{Verbs} + \text{Adjectives}}{\text{Total Words}} \times 100$$
Aim for $\ge 55\%$ in documentation and commit messages.

### Protocol 2: Auxiliary Verb Pruning
Eliminate continuous and passive verb tenses that require auxiliary glue (*is doing*, *has been verified by*, *will be responsible for*):

| Glue-Heavy Auxiliary | Compact Active Verb |
|---|---|
| `is responsible for handling` | `handles` |
| `has the capability to parse` | `parses` |
| `will be executing` | `executes` |
| `is capable of supporting` | `supports` |
| `is intended to serve as` | `serves as` |

### Protocol 3: Dummy Pronoun Elimination
Strip empty syntactic place-holders (*"there is"*, *"it is"*, *"what we want to do is"*):
* **Slop**: *"What this pull request does is to provide support for WebSockets."* (12 words, 4 content words = 33%)
* **Compressed**: *"This PR adds WebSocket support."* (5 words, 4 content words = 80%)

---

## 3. Engineering Application Scenarios

### 3.1 Architecture Decision Records (ADRs)
* **Glue-Heavy**: *"It was decided by the team that we should be adopting gRPC because of the fact that it is faster."* (20 words, 5 content = 25%)
* **DNA Compressed**: *"The team adopted gRPC for lower serialization latency."* (8 words, 6 content = 75%)

### 3.2 Commit Messages & Release Notes
* **Glue-Heavy**: *"Made changes to the cache manager so that it will automatically evict old keys when it runs out of memory."* (21 words, 7 content = 33%)
* **DNA Compressed**: *"feat(cache): auto-evict expired keys on OOM pressure"* (7 words, 6 content = 85%)

### 3.3 Code Comments
* **Glue-Heavy**: `// This is a function that has been created to check if the user is authenticated or not.`
* **DNA Compressed**: `// Checks user authentication status.`

---

## 4. Verification Checklist

- [ ] Does the sentence achieve $\ge 55\%$ content word ratio?
- [ ] Have auxiliary constructions (*"is responsible for"*) been replaced by active verbs?
- [ ] Are empty grammatical openers (*"It is"*, *"There are"*) removed?
- [ ] Do technical nouns and verbs dominate the sentence line?
