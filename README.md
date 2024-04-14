# HPC
DATA COMPRESSION
LZ77 compression algorithm using OpenMP for parallelization.

### Libraries
```cpp
#include <bits/stdc++.h>
#include <omp.h>
```
- `bits/stdc++.h`: This is a header file that includes every standard library.
### Namespaces
```cpp
using namespace std;
using namespace std::chrono;
```
- `using namespace std;`: This allows the usage of standard library functions and objects without prefixing them with `std::`.
- `using namespace std::chrono;`: This allows the usage of time-related functions and objects from the `<chrono>` library without prefixing them with `std::chrono::`.

### Struct Definition
```cpp
struct token {
    int offset;
    int length;
    char next;
};
```
- Defines a `struct` named `token`, which represents a token in the LZ77 compression algorithm. It consists of an offset, length, and the next character.

### LZ77 Compression Function
```cpp
vector<token> lz77_compress(string input, int window_size, int buffer_size) {
}
```
- Implements the LZ77 compression algorithm. It takes input string, window size, and buffer size as parameters and returns a vector of tokens representing the compressed data.

### OpenMP LZ77 Compression Function
```cpp
void omp_lz77_compress(string input, int window_size, int buffer_size, int threads, vector<vector<token>> *array_tokens) {
}
```
- This function parallelizes the LZ77 compression using OpenMP. It divides the input string among multiple threads, compresses each part separately, and stores the results in a vector of vectors of tokens.

### Main Function
```cpp
int main() {
}
```
- The main function of the program.
- It reads input from a file, performs LZ77 compression sequentially and in parallel with different numbers of threads, and records the compression time and size of the compressed data in output files.

### Explanation
- The main loop in the `main` function iterates 10 times, each time compressing the input string sequentially and in parallel with different numbers of threads.
- Performance metrics like compression time and size of the compressed data are recorded in output files.
- OpenMP is utilized to parallelize the compression process, and the number of threads used is varied from 1 to 16.
