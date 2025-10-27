1. The easiest issues to fix were the naming convention changes and the default list argument. Both were simple edits that did not require much thought. The hardest issue was the bare except warning because it needed some reasoning about which specific error could happen and how to handle it safely.

2. The unused import logging warning felt like a false positive. At first it was correct since logging was not used, but once proper exception handling was added, the logging import became necessary and the warning was no longer valid.

3. I would use tools like Pylint, Flake8, and Bandit both locally and in CI. Locally, they can run through pre commit hooks to catch issues early. In CI, they can run automatically on every push or pull request to maintain code quality and prevent bad code from being merged.

4. After applying the fixes, the code became cleaner and more consistent. The new naming style improved readability, and the safer defaults reduced the risk of subtle bugs. Type checks and better exception handling made the program more reliable and easier to maintain.