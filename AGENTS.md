# AGENTS

This document provides guidance for contributors working with this repository.

## Style
- Use clear, inclusive and gender-neutral language.
- Avoid Latin abbreviations. Prefer full phrases such as "for example" and "that is".
- Do not include placeholder text such as "Lorem ipsum".
- Provide descriptive alternative text for all images.

## Testing
Run the following checks from the repository root before committing:

```bash
pip install -r tests/requirements.txt
python tests/no-bad-latin.py
python tests/lorem-ipsums.py
bash tests/test-file-size.sh
```

Additional checks:
- Run `python tests/validate-all-contributorsrc.py` when `.all-contributorsrc` is modified.
- Run `cffconvert --validate CITATION.cff` when `CITATION.cff` is changed.
- When editing book content, ensure it builds by running:
  ```bash
  cd book
  make deps  # first time only
  make book
  ```

## Git and pull requests
- Write descriptive commit messages and do not rewrite existing history.
- Keep pull requests focused and mention which tests were run.
