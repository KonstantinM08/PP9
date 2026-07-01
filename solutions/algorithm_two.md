```mermaid
graph TD
  A([Start: evaluate_sequence arr, len]) --> B[Initialize state = 0, i = 0]
  B --> C{i < len}
  C -- Yes --> D{arr[i] < 0}
  C -- No --> H{switch state}
  D -- Yes --> E[state = -1]
  D -- No --> F{arr[i] == 0}
  F -- Yes --> G[state = 0]
  F -- NO --> H1[state = 1]
  E --> I{state == 1}
  G --> I
  H1 --> I
  I -- Yes --> H
  I -- No --> J[i++]
  J --> C
  H --> K{case 1}
  K -- Yes --> L([Return true])
  K -- Default --> M([Return false])
```
