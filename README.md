# AI_assignment-4

1. Map Coloring Australia using CSP:-
   Variables (Each state is a variable) - WA, NT, SA, Q, NSW, V, T
   Domain (Each state can take) - Red, Green, Blue
   Constraints (Neighbouring states cannot have the same color)
   Constraint Graph
    You can draw like this:
    -WA connected to NT, SA
    -NT connected to WA, SA, Q
    -SA connected to almost all
   Backtracking:
   a) Start with empty assignment
   b) Pick a state (say WA)
   c) Assign a color (Red)
   d) Move to next state (NT)
   e) Try a color
      If conflict → try next color
   f) If no color works → go back (backtrack)
   g) Continue until all states are assigned
   Why Backtracking?
   a) We try all possibilities
   b) But we stop early when constraint fails
   c) So it is efficient
2. Telangana Map Coloring
   Each district is like a node in a graph. According to the Four Color Theorem: Any map can be colored using at most 4 colors
   More districts → more recursive calls
   But same algorithm works
   Define districts
   Define neighbors
   Run backtracking
   Show output
3. Sudoku CSP
   Variables- each empty cell in 9×9 grid
   Domain- {1,2,3,4,5,6,7,8,9}
   Constraints:-
   a) Row constraint → no duplicates
   b) Column constraint → no duplicates
   c) Box constraint (3×3) → no duplicates
   How CSP Solves Sudoku:-
   a) Find an empty cell (0)
   b) Try numbers 1–9
   c) Check if row, column and box are safe
   b) If valid → assign
   e) Move to next empty cell
   f) If stuck → backtrack
   This is constraint propagation + backtracking
   a) Constraint → reduces choices
   b) Backtracking → tries alternatives
   This is efficient because
   a) Invalid numbers are rejected early
   b) Reduces search space
4. Cryptarithmetic Puzzle
   Variables- S, E, N, D, M, O, R, Y
   Domain- 0-9
   Constraints-
   1. All letters must have different digits
   2. First letters cannot be zero - S ≠ 0, M ≠ 0
   3. Arithmetic must be correct
   We try all possible assignments using permutations
   1. Assign digits to letters
   2. Form numbers: SEND = 1000S + 100E + ...
   3. Check equation
   4. If true → solution found
   Why This is CSP?
   - Variables → letters
   - Domain → digits
   - Constraints → uniqueness + equation

   
   
