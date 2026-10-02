# Elastic Query Examples

## Suspicious Process Execution

```json
{
  "query": {
    "bool": {
      "must": [
        {"match": {"event.category": "process"}},
        {"match": {"process.name": "powershell.exe"}}
      ]
    }
  }
}
```

## Failed Authentication Activity

```json
{
  "query": {
    "bool": {
      "must": [
        {"match": {"event.category": "authentication"}},
        {"match": {"event.outcome": "failure"}}
      ]
    }
  }
}
```

## Service Creation

```json
{
  "query": {
    "bool": {
      "must": [
        {"match": {"event.category": "process"}},
        {"match": {"process.parent.name": "services.exe"}}
      ]
    }
  }
}
```

---

Use Elastic queries to start focused hunting and validation workflows.
