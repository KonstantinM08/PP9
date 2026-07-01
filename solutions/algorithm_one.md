```mermaid
graph TD
  A([Start: transform_complex x]) --> B[Initialize result = 1, i = 1]
  B --> C{i <= x}
  C -- True --> D{i % 2 == 0}
  C -- False --> I([Return result])
  D -- True --> E[result += i]
  D -- False --> F[result *= i]
  E --> G{result > 1000}
  F --> G
  G -- True --> H[result -= 100]
  G -- False --> J[i++]
  H --> J
  J --> C
```
