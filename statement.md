#include <functional>
#include <iostream>

int main() {
    const std::function<std::size_t (const std::size_t)> f_fib =
    [&f_fib](const std::size_t v) {
    if (v <= 1)
        return v;

    return f_fib(v - 2) + f_fib(v - 1);
    };

    std::cout << f_fib(25);     // 75025
}