#include <iostream>

int customFibonacci(int A, int B, int N) {
    if (N == 1) return A;
    if (N == 2) return B;

    int prev1 = A;
    int prev2 = B;
    int current = 0;

    for (int i = 3; i <= N; ++i) {
        current = prev1 + prev2;
        prev1 = prev2;
        prev2 = current;
    }

    return current;
}

int main() {
    int A, B, N;
    std::cin >> A >> B >> N;

    int result = customFibonacci(A, B, N);

    std::cout << result << std::endl;

    return 0;
}
