#include <bits/stdc++.h>
using namespace std;

static int t[102][1002];   // Static DP array

int knapSack(int wt[], int val[], int W, int n) {

    // Base case
    if (n == 0 || W == 0)
        return 0;

    // Memoization check
    if (t[n][W] != -1)
        return t[n][W];

    // Choice diagram
    if (wt[n-1] <= W) {

        // include + exclude
        return t[n][W] = max(
            val[n-1] + knapSack(wt, val, W - wt[n-1], n-1),
            knapSack(wt, val, W, n-1)
        );
    }

    else {
        // can't include
        return t[n][W] = knapSack(wt, val, W, n-1);
    }
}

int main() {

    int n = 4;
    int wt[]  = {1, 3, 4, 5};
    int val[] = {1, 4, 5, 7};
    int W = 7;

    // DP array initialize to -1
    memset(t, -1, sizeof(t));

    cout << "Maximum value = " << knapSack(wt, val, W, n);

    return 0;
}
