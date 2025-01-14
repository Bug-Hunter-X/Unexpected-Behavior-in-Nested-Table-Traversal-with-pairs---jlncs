# Lua Nested Table Traversal Bug
This repository demonstrates a potential bug in Lua when traversing nested tables using the `pairs` iterator. The issue arises from the fact that `pairs` does not guarantee a specific order of iteration. If the table's structure is modified during iteration (e.g., keys are added or removed), the behavior may become unpredictable.

## Bug Description
The provided `bug.lua` file contains a function `foo` that recursively iterates through a nested table using `pairs`. However, if the nested tables are modified during the traversal, the iteration may skip or repeat elements, leading to incorrect results.

## Solution
The `bugSolution.lua` file demonstrates a solution that uses a manual iteration approach to avoid the issues caused by the unpredictable ordering of `pairs`. This approach ensures that all elements are visited regardless of modifications during iteration.

## How to Reproduce
1. Clone this repository.
2. Run `bug.lua`.
3. Observe the potential unexpected behavior.
4. Run `bugSolution.lua` to see the corrected behavior.