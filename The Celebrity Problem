#include <bits/stdc++.h> 
/*
	This is signature of helper function 'knows'.
	You should not implement it, or speculate about its implementation.

	bool knows(int A, int B); 
	Function 'knows(A, B)' will returns "true" if the person having
	id 'A' know the person having id 'B' in the party, "false" otherwise.
*/

int findCelebrity(int n) {
	// here 'i' is treated as potential celebrity
 	int i = 0, j = 1;
	while(i < n and j < n) {
		// if 'i' knows 'j' then 'i' can't be a celebrity
		if(knows(i, j)) {
			i = j;
			j++;
		}
		else {
			if(knows(j, i)) j++;
			// if 'j' doesn't know 'i' then 'i' can't be a celebrity
			else {
				i = j;
				j++;
			}
		}
	}
	if(i >= n) return -1;
	// checking for -1 case
	for(int k = 0; k < n; k++) {
		if(k == i) continue;
		if((!knows(k, i)) || (knows(i, k))) return -1;
	}
	return i;
}
