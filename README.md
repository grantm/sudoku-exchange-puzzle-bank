# Sudoku Exchange "Puzzle Bank"

This repository contains several hundred thousand Sudoku puzzles that were
computer generated for use by the [Sudoku Exchange](https://sudokuexchange.com/)
web site.

The puzzles were generated using the
[QQWing Sudoku](https://github.com/stephenostermiller/qqwing) software, which
ensure that each puzzle has a unique solution.
The generated puzzles were then graded using
[Sukaku Explainer](https://github.com/SudokuMonster/SukakuExplainer) and
sorted into four 'buckets':

| Filename            | Difficulty Rating |
| ------------------- | ----------------- |
| [easy.txt][1]       | < 1.5             |
| [medium.txt][2]     | < 2.5             |
| [hard.txt][3]       | < 5.0             |
| [diabolical.txt][4] | ≥ 5.0             |

Each text file has one puzzle per line, represented as three space-separated
fields and a Unix-style line-ending, for a total of 100 bytes per record:

     12 bytes of SHA1 hash of the digits string (for randomising order)
     81 bytes of puzzle digits
      4 bytes of rating (nn.n)
      3 bytes of white-space (including the linefeed);
    100 bytes total

### License

The data set is dedicated to the [public domain](LICENSE.txt).

[1]: https://github.com/grantm/sudoku-exchange-puzzle-bank/raw/master/easy.txt
[2]: https://github.com/grantm/sudoku-exchange-puzzle-bank/raw/master/medium.txt
[3]: https://github.com/grantm/sudoku-exchange-puzzle-bank/raw/master/hard.txt
[4]: https://github.com/grantm/sudoku-exchange-puzzle-bank/raw/master/diabolical.txt
