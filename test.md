# Sum of first n natural numbers
if $$n = 4$$ then sum bill be $$1 + 2 + 3 + 4 = 10$$.

More formally

$$\sum_{i=1}^{n} i \times (i + 1)$$

# Just Test

<details>
  <summary> C++ Code </summary>
  
  ```c++
  #include <bits/stdc++.h>
  using namespace std;
  int main() {
        int n;
        cin >> n;
        int arr[n];
        for (int i = 0; i < n; i++) {
            cin >> arr[i];
        }
        int sum = 0;
        for (int i = 0; i < n; i++) {
            sum += arr[i];
        }
        cout << sum;
        return 0;
  }
  ```
</details>

> :warning: **Warning:** Do not push the red button
> :brain: :brain: :brain: **Bring your brain with you:**

<iframe width="560" height="315" src="https://www.youtube.com/embed/pFPrxL8ZidY" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
