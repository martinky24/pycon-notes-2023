# Saturday, April 22

## Keynote - James Powell

Awesome talk. Tries to really dig into understanding "what does being a python expert get you", and talks through some of the reasons it might not be worth everyone's time.

## Python Linters at Scale ([link](https://us.pycon.org/2023/schedule/presentation/101/))

- Speaker recommends:
  - Black
  - isort
  - flake8
  - mypy
- Recommends pinning linter versions and configs in repo's version control
- In CI, pre-install and cache dependencies in CI
- Try to keep versions and configs consistent across codebases (a lot of work, hard to pull off)
- Tips to help linters scale
  - Only run linters on updated code if possible, not ALL code
    - Very easy in local code, pre-commit does this by default
    - In CI you can use the Github Pulls API
  - Run linters in parallel
  - Reuse prior results if possible (caches)
- Suggests collecting observability info on linter runs
- Mentioned `fixit` ([link](https://github.com/Instagram/Fixit)) as a useful tool (author seems to be a contributor, I'm not sure it's actually super useful after glancing at the github page)

Presenter not great, but if someone is completley new to Python linting it could be worth watching.

## Python's syntactic sugar ([link](https://us.pycon.org/2023/schedule/presentation/41/))

- Brett Cannon, core deveoper and Python Steering Council member
- Basically defines any piece of non-super-essential syntax as sugar. Get's very conservative with "essential". Basically 10 things, `int`, `def`, assignments, `try`/`except`. Gets rid of stuff like `class`, `plus`, loops, attribute access, decorators, etc...
- [Here](https://snarky.ca/tag/syntactic-sugar/) is Brett's website with this talk as blog posts

Cool talk. Pretty theoretical, but very consumable by anyone whose familiar with Python. Interesting, worth watching for a "fun talk".

## How Pydantic V2 leverages Rust's Superpowers ([link](https://us.pycon.org/2023/schedule/presentation/39/))

## Subclassing, Composition, Python, and You ([link](https://us.pycon.org/2023/schedule/presentation/7/))

Didn't go to this talk, but I really wanted to. Need to watch the recording.

## How memory profilers work ([link](https://us.pycon.org/2023/schedule/presentation/91/))
