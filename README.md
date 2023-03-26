# Diora Network Documentation


Diora [documentation](https://diora.network/docs).

## Requirements


## Contribute

Clone the project.

```bash
git clone https://github.com/diora-network/docs.git
```

Create a virtualenv for this project.

cd docs


Install the required libraries in your project's virtualenv.

```
pip install -r requirements.txt
```

You can now edit some files and check your changes live by running a local server.
You can access it at [localhost:3000](http://localhost:3000/).

```bash
./ serve.sh
```

Note: don't forget to activate/deactivate your virtualenv when you start/stop working on this project.

```bash
# activate: from the project folder
source .env/bin/activate

# deactivate: from everywhere
deactivate
```

## Contribution guideline

### Branches

If you are a technical writer with assigned issues, please work on a separate branch for each of them.

They should be named `d/[id of the issue]`

Example:

`git checkout -b d/24`

All other branches can be named with a short descriptive word.

Example:

`git checkout -b guidelines`

### Commits

Commits should start by a verb.

Example:

`fix typo in technical whitepaper`

### Markdown

When contributing to the documentation, please write one sentence per line.

This will not create a new paragraph as markdown require two blank line to create one.

It will help keep git diffs clearer.
When editing a file, if you see multiples sentences in one line, it would be welcomed if you split them.

Example:

```markdown
Hello, this is the first paragraph.
This is still the first paragraph and this is still on the same line.

This is on a new paragraph because there is two new lines.
```

Hello, this is the first paragraph.
This is still the first paragraph and this is still on the same line.

This is on a new paragraph because there is two new lines.
