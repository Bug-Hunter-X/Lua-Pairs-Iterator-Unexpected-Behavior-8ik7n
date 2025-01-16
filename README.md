# Lua Pairs Iterator Bug

This repository demonstrates a potential issue with Lua's `pairs` iterator when dealing with nested tables that are modified during iteration.  The `bug.lua` file contains code that showcases the problem, while `bugSolution.lua` offers a solution.

**Problem:**

Lua's `pairs` iterator can produce unexpected results if you modify the table being iterated while the loop is running.  This is because the iterator maintains an internal state, and changes to the table's structure can disrupt this state.

**Solution:**

To solve this, create a copy of the table before iteration and use that copy in the loop to avoid unexpected changes and infinite loops.  The `bugSolution.lua` file provides this corrected implementation.  Consider using alternative iteration methods or explicitly managing the table's structure if creating a copy is undesirable for performance reasons.