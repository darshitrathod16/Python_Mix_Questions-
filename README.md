# Python_Mix_Questions-

# Python Mix Questions – Strings Practice

This repo has my practice notebook for Python strings and basic type handling. I solved these questions while learning Python for data science, and I wrote short comments in the notebook to explain why an answer works.

Strings look easy in the beginning, but they come up everywhere in real data work: cleaning column names, building file names, writing SQL text, parsing dates and fixing messy values. So I wanted to get the basics really strong.

---

## What's inside

The notebook is split into small sections. Each section has a few questions and my answers right below them.

| Section | What I practiced |
|---|---|
| **A. Creating strings** | Multiline strings, raw strings, triple quotes, single vs double quotes |
| **B. Add & multiply** | Concatenation, repeating strings, `join`, f-string padding, why `"a" + 5` fails |
| **C. Indexing** | Positive and negative indexes, `isalpha()`, `isdigit()`, swapping first and last character |
| **D. Slicing & reverse** | `[start:stop:step]`, reversing with `[::-1]`, slicing dates and file names |
| **E. Immutability & replace** | Why `s[0] = "D"` fails, `replace()` with a count, `partition()` and `split()` |
| **F. Delete variables** | `del` on variables and list items, `id()` before and after, name vs object |
| **G. Join, f-strings, format** | Three ways to build the same string, aligned table printing, zero padding |
| **K. Type casting** | Auto and forced casting, boolean strings, parsing `"1,234.56"` to float, `None` handling |
| **General mixed questions** | `len`, `ljust` / `rjust`, `strip`, `split`, `isdecimal`, palindrome check and more |

---

## A few things I learned

- **Strings are immutable.** You can't change a character in place. You make a new string instead, like `"D" + a[1:]`.
- **`join()` is better than `+`** when you combine many pieces, and it is cleaner to read too.
- **Raw strings (`r""`)** are the safe way to write Windows file paths, because backslashes stay as normal text.
- **Slicing never crashes** when the index is out of range (`s[100:]` gives `''`), but indexing does (`s[100]` gives an `IndexError`).
- **Three ways to format** the same output: f-strings, `.format()` and `format()`. They all work, f-strings are the easiest for me.
- **Booleans from text:** `bool("false")` is `True` because the string is not empty. The right way is `s.lower() == "true"`.
- **`del` removes the name**, not always the object. After `b = a` and `del a`, `b` still works.

---

## Quick example

Zero padding with three different methods:

```python
format(7, "04d")          # '0007'
f"{7:04d}"                # '0007'
"{:04d}".format(7)        # '0007'
```

Parsing a number with a comma safely:

```python
s = "1,234.56"
result = float(s.replace(",", ""))   # 1234.56
```

---

## How to run it

1. Clone this repo
   ```bash
   git clone <your-repo-link>
   cd <your-repo-folder>
   ```
2. Install Jupyter if you don't have it
   ```bash
   pip install notebook
   ```
3. Open the notebook
   ```bash
   jupyter notebook Python_Mix_Questions.ipynb
   ```

No extra libraries are needed. Everything uses plain Python.

---

## Files

```
├── Python_Mix_Questions.ipynb   # questions and solutions
└── README.md
```

---

## Why I made this

I learn best by writing the code myself, getting it wrong, and then understanding the mistake. This notebook is the record of that. I will keep adding more practice questions as I move to lists, dictionaries, functions and pandas.

Feel free to open it, try the questions yourself first, and compare with my answers. If you find a better way to solve any question, I would be happy to hear it.
