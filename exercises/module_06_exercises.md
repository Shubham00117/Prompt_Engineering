# 📝 Module 6 Exercises: Production and Integration

---

## Exercise 6.1: API Call Structure

Write the API call code for different providers.

**Task 1: OpenAI API Call**
```python
# Complete this function for OpenAI

def generate_with_openai(
    prompt: str,
    system_message: str = "You are a helpful assistant",
    model: str = "gpt-4",
    temperature: float = 0.7,
    max_tokens: int = 1000
) -> str:
    """
    Call OpenAI API and return response text.
    
    Handle:
    - API errors
    - Rate limits
    - Timeouts
    """
    # Your implementation:
    pass
```

**Task 2: Claude API Call**
```python
# Complete this function for Claude

def generate_with_claude(
    prompt: str,
    system_message: str = None,
    model: str = "claude-3-opus-20240229",
    max_tokens: int = 1024
) -> str:
    """
    Call Claude API and return response text.
    """
    # Your implementation:
    pass
```

---

## Exercise 6.2: Error Handling

Implement comprehensive error handling.

```python
from enum import Enum

class APIErrorType(Enum):
    RATE_LIMIT = "rate_limit"
    TIMEOUT = "timeout"
    INVALID_REQUEST = "invalid_request"
    SERVER_ERROR = "server_error"
    AUTH_ERROR = "auth_error"
    UNKNOWN = "unknown"

class APIResponse:
    def __init__(self, success: bool, data=None, error_type=None, message=""):
        self.success = success
        self.data = data
        self.error_type = error_type
        self.message = message

def call_api_with_handling(prompt: str) -> APIResponse:
    """
    Call API and return standardized response.
    
    Implement handling for:
    - Rate limit (429) - suggest retry after
    - Timeout - log and return error
    - Bad request (400) - include validation info
    - Server error (500) - retry with backoff
    - Auth error (401/403) - clear error message
    """
    # Your implementation:
    pass
```

---

## Exercise 6.3: Retry Logic

Implement sophisticated retry logic.

```python
import time
from typing import Callable, Optional

def retry_with_exponential_backoff(
    func: Callable,
    max_retries: int = 3,
    base_delay: float = 1.0,
    max_delay: float = 60.0,
    exponential_base: float = 2.0,
    jitter: bool = True
) -> Optional[any]:
    """
    Retry a function with exponential backoff.
    
    Implement:
    - Exponential delay increase
    - Maximum delay cap
    - Optional jitter (randomness)
    - Logging of retry attempts
    """
    # Your implementation:
    pass

# Test with:
def unreliable_api_call():
    import random
    if random.random() < 0.7:
        raise Exception("API Error")
    return "Success"
```

---

## Exercise 6.4: Batch Processing

Design a batch processing system.

```python
from typing import List, Dict
import asyncio

async def process_prompts_batch(
    prompts: List[str],
    batch_size: int = 5,
    rate_limit_per_minute: int = 60,
    timeout_seconds: int = 30
) -> List[Dict]:
    """
    Process multiple prompts efficiently.
    
    Implement:
    - Batch processing
    - Rate limiting
    - Progress tracking
    - Error handling per item
    - Results aggregation
    
    Returns list of:
    {
        "prompt": str,
        "response": str or None,
        "success": bool,
        "error": str or None,
        "latency_ms": int
    }
    """
    # Your implementation:
    pass
```

---

## Exercise 6.5: Logging System

Create a comprehensive logging system.

```python
import logging
from datetime import datetime
from typing import Dict, Any

class PromptLogger:
    """
    Log all prompt interactions with relevant metadata.
    """
    
    def __init__(self, log_file: str = "prompts.log"):
        """Initialize logger with file and console output."""
        # Setup logging:
        pass
    
    def log_request(
        self,
        prompt: str,
        model: str,
        parameters: Dict[str, Any],
        request_id: str = None
    ) -> str:
        """
        Log outgoing request.
        Return request_id for matching with response.
        """
        pass
    
    def log_response(
        self,
        request_id: str,
        response: str,
        tokens_used: int,
        latency_ms: int,
        success: bool
    ):
        """Log the response with metrics."""
        pass
    
    def log_error(
        self,
        request_id: str,
        error_type: str,
        error_message: str
    ):
        """Log an error."""
        pass
    
    def get_metrics(self, time_range_hours: int = 24) -> Dict:
        """
        Get aggregated metrics.
        
        Returns:
        {
            "total_requests": int,
            "success_rate": float,
            "avg_latency_ms": float,
            "total_tokens": int,
            "error_breakdown": {error_type: count}
        }
        """
        pass
```

---

## Exercise 6.6: Configuration Management

Create a configuration system for prompts.

```python
from dataclasses import dataclass
from typing import Dict, Any
import json
import os

@dataclass
class PromptConfig:
    name: str
    version: str
    model: str
    temperature: float
    max_tokens: int
    system_prompt: str
    user_prompt_template: str
    metadata: Dict[str, Any]

class PromptConfigManager:
    """
    Manage prompt configurations with versioning.
    """
    
    def __init__(self, config_dir: str = "./prompts"):
        self.config_dir = config_dir
    
    def save_config(self, config: PromptConfig) -> str:
        """
        Save configuration to file.
        Return file path.
        
        File format: {name}_v{version}.json
        """
        pass
    
    def load_config(self, name: str, version: str = "latest") -> PromptConfig:
        """
        Load configuration by name and version.
        If version="latest", load most recent.
        """
        pass
    
    def list_versions(self, name: str) -> List[str]:
        """List all versions of a prompt config."""
        pass
    
    def compare_versions(self, name: str, v1: str, v2: str) -> Dict:
        """
        Compare two versions.
        Return dict of differences.
        """
        pass
```

