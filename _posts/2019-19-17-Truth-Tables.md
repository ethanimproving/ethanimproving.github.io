A simple blog post to explore the 16 possible boolean operators.

## 1. NOT Operator

| a | !a |
|---|---|
| true | false |
| false | true |

## 2. OR Operator

| a     | b     | a &#124;&#124; b |
|-------|-------|------------|
| true  | true  | true       |
| true  | false | true       |
| false | true  | true       |
| false | false | false      |

## 3. AND Operator

| a     | b     | a && b |
|-------|-------|------------|
| true  | true  | true       |
| true  | false | false      |
| false | true  | false      |
| false | false | false      |

## 4. Exclusive OR Operator

| a     | b     | XOR |
|-------|-------|------------|
| true  | true  | false      |
| true  | false | true       |
| false | true  | true       |
| false | false | false      |

## 5. Contradiction

| a     | b     | false |
|-------|-------|------------|
| true  | true  | false      |
| true  | false | false      |
| false | true  | false      |
| false | false | false      |

## 6. Joint Denial

| a     | b     | NOR |
|-------|-------|------------|
| true  | true  | false      |
| true  | false | false      |
| false | true  | false      |
| false | false | true       |

## 7. Converse Nonimplication

| a     | b     | ↚ |
|-------|-------|------------|
| true  | true  | false      |
| true  | false | false      |
| false | true  | true       |
| false | false | false      |

## 8. Negation

| a     | b     |  ¬p |
|-------|-------|------------|
| true  | true  | false      |
| true  | false | false      |
| false | true  | true       |
| false | false | true       |

## 9. Material Nonimplication

| a     | b     |  ↛ |
|-------|-------|------------|
| true  | true  | false      |
| true  | false | true       |
| false | true  | false      |
| false | false | false      |

## 10. Logical Complement

| a     | b     |  ¬p |
|-------|-------|------------|
| true  | true  | false      |
| true  | false | true       |
| false | true  | false      |
| false | false | true       |

## 11. Sheffer Stroke

| a     | b     |  NAND |
|-------|-------|------------|
| true  | true  | false      |
| true  | false | true       |
| false | true  | true       |
| false | false | true       |

## 12. Projection

| a     | b     |  q |
|-------|-------|------------|
| true  | true  | true       |
| true  | false | false      |
| false | true  | true       |
| false | false | false      |

## 13. Material Condition

| a     | b     |  → |
|-------|-------|------------|
| true  | true  | true       |
| true  | false | false      |
| false | true  | true       |
| false | false | true       |

## 14. Projection

| a     | b     |  p |
|-------|-------|------------|
| true  | true  | true       |
| true  | false | false      |
| false | true  | true       |
| false | false | true       |

## 15. Converse Implication

| a     | b     |  ← |
|-------|-------|------------|
| true  | true  | true       |
| true  | false | true       |
| false | true  | false      |
| false | false | true       |

## 16. Tautology

| a     | b     |  true |
|-------|-------|------------|
| true  | true  | true       |
| true  | false | true       |
| false | true  | true      |
| false | false | true       |