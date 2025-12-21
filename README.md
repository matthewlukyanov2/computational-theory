# computational-theory
# G00421514 Matthew Lukyanov

This project is based off the requirements given and the work is structured to demonstrate my understanding of binary operations used in SHA-256 and  generation and verification of SHA-256 constants throughout.

The notebook combines **Python code**, **NumPy**, and **Markdown explanations** to present a clear technical overview.


## Repository Structure
```
.
├── .gitignore         # Python-specific ignores
├── problems.ipynb     # Main assessment notebook of all problems
├── README.md          # Project overview and setup instructions

```

All work is contained in a single reproducible notebook, as required by the assessment instructions.


## Requirements

- **Python 3.10+**
- **Jupyter Notebook**
- **NumPy**

You can install the required package using:
```bash
pip install numpy
```

No external data files are required.


## How to Run

Clone the repository:
```bash
git clone <repository-url>
cd <repository-name>
```

Launch Jupyter Notebook:
```bash
jupyter notebook
```

Open `problems.ipynb`.

Run the notebook cells from top to bottom to reproduce all results.

All outputs (tests, verification steps, and demonstrations) are generated within the notebook.


## Contents Summary

### Problem 1 – Binary Words and Operations

Implementation and explanation of the logical and rotation functions used in SHA-256 including

- Parity, Ch, Maj
- Uppercase Σ (Sigma) functions
- Lowercase σ (sigma) functions

Each function is documented, explained in Markdown, and tested with examples.

### Problem 2 – Fractional Parts of Cube Roots

- Generation of the first 64 prime numbers
- Calculation of cube roots
- Extraction of the first 32 bits of fractional parts
- Conversion to hexadecimal constants
- Verification against the official SHA-256 constants from FIPS 180-4

### Problem 3 – Padding

Implementation of a generator function `block_parse(msg)` that

- Applies SHA-256 padding rules
- Yields 512-bit message blocks
- Correctly handles edge cases (empty messages, multi-block padding)

Tested using messages of varying lengths.

### Problem 4 – Hash Computation

Implementation of the SHA-256 compression function as defined in Section 6.2.2 of FIPS 180-4

- Message schedule expansion
- 64-round compression loop
- State update and output hash

Intermediate overflow warnings are expected and consistent with unsigned 32-bit arithmetic.

### Problem 5 – Passwords

Analysis of three unsalted single-round SHA-256 password hashes:

- Password recovery using dictionary-based reasoning
- Explanation of why the attack succeeds
- Discussion of best practices for secure password storage (salting, key stretching, bcrypt/scrypt/Argon2)

## Reproducibility

This repository is fully reproducible:

- All constants are derived programmatically
- All tests are self-contained
- No external services or datasets are required

A reviewer can clone the repository and execute the notebook with minimal setup.

## Use of AI Assistance

Claudeai (Anthropic) and Chatgpt (OpenAI) were used as support tools during the development process to improve any code documentation or markdown explanations, review the structure or readabiity and debugging syntax errors and troubleshoot implementation issues.

All implementations were written, tested and verified by I, the author. AI assistance was not as a substitute for understanding or original work.


## References

- NIST, Secure Hash Standard (SHS), FIPS PUB 180-4, 2015  
  https://nvlpubs.nist.gov/nistpubs/FIPS/NIST.FIPS.180-4.pdf

- NumPy Documentation  
  https://numpy.org/doc/stable/

- OWASP Password Storage Cheat Sheet  
  https://cheatsheetseries.owasp.org/cheatsheets/Password_Storage_Cheat_Sheet.html

- RFC 9106 – Argon2 Password Hashing Function  
  https://www.rfc-editor.org/rfc/rfc9106.html

- Python Standard Library
  https://docs.python.org/3/library/stdtypes.html#int.from_bytes) and [to_bytes](https://docs.python.org/3/library/stdtypes.html#int.to_bytes

- How does SHA-256 work? Video
  https://youtu.be/f9EbD6iY9zI

- Anthropic, Claude
  https://claude.ai

- OpenAI, ChatGPT  
  https://openai.com/chatgpt