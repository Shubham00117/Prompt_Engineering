# 📝 Module 4 Exercises: Domain-Specific Applications

---

## Exercise 4.1: Writing Improvement

Create a prompt that improves this poorly written paragraph.

**Original Text:**
```
The company is doing good. We made alot of money last year. 
the customers seem happy I think. We will do more marketing 
next year maybe and also hire people probably.
```

**Your improvement prompt:**
```
[Write a prompt that:
1. Specifies what to improve (grammar, clarity, professionalism)
2. Maintains the core message
3. Asks for a list of changes made]
```

**Test and document the result:**

---

## Exercise 4.2: Style Matching

Create a prompt that matches this writing style.

**Sample Style:**
```
Listen up, folks—here's the deal. You want results? 
You gotta put in the work. No shortcuts. No excuses. 
Just pure, relentless hustle. That's what separates 
winners from everybody else.
```

**Content to Rewrite in This Style:**
"Research shows that consistent effort is correlated with higher achievement rates."

**Your style-matching prompt:**
```
[Write the prompt]
```

---

## Exercise 4.3: Marketing Copy (PAS Framework)

Create marketing copy using the Problem-Agitation-Solution framework.

**Product:** A smart water bottle that tracks hydration

**Your PAS prompt:**
```
[Write a prompt that generates copy using PAS]
```

**Test for multiple audiences:**
- Fitness enthusiasts
- Busy professionals
- Health-conscious seniors

---

## Exercise 4.4: Social Media Variations

Create a prompt that generates multiple platform-specific posts.

**Product Launch:** New eco-friendly running shoes

**Your prompt asking for:**
- Twitter (280 char, hashtags)
- LinkedIn (professional, 100 words)
- Instagram (emoji, visual call-out)
- Facebook (casual, community-focused)

```
[Write your prompt]
```

---

## Exercise 4.5: Character Development

Create a detailed character using a structured prompt.

**Basic Info:**
- Name: Dr. Maya Chen
- Role: AI researcher who discovers something unsettling

**Your prompt for character development:**
```
[Write a prompt that generates:
- Background
- Motivation
- Fears
- Speech patterns
- A secret]
```

---

## Exercise 4.6: Code Generation

Create prompts for code generation with specific requirements.

**Task 1: API Endpoint**
```
Create a prompt for generating a REST API endpoint that:
- Language: Python/FastAPI
- Route: POST /users/register
- Validates email format
- Hashes password
- Returns user ID

[Your prompt]
```

**Task 2: Data Processing Function**
```
Create a prompt for a function that:
- Reads CSV file
- Filters rows by condition
- Aggregates data
- Includes type hints and docstring

[Your prompt]
```

---

## Exercise 4.7: Code Debugging

Create a debugging prompt for this code.

**Buggy Code:**
```python
def find_average(numbers):
    total = 0
    for num in numbers:
        total += num
    return total / len(numbers)

# Problems:
# - Crashes on empty list
# - Doesn't handle None in list
```

**Your debugging prompt:**
```
[Write a prompt that:
1. Identifies the bugs
2. Explains the issues
3. Provides fixed code
4. Adds test cases]
```

---

## Exercise 4.8: Data Extraction

Create a data extraction prompt for unstructured text.

**Input Text:**
```
Meeting Notes - March 15, 2024

Attendees: John Smith (Product), Sarah Lee (Engineering), 
Mike Brown (Design)

Key Decisions:
- Launch date moved to April 1st
- Budget increased to $50,000
- Need to hire 2 more developers

Action Items:
- Sarah: Update timeline by March 18
- Mike: Complete mockups by March 20
- John: Get budget approval by March 17
```

**Your extraction prompt:**
```
[Write a prompt that extracts to JSON with:
- Meeting date
- Attendees (name and role)
- Decisions (list)
- Action items (person, task, deadline)]
```

---

## Exercise 4.9: Customer Service Bot

Create a complete customer service system prompt.

**Business:** Online bookstore

**Create prompts for:**

**System Prompt:**
```
[Define identity, capabilities, limitations]
```

**Query Classification:**
```
[Classify incoming questions]
```

**Response Template:**
```
[Structure for different query types]
```

---

## Exercise 4.10: Escalation Logic

Create an escalation detection prompt.

**Conversation to Analyze:**
```
Customer: I've been waiting 3 weeks for my order!
Bot: I apologize for the delay. Let me check your order status.
Customer: This is ridiculous. I want a full refund NOW.
Bot: I understand your frustration. I can process a refund...
Customer: No, I want to speak to a manager. This is unacceptable.
```

**Your escalation prompt:**
```
[Write a prompt that:
1. Analyzes conversation for escalation signals
2. Identifies trigger(s)
3. Determines urgency
4. Creates handoff summary for human agent]
```

---

## 🎯 Challenge Exercise: Complete Content Pipeline

Build a content creation pipeline for a tech blog.

**Pipeline Steps:**

**Step 1: Topic Research Prompt**
```
Given a general theme, generate specific blog post ideas.

[Write prompt]
```

**Step 2: Outline Generation**
```
For a chosen topic, create a structured outline.

[Write prompt]
```

**Step 3: Section Writing**
```
Write individual sections based on outline.

[Write prompt with section-specific requirements]
```

**Step 4: Style Editing**
```
Edit for consistency and brand voice.

[Write prompt]
```

**Step 5: SEO Optimization**
```
Add SEO elements (title, meta, keywords).

[Write prompt]
```

**Test your pipeline with theme:** "AI in Healthcare"

---

## Exercise 4.11: Technical Documentation

Create documentation generation prompts.

**Code to Document:**
```python
def batch_process(
    items: List[dict],
    processor: Callable,
    batch_size: int = 10,
    on_error: str = "skip"
) -> List[dict]:
    # Process items in batches
    pass
```

**Your documentation prompt:**
```
[Generate comprehensive documentation including:
- Description
- Parameters (with types)
- Returns
- Raises
- Example usage
- Notes]
```

---

## Exercise 4.12: Tone Spectrum

Create 5 versions of this message in different tones:

**Original Message:** "The project deadline has been moved up by one week."

**Your prompt for tone variations:**
```
[Write a prompt that generates each tone:]

1. Formal/Corporate:
2. Friendly/Casual:
3. Urgent/Serious:
4. Encouraging/Positive:
5. Apologetic:
```

---

## ✅ Self-Assessment

Rate your understanding (1-5):

| Concept | Rating | Notes |
|---------|--------|-------|
| Writing improvement | /5 | |
| Style matching | /5 | |
| Marketing copy | /5 | |
| Code generation | /5 | |
| Code debugging | /5 | |
| Data extraction | /5 | |
| Customer service bots | /5 | |
| Technical documentation | /5 | |

---

**Practice with real-world scenarios from your work!**
