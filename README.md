# Elixir Enum.each List Modification

This repository demonstrates a common mistake when working with lists and `Enum.each` in Elixir. The example shows that modifying a list directly within an `Enum.each` iteration does not affect the original list.

**Problem:**
The code attempts to remove the element '3' from the list while iterating through it. However, due to immutability, the list remains unchanged. The reassignment to `list` within the function creates a new local variable, and not changing the original list in the loop

**Solution:**
Instead of attempting to modify the list in place, the solution uses `Enum.filter` to create a new list containing only the elements that satisfy a given condition, effectively removing the element.