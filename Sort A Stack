#include <bits/stdc++.h> 
void insert_into_stack(stack<int> &st, int val){
	if(st.empty()|| st.top()<=val){
		st.push(val);
		return ;
	}
	int top = st.top();
	st.pop();
	insert_into_stack(st,val);
	st.push(top);
}
void sortStack(stack<int> &st)
{
	if(st.empty()|| st.size()==1)return;
	int top = st.top();
	st.pop();
	sortStack(st);
	insert_into_stack(st,top);
}
