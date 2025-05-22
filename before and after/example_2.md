# Before/After Example 2: Menu Loop Improvement

## Initial Prompt

```
Make the weather app menu repeat even after selecting option 2.
```

## Initial AI-Generated Code (Before)

```python
while True:
    print("1. Check today’s weather")
    print("2. Visualise forecast")
    choice = input("Enter choice: ")
    if choice == '2':
        # Plot graph
        break  # This exits loop
```

## My Analysis

- The loop ends prematurely after one choice
- No re-display of menu after option 2
- User experience is broken

## My Follow-up Prompt

```
Please make the code loop back to the menu even after option 2. Don’t make me press Enter manually.
```

## Improved AI-Generated Code (After)

```python
while True:
    print("1. Check today’s weather")
    print("2. Visualise forecast")
    print("3. Exit")
    choice = input("Choose option: ").strip()
    if choice == '1':
        check_weather()
    elif choice == '2':
        visualise_forecast()
    elif choice == '3':
        break
    else:
        print("Invalid option")
```

## Why This Prompting Strategy Was Effective

- Clarified what “loop” behavior I wanted
- Explained UX frustration (Enter key)
- Encouraged graceful looping

---