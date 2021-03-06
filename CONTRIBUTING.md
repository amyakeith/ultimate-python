# Contributing

Thanks for taking the time to understand how you can contribute to the
Ultimate Python Study guide!

Please take a look at the [code of conduct](CODE_OF_CONDUCT.md) before
proceeding further.

---

The repository consists of documentation and Python modules. If you intend
to contribute by creating or updating resources of either type, please
review the standards defined in the upcoming sections to learn how you
can make a big impact for the developers consuming this content.

## README documentation

The [README](README.md) is important because it is the most frequently viewed
page in this repository. As such, any changes that are made to this page
must be legitimate and meaningful. Specifically:

- All Python modules must be referenced in the ToC
- All links must point to HTTPS resources that return a `2xx` status
- External Python documentation must be useful for newcomers and professionals
- External GitHub repositories should have at least 1k stars
- External practice resources must have Python exercises

## Python modules

Every Python module is a lesson which helps developers build their own
intuition for core Python. The modules tend to avoid physical I/O operations
as they may be run in a constrained environment like a web browser.

### Standard block

Every standalone Python module consists of the following:

```python
# Main function
def main():
    # Assertion comments
    assert 1 + 1 == 2
    assert True is not False


# Main function conditional
if __name__ == "__main__":
    main()
```

If the module involves additional functions and classes, they are placed
above the `main` function. Additionally, module-level constants are
defined with the `_UNDER_SCORE_FIRST` convention.

### Code coverage

Each module should have 80-100% code coverage with the [test runner](runner.py).
The reason for this high standard is that the repository code is relatively
simple. All interactive learning tends to revolve around the `main` function
since that is where the assertions are. That way, developers immediately know
when they make a mistake in the module. This is valuable feedback because it
helps them improve quickly.

To validate code coverage, run the following commands:

```bash
$ coverage run -m runner
$ coverage html
$ open htmlcov/index.html
```