---

## Exercise 6.7: Monitoring Dashboard Data

Design data collection for a monitoring dashboard.

```python
from datetime import datetime
from collections import defaultdict
from typing import List, Dict

class PromptMetricsCollector:
    """
    Collect metrics for dashboard display.
    """
    
    def __init__(self):
        self.requests = []
    
    def record_request(
        self,
        prompt_name: str,
        model: str,
        success: bool,
        latency_ms: int,
        input_tokens: int,
        output_tokens: int,
        error_type: str = None
    ):
        """Record a single request."""
        pass
    
    def get_hourly_stats(self, hours: int = 24) -> List[Dict]:
        """
        Get stats grouped by hour.
        
        Returns list of:
        {
            "hour": "2024-03-15 14:00",
            "total_requests": int,
            "success_rate": float,
            "avg_latency": float,
            "total_tokens": int,
            "estimated_cost": float
        }
        """
        pass
    
    def get_prompt_breakdown(self) -> Dict[str, Dict]:
        """
        Get stats broken down by prompt name.
        
        Returns:
        {
            "prompt_name": {
                "total_calls": int,
                "success_rate": float,
                "avg_latency": float
            }
        }
        """
        pass
    
    def get_error_summary(self) -> Dict[str, int]:
        """Get error counts by type."""
        pass
```

---

## 🎯 Challenge Exercise: Build a Complete Prompt Service

Build a production-ready prompt service.

**Component 1: Prompt Definition**
```python
class EmailClassifier:
    """Production email classification service."""
    
    SYSTEM_PROMPT = """
    [Write your system prompt]
    """
    
    # Define your prompt here
```

**Component 2: API Integration**
```python
class EmailClassifierService:
    def __init__(self, api_key: str, model: str = "gpt-3.5-turbo"):
        # Initialize with config
        pass
    
    def classify(self, email_subject: str, email_body: str) -> Dict:
        # Implement with error handling
        pass
    
    def classify_batch(self, emails: List[Dict]) -> List[Dict]:
        # Batch processing
        pass
```

**Component 3: Logging and Monitoring**
```python
# Add logging throughout the service
```

**Component 4: Testing**
```python
def test_email_classifier():
    """
    Test cases for the email classifier.
    """
    test_cases = [
        {"subject": "...", "body": "...", "expected": "..."},
        # Add more
    ]
    
    # Run tests and check accuracy
    pass
```

---

## Exercise 6.8: Capstone Project Planning

Plan your own capstone project.

**Project Planning Document:**

```markdown
# Capstone Project: [Title]

## Problem Statement
[What problem are you solving?]

## Target Users
[Who will use this?]

## Solution Overview
[High-level description]

## Prompts Required

### Prompt 1: [Name]
- Purpose:
- Type (zero-shot/few-shot/chain):
- Expected output format:

### Prompt 2: [Name]
- Purpose:
- Type:
- Expected output format:

## Architecture
[Diagram or description of data flow]

## Success Metrics
1.
2.
3.

## Implementation Timeline
- Week 1:
- Week 2:

## Risk Assessment
- Risk 1:
- Mitigation:

## Testing Plan
[How will you verify it works?]
```

---

## Exercise 6.9: Documentation

Create documentation for a prompt you've built.

```markdown
# [Prompt Name] Documentation

## Overview
[What does this prompt do?]

## Version
Current: v[X.Y]

## API Contract

### Input
```json
{
  "field1": "type",
  "field2": "type"
}
```

### Output
```json
{
  "result": "type",
  "metadata": {}
}
```

## Examples

### Example 1: [Normal case]
Input:
Output:

### Example 2: [Edge case]
Input:
Output:

## Error Handling
[How errors are communicated]

## Performance
- Latency: avg X ms
- Token usage: avg X tokens
- Cost per request: $X

## Changelog
[Version history]
```

---

## Exercise 6.10: Presentation

Prepare a presentation for your prompt engineering solution.

**Slide Outline:**

```
Slide 1: Title
- Project name
- Your name
- Date

Slide 2: Problem
- What problem did you solve?
- Why does it matter?

Slide 3: Solution
- High-level approach
- Key prompts used

Slide 4: Technical Details
- Prompt techniques
- Architecture

Slide 5: Demo
- Live demonstration or screenshots

Slide 6: Results
- Metrics achieved
- Comparison to baseline

Slide 7: Lessons Learned
- What worked
- What didn't
- Improvements for future

Slide 8: Q&A
- Contact info
- Resources
```

---

## ✅ Final Self-Assessment

Rate your overall course understanding (1-5):

| Module | Rating | Confidence |
|--------|--------|------------|
| 1. Foundations | /5 | |
| 2. Core Strategies | /5 | |
| 3. Advanced Techniques | /5 | |
| 4. Domain Applications | /5 | |
| 5. Evaluation | /5 | |
| 6. Production | /5 | |

**Areas for continued learning:**
1.
2.
3.

---

**Congratulations on completing all exercises! 🎉**
