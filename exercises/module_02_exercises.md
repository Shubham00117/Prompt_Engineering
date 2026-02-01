# 📝 Module 2 Exercises: Core Prompting Strategies

---

## Exercise 2.1: Delimiter Practice

Rewrite this messy prompt using proper delimiters.

**Original (messy):**
```
Translate the following text which is about a cooking recipe 
to Spanish and make sure you only translate the recipe part 
not the instructions I'm giving you and the recipe is 
Mix flour sugar and eggs bake at 350 for 30 minutes.
```

**Your improved version with delimiters:**
```
[Write your version here using XML tags or other delimiters]
```

---

## Exercise 2.2: XML Tag Structure

Create properly structured prompts using XML tags for:

**Scenario 1: Sentiment Analysis**
Input: A product review
Output: Sentiment label + explanation

```xml
[Write your XML-structured prompt]
```

**Scenario 2: Language Translation with Context**
Input: A sentence and its context
Output: Translation with cultural notes

```xml
[Write your XML-structured prompt]
```

---

## Exercise 2.3: Role Assignment

Create role-based prompts for these scenarios:

**Scenario 1:** You need advice on investing for retirement
```
Role prompt:
[Your prompt with role assignment]
```

**Scenario 2:** You want creative feedback on a short story
```
Role prompt:
[Your prompt with role assignment]
```

**Scenario 3:** You need to explain a complex legal document simply
```
Role prompt:
[Your prompt with role assignment]
```

---

## Exercise 2.4: Output Format Specification

Write prompts that specify exact output formats.

**Task 1:** Extract contact info from text → JSON
```
Input text: "Call John at 555-1234 or email john@email.com"

Your prompt:
[Include exact JSON schema expected]
```

**Task 2:** Compare 3 products → Markdown table
```
Products: iPhone, Samsung Galaxy, Google Pixel

Your prompt:
[Specify exact table format]
```

**Task 3:** Summarize an article → Bullet points
```
Your prompt:
[Specify exact bullet format and constraints]
```

---

## Exercise 2.5: Zero-Shot to Few-Shot Conversion

Convert these zero-shot prompts to few-shot with 2-3 examples.

**Zero-Shot Prompt:**
```
Classify this email as spam or not spam:
"Congratulations! You've won $1,000,000!"
```

**Your Few-Shot Version:**
```
[Add 2-3 examples before the actual classification]
```

---

**Zero-Shot Prompt:**
```
Extract the main topic from this news headline:
"Tech Giants Report Record Profits Amid AI Boom"
```

**Your Few-Shot Version:**
```
[Add examples showing input/output pairs]
```

---

## Exercise 2.6: Creating Positive and Negative Examples

Create a few-shot prompt that includes both good and bad examples.

**Task:** Generate professional email subject lines

**Your prompt with + and - examples:**
```
[Include at least 2 good examples and 2 bad examples
with explanations of why each is good or bad]
```

---

## Exercise 2.7: Chain-of-Thought Prompts

Add chain-of-thought reasoning to these prompts.

**Original Prompt 1:**
```
Is this argument logically valid?
"All birds can fly. Penguins are birds. 
Therefore, penguins can fly."
```

**With Chain-of-Thought:**
```
[Rewrite to encourage step-by-step analysis]
```

---

**Original Prompt 2:**
```
A store has a "Buy 2, Get 1 Free" deal. 
Each item costs $15. If I want 7 items, 
how much will I pay?
```

**With Chain-of-Thought:**
```
[Rewrite to encourage step-by-step calculation]
```

---

## Exercise 2.8: Self-Verification Prompts

Create prompts that ask the AI to verify its own answers.

**Task:** Code generation with verification
```
Write a Python function to find the second largest 
number in a list, then verify your solution.

[Write a prompt that includes:
1. The coding task
2. Request to verify with test cases
3. Request to check edge cases]
```

---

## Exercise 2.9: Complex Combined Prompt

Create a single prompt that combines multiple techniques:
- Role assignment
- Delimiters
- Output format
- One example (one-shot)

**Scenario:** You want AI to analyze customer feedback and provide improvement suggestions.

```
[Write your comprehensive prompt]
```

---

## 🎯 Challenge Exercise: Complete Prompt Engineering Task

**Scenario:** Build a prompt for a recipe recommendation system.

Requirements:
1. Use role assignment (culinary expert)
2. Accept user preferences in a structured format
3. Provide recommendations with specific format
4. Include one example
5. Add chain-of-thought for matching logic

**User Input Structure:**
```
Cuisine preference: [type]
Dietary restrictions: [list]
Cooking time available: [minutes]
Skill level: [beginner/intermediate/advanced]
```

**Your Complete Prompt:**
```
[Write the full prompt with all techniques combined]
```

**Test Your Prompt:**
- Try with: Italian, vegetarian, 30 minutes, beginner
- Document the response quality

---

## Exercise 2.10: Prompt Debugging

These prompts have issues. Identify and fix them.

**Problem Prompt 1:**
```
You are a helpful assistant. 
Answer this question: What is 25% of 80?
Make sure to be accurate.
Think about it carefully.
Double check your math.
```

**Issue(s):** 
```
[Identify]
```

**Fixed:**
```
[Fix it]
```

---

**Problem Prompt 2:**
```
Examples:
Input: Dog
Output: Animal

Now classify: Cloud
```

**Issue(s):** 
```
[Identify]
```

**Fixed:**
```
[Fix it]
```

---

## ✅ Self-Assessment

Rate your understanding (1-5):

| Concept | Rating | Notes |
|---------|--------|-------|
| Using delimiters | /5 | |
| Separating instruction/content | /5 | |
| Role-based prompting | /5 | |
| Output format specification | /5 | |
| Zero-shot vs few-shot | /5 | |
| Chain-of-thought | /5 | |
| Creating effective examples | /5 | |

---

**Compare your solutions with the answer key!**
