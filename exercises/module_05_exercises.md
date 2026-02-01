# 📝 Module 5 Exercises: Evaluation and Optimization

---

## Exercise 5.1: Defining Success Metrics

Define metrics for these prompt use cases.

**Use Case 1: Sentiment Analysis Bot**
```
Primary Metrics:
1. _____________ (Target: ___)
2. _____________ (Target: ___)

Secondary Metrics:
1. _____________ (Target: ___)

How to Measure:
[Describe measurement approach]
```

**Use Case 2: Customer Email Generator**
```
Primary Metrics:
1. _____________ (Target: ___)
2. _____________ (Target: ___)

Secondary Metrics:
1. _____________ (Target: ___)

How to Measure:
[Describe measurement approach]
```

**Use Case 3: Code Review Assistant**
```
Primary Metrics:
1. _____________ (Target: ___)
2. _____________ (Target: ___)

Secondary Metrics:
1. _____________ (Target: ___)

How to Measure:
[Describe measurement approach]
```

---

## Exercise 5.2: A/B Test Design

Design an A/B test for improving a summary prompt.

**Current Prompt (Control):**
```
Summarize the following article.
[article]
```

**Test Prompt (Variant):**
```
[Write an improved version to test]
```

**A/B Test Plan:**
```
Hypothesis: 
[What do you expect to happen?]

Sample Size: 
[How many test cases?]

Metrics to Compare:
1. 
2.
3.

Success Criteria:
[What counts as "better"?]

Test Duration:
[How long to run?]
```

---

## Exercise 5.3: Test Case Creation

Create a test dataset for a classification prompt.

**Task:** Classify customer feedback as: Complaint, Question, Praise, Suggestion

**Create 12 test cases (3 per category):**

| ID | Input | Expected | Category |
|----|-------|----------|----------|
| 1 | | Complaint | Clear |
| 2 | | Complaint | Subtle |
| 3 | | Complaint | Edge case |
| 4 | | Question | Clear |
| 5 | | Question | Subtle |
| 6 | | Question | Edge case |
| 7 | | Praise | Clear |
| 8 | | Praise | Subtle |
| 9 | | Praise | Edge case |
| 10 | | Suggestion | Clear |
| 11 | | Suggestion | Subtle |
| 12 | | Suggestion | Edge case |

---

## Exercise 5.4: Variability Analysis

Test a prompt at different temperatures and document variability.

**Prompt to Test:**
```
Generate a creative product name for:
A smartwatch designed for athletes
```

**Test Results:**

| Run | Temp 0.0 | Temp 0.5 | Temp 1.0 |
|-----|----------|----------|----------|
| 1 | | | |
| 2 | | | |
| 3 | | | |
| 4 | | | |
| 5 | | | |

**Analysis:**
```
Consistency at temp 0.0: ____%
Consistency at temp 0.5: ____%
Consistency at temp 1.0: ____%

Observations:
[What patterns did you notice?]

Recommendation:
[Which temperature is best for this use case?]
```

---

## Exercise 5.5: Failure Mode Analysis

Analyze these prompt failures and propose fixes.

**Failure 1:**
```
Prompt: Extract the date from this text.
Input: "Let's meet sometime next week"
Expected: Error/No date found
Actual: "2024-03-25" (made up a date)

Failure Type: _______________
Root Cause: ________________
Fix: ______________________
```

**Failure 2:**
```
Prompt: Translate to formal English.
Input: "yo whats good"
Expected: "Hello, how are you?"
Actual: "Yo, what is good?"

Failure Type: _______________
Root Cause: ________________
Fix: ______________________
```

**Failure 3:**
```
Prompt: Answer the question using the provided context.
Input: Question about 2024, context only has 2023 data
Expected: "Information not available in context"
Actual: Generated speculative 2024 data

Failure Type: _______________
Root Cause: ________________
Fix: ______________________
```

---

## Exercise 5.6: Prompt Versioning

Create a version history for a prompt through several iterations.

**Initial Problem:** Prompt for extracting action items from meeting notes

**Version 1.0:**
```
Extract action items from these meeting notes.
[notes]
```

**Issues Found:** [List issues]

**Version 1.1:**
```
[Improved prompt]
```

**Issues Found:** [List issues]

**Version 2.0:**
```
[Major revision]
```

**Create a changelog:**
```markdown
# Action Item Extractor - Changelog

## v2.0 (Current)
- Changes: 
- Metrics: 

## v1.1
- Changes:
- Metrics:

## v1.0 (Initial)
- Metrics:
```

