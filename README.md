# CSE 031 · Computer Organization

UC Merced coursework from **Fall 2023**, covering C programming, memory and pointers, MIPS assembly, procedures, recursion, and cache exercises.

The original lab files, two projects, notes, assignment PDFs, and saved answers are preserved in [CSE031.zip](CSE031.zip). This repository is an archive of coursework, with multiple exercise variants and debugging files; it is not a single application or a verified set of finished solutions.

## Explore the coursework

[Download the coursework archive](CSE031.zip), extract it, and open its `CSE031/` folder. GitHub does not expose ZIP members as individual source pages, so the paths below are **inside the archive**, relative to that folder. Folder spelling and capitalization match the original upload.

| Area | Path inside `CSE031/` | What to look for |
| --- | --- | --- |
| Early C exercises | `CSE 031 LAB/Lab_1/` | Averages, repetition, pseudocode, and the Lab 1 instructions |
| Pointers and debugging | `Lab_2/` | Pointer examples, array copying, string append, and original/revised average programs |
| Memory and structures | `Lab_3/` | Dynamic arrays, node structures, memory examples, and linked-list cycle detection |
| Arrays and representation | `Lab_4/` | `Array2D.c`, `MatrixMult.c`, and `MemCast.c` |
| First MIPS programs | `Lab_5/` | `myFirstExample.s`, `myFirstMIPS.s`, and Fibonacci variants |
| MIPS control flow | `Lab_6/` | Comparisons, Fibonacci, and even/odd summation |
| Procedure calls | `Lab_07/` | Paired C and MIPS `proc1`, `proc2`, and `proc3` examples |
| Recursion | `Lab_08/` | C recurrence examples and several MIPS translations |
| Branch exercises | `Lab_9/` | MIPS comparison programs and written answers |
| Cache exercises | `lab_10/` | Written answers and recorded macOS cache information |
| Word-search project | `Project1/` | `wordsearch.c` and five `puzzle*.txt` input files |
| Score-average project | `Project2/` | `avgScore.c` and `avgScore.s`: sorting, recursive summation, and dropping low scores |
| Notes | `Notes/` | Lecture notes and `asemblybasic.md` |

Assignment PDFs are included in Labs 1, 2, 4, 7, and 8. Saved executables, `.dSYM` bundles, `.DS_Store`, `__MACOSX/` metadata, and `tempCodeRunnerFile.c` fragments also remain in the upload; use the named source files when studying or building an exercise.

## Open and run individual exercises

**Prerequisites:** a ZIP extractor and text editor; a C compiler supporting C99 or later for `.c` files; MARS for the MIPS simulator exercises. The saved Lab 5 answers explicitly refer to MARS. The assembly uses simulator syscalls and pseudo-instructions, so it is not a native executable for a modern desktop CPU.

On Windows, extract the archive from the repository directory with PowerShell:

```powershell
Expand-Archive -LiteralPath .\CSE031.zip -DestinationPath .\coursework
```

The source folder is then `coursework/CSE031/`. On other systems, extract the ZIP with your usual archive tool.

### C: score-average project

From the extracted `CSE031/Project2/` directory, a GCC-compatible compiler command is:

```sh
gcc -std=c99 -Wall -Wextra avgScore.c -o avgScore
./avgScore
```

In PowerShell, use `./avgScore.exe` if the compiler creates an `.exe`. The program prompts for the number of assignments, each integer score, and the number of lowest scores to drop. Use 1–25 scores and a drop count from 0 to one less than the score count: the source does not validate these bounds, and dropping every score would divide by zero.

### MIPS: first example

Open `Lab_5/myFirstExample.s` in MARS, assemble it, then run it. Its source describes adding 10 to `$t1`, saving the result in `$s1`, and printing it. Other files include alternative attempts or incomplete exercises, so inspect each file and its assignment instructions before expecting a particular result.

**Verification:** the archive paths and extraction were checked, and the instructions above were reviewed against the source. C compilation and MARS execution have not been tested in the documentation environment. In particular, `Project2/avgScore.s` should not be assumed to reproduce the C version, and `Project1/wordsearch.c` has memory-handling issues, including calling `strlen` on puzzle rows without a stored null terminator.

## Original materials and attribution

The archive retains its original comments, filenames, assignment text, and attribution. For example, `Lab_5/myFirstExample.s` credits **Santosh Chandrasekhar** as the demo's author. This guide does not change the source or add a license.
