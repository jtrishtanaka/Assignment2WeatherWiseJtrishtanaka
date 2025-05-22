# Before/After Example 3: Natural Language Parsing Function

## Initial Prompt

```
Write a function to understand questions like “Weather in Paris tomorrow?”
```

## Initial AI-Generated Code (Before)

```python
def parse_question(q):
    return "Port Louis", 0
```

## My Analysis

- Hardcoded response
- No regex or keyword checking
- No dynamic handling of different cities/days

## My Follow-up Prompt

```
Make the function detect a city from a question, plus whether it refers to today, tomorrow, or the day after.
```

## Improved AI-Generated Code (After)

```python
def parse_question(question):
    import re
    location_match = re.search(r"in ([a-zA-Z\s]+)", question)
    location = location_match.group(1).strip() if location_match else "Port Louis"
    day_offset = 0
    if "tomorrow" in question.lower():
        day_offset = 1
    elif "day after" in question.lower():
        day_offset = 2
    return location, day_offset
```

## Why This Prompting Strategy Was Effective

- Gave concrete input/output expectations
- Suggested regex as a solution
- Provided examples of valid input cases