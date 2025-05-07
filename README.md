# AI-chess-engines
### How to Download LCZero Engine

1. **Go to the official LCZero download page**:
   [Download LCZero](https://lczero.org/play/download/)

2. **Choose the appropriate version for your system**:

   * **Windows**: Select the Windows version (x86\_64 or ARM).
   * **macOS**: Choose the macOS version.
   * **Linux**: Select the version for your distribution (x86\_64 or ARM).

3. **Integration with your code**:
   The code should be updated in the function `Function to Get the Best Move from the lc0 (one best move)`, like this:

   ```python
   lc0_path = Path("your_path_to_lc0/lc0.exe")
   ```