---

## Exercise 5.7: Token Optimization

Optimize these prompts for token efficiency without losing quality.

**Original Prompt (est. 120 tokens):**
```
You are a helpful AI assistant designed to help users with their 
questions. Your goal is to provide accurate, helpful, and relevant 
answers to whatever the user asks. Please think carefully about 
the question before responding and make sure your answer is correct. 
Be concise but thorough in your explanations.

The user's question is: What is the capital of France?

Please provide your answer below:
```

**Optimized Version (target: <50 tokens):**
```
[Write optimized version]
```

**Token Savings:** ____%

---

**Original Prompt (est. 150 tokens):**
```
I would like you to take on the role of a professional editor 
who specializes in improving the clarity and readability of 
written content. Please review the following text carefully 
and make improvements to:
1. Grammar and punctuation
2. Sentence structure  
3. Word choice
4. Overall flow

Here is the text that needs editing:
"The quick brown fox jumped over lazy dog yesterday morning."

Please provide your edited version along with explanations 
for each change you made.
```

**Optimized Version (target: <80 tokens):**
```
[Write optimized version]
```

---

## Exercise 5.8: Cost Calculation

Calculate costs for a prompt deployment scenario.

**Scenario:**
- Prompt system tokens: 200
- Average user input: 150 tokens
- Average output: 300 tokens
- Daily requests: 5,000
- Model: GPT-4 ($0.03/1K input, $0.06/1K output)

**Calculate:**
```
Cost per request:
- Input tokens: ____ × $0.03/1K = $____
- Output tokens: ____ × $0.06/1K = $____
- Total per request: $____

Daily cost: ____ × $____ = $____
Monthly cost: $____ × 30 = $____

Cost reduction strategies:
1.
2.
3.
```

---

## Exercise 5.9: Evaluation Script

Write pseudocode for an automated evaluation system.

```python
# Evaluation System for Classification Prompt

def evaluate_classifier(prompt, test_cases):
    """
    Parameters:
    - prompt: The classification prompt template
    - test_cases: List of {input, expected_output}
    
    Returns:
    - Accuracy score
    - Detailed results
    - Failure analysis
    """
    
    # Your implementation:
    results = []
    
    # 1. Loop through test cases
    
    # 2. Call LLM with prompt + input
    
    # 3. Compare output to expected
    
    # 4. Record result
    
    # 5. Calculate metrics
    
    # 6. Group failures by type
    
    return {
        'accuracy': 0.0,
        'results': results,
        'failure_analysis': {}
    }
```

---

## 🎯 Challenge Exercise: Complete Evaluation Pipeline

Build a complete evaluation pipeline for a translation prompt.

**Step 1: Define Metrics**
```
Primary:
Secondary:
```

**Step 2: Create Test Dataset**
```
[Create 10 diverse test cases with expected outputs]
```

**Step 3: Baseline Prompt**
```
[Write your initial prompt]
```

**Step 4: Run Evaluation**
```
[Document results]
```

**Step 5: Iterate and Improve**
```
[Show 2-3 iterations with improvements]
```

**Step 6: Final Results**
```
| Version | Accuracy | Consistency | Latency |
|---------|----------|-------------|---------|
| v1 | | | |
| v2 | | | |
| v3 | | | |
```

---

## Exercise 5.10: Iterative Improvement Process

Document your improvement process for this prompt.

**Starting Prompt:**
```
Summarize this product review.
```

**Improvement Cycle 1:**
```
Issue Identified:
Changes Made:
New Prompt:
Result:
```

**Improvement Cycle 2:**
```
Issue Identified:
Changes Made:
New Prompt:
Result:
```

**Improvement Cycle 3:**
```
Issue Identified:
Changes Made:
New Prompt:
Result:
```

**Final Comparison:**
| Metric | V1 | V2 | V3 | V4 (Final) |
|--------|----|----|----|----|
| Quality | | | | |
| Consistency | | | | |
| Token Usage | | | | |

---

## ✅ Self-Assessment

Rate your understanding (1-5):

| Concept | Rating | Notes |
|---------|--------|-------|
| Defining metrics | /5 | |
| A/B testing | /5 | |
| Creating test datasets | /5 | |
| Handling variability | /5 | |
| Failure analysis | /5 | |
| Prompt versioning | /5 | |
| Token optimization | /5 | |
| Cost calculation | /5 | |

---

**These exercises build evaluation skills - crucial for production!**
