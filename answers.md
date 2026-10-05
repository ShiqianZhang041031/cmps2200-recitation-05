# Recitation 05

Name (Team Member 1): Shiqian Zhang

Name (Team Member 2):

## Question 3

The work of `get_positions` is $O(k)$ because scan processes the counts array, which has $k+1$ elements. The span is $O(\log k)$ assuming the efficient parallel implementation of scan from class.

## Question 5

The work of `construct_output` is $O(n)$ because it loops through all $n$ elements of the input once. The span is also $O(n)$ because the loop is sequential.

## Question 6

The work of `supersort` is $O(n+k)$. `count_values` takes $O(n+k)$ work, `get_positions` takes $O(k)$ work, and `construct_output` takes $O(n)$ work.

The span is $O(n+k)$ because `count_values` and `construct_output` are sequential in this implementation and therefore have linear span.

## Question 8

The work of `count_values_mr` is $O(n+k)$ because the map-reduce processes the $n$ input elements and the final counts array has $k+1$ entries. With a parallel map-reduce implementation, the reductions can be performed using balanced reduction trees, so the span is logarithmic rather than linear. The span is $O(\log n)$, assuming the map-reduce sequence operations are implemented in parallel.