# Flash Content (DEMO Schema)

`flash/index.html` now loads only these files:

- `./content/@01.json`
- `./content/@02.json`
- ...
- `./content/@12.json`

Old `01.json` to `12.json` schema is not used anymore.

## Required schema

Each `@NN.json` file should follow the structure from `g:/DEMO.json`:

```json
{
  "id": "01",
  "flow": { "type": "SIGNAL->RESPONSE", "order": 1 },
  "name": { "concept": "INPUT -> PROCESS -> OUTPUT", "alias": "Function 01" },
  "hardware": { "required": [], "optional": [] },
  "learn": { "concept": "", "whyItWorks": "", "keyInsight": "", "realWorld": "" },
  "system": { "input": "", "process": "", "output": "" },
  "howItWorks": { "steps": [], "variables": [{ "name": "", "range": "" }] },
  "observe": {
    "visual": { "led": "", "buzzer": "" },
    "data": { "enabled": false, "type": "none", "description": "", "parameters": [] }
  },
  "run": { "steps": [], "expected": "" },
  "explore": { "tune": [{ "parameter": "", "effect": "" }], "experiments": [] }
}
```

## UI mapping

- Left menu title: `name.alias`
- Meta tag: `flow.type`
- Learn tab: `learn.*` and `system.*`
- The Code tab: `howItWorks.steps`, `howItWorks.variables`
- Flash & Play tab: `observe.*`, `run.*`, `explore.*`
