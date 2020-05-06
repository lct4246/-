#include <iostream>
using namespace std;

void find(int fri[], int n) {
	int group=0;
	int i;
	
	for (i = 0; i < n; ++i) {
		if (fri[i] != -1) {
			++group;
			int j = i;
			
			while (fri[j] != -1) {
				int next = fri[j];
				fri[j] = -1;
				j = next;
			}
		}
	}
	
	cout << group << endl;
}

int main(void) {
	int fri[10]={4, 7, 2, 9, 6, 0, 8, 1, 5, 3};
	find(fri, 10);
	
	return 0;
}
