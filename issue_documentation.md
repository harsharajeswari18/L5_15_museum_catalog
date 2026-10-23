# Lab 5: Static Code Analysis — Issue Documentation

| Issue | Type | Original Line(s) | Description | Fix Approach |
|---|---|---|---|---|
| Long lines | Code quality/style | 6, 11 | Lines exceed the recommended length. | Split long statements across multiple lines. |
| Missing module docstring | Code quality | 1 | The Python module has no introductory documentation. | Added a module docstring. |
| Missing function docstrings | Code quality | 10, 15, 24, 31, 36, 40 | Functions lack descriptions. | Added docstrings describing function behavior. |
| Invalid function names | Code style | 10, 15, 24, 31, 36 | Function names use camelCase rather than snake_case. | Renamed functions using snake_case. |
| Unnecessary else | Code quality | 17 | An `else` follows a `return` statement unnecessarily. | Removed the `else` and de-indented the return statement. |
| Unused argument | Code quality | 15 | The `curator` argument is not used. | Renamed it `_curator` to indicate it is intentionally unused. |
| Unused import | Code quality | 2 | The `datetime` module is imported but not used. | Removed the unused import. |
| SQL injection risk | Security | 11 | SQL was constructed using string concatenation. | Used parameterized SQL queries. |
| Hardcoded password | Security | 7 | A password was stored directly in source code. | Removed the hardcoded credential. |
| Subprocess shell usage | Security | 37 | A subprocess call used `shell=True`. | Replaced the subprocess call with a direct `print()` because the operation only displays a message. |

## Summary

Static analysis was performed using Pylint, Bandit, and Flake8. The original Pylint score was 4.85/10. After improvements, the score reached 10.00/10. The final Bandit report identified no issues, and the final Flake8 check passed without errors.
