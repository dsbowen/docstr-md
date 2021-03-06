# Docstring-Markdown

Docstring-Markdown is a fast and easy way to make beautiful documentation markdown files.

## Why Docstring-Markdown

It's time to share your awesome new package with the world. And... get ready to spend the next week making your docs. Or, make beautiful docs with Docstring-Markdown in just a few lines of code.

## Installation

```
$ pip install docstr-md
```

## Quickstart

First, clone a test file from the Docstring-Markdown repo.

```bash
$ curl https://raw.githubusercontent.com/dsbowen/docstr-md/master/test.py --output test.py
```

The example `test.py` uses sklearn formatted docstrings. Let's convert it to markdown.

```python
from docstr_md.python import PySoup, compile_md
from docstr_md.src_href import Github

src_href = Github('https://github.com/dsbowen/docstr-md/blob/master')
soup = PySoup(path='test.py', parser='sklearn', src_href=src_href)
compile_md(soup, compiler='sklearn', outfile='test.md')
```

You'll now have a `test.md` file in your current directory. [This](test.md) is what it looks like rendered.

## Citation

```
@software{bowen2020docstr-md,
  author = {Dillon Bowen},
  title = {Docstring-Markdown},
  url = {https://dsbowen.github.io/docstr-md/},
  date = {2020-06-04},
}
```

## License

Users must cite this package in any publications which use it.

It is licensed with the MIT [License](https://github.com/dsbowen/docstr-md/blob/master/LICENSE).