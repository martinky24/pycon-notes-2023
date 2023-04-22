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
- [Here](https://snarky.ca/tag/syntactic-sugar/)` is Brett's website with this talk as blog posts

Cool talk. Pretty theoretical, but very consumable by anyone whose familiar with Python. Interesting, worth watching for a "fun talk".

## Plug life into your codebase: Making an established Python codebase pluggable ([link](https://us.pycon.org/2023/schedule/presentation/66/))

Didn't attend but heard is was good. Potentially worth looking up video.

## How Pydantic V2 leverages Rust's Superpowers ([link](https://us.pycon.org/2023/schedule/presentation/39/))

- Talked about the life cycle of pydantic to date. Origin story, and how/where we got to its usage today.
- Priorities for v2. It will include breaking changes, intending to "fix" some misdeeds of the original implementation.
  - This it the authors intended "only opportunity" to make breaking changes
- Wrote v2 in Rust. Gave info on reasoning why Rust.
- "Python is the most concise, elegant way of defining logic right now" (presenters opinion)
- Addition of pydantic "stict mode", which doesn't attempt to coerce inputs and instead fails if the type is incorrect

Good talk! Super interesting. If someone's a heavy pydantic user, it's good big picture info on the library.

## Subclassing, Composition, Python, and You ([link](https://us.pycon.org/2023/schedule/presentation/7/))

Didn't go to this talk, but I really wanted to. Need to watch the recording.

## How memory profilers work ([link](https://us.pycon.org/2023/schedule/presentation/91/))

- Memory is complicated
- Memory profilers are complicated
- Memory profiles are a useful piece of the toolkit

Great talk on how memory allocation and such works. Worth watching the topic is at all interesting to you.

## How we are making CPython faster. Past, present and future. ([link](https://us.pycon.org/2023/schedule/presentation/73/))

- A lot of work to make the default `object()` take up fewer bytes. It's been reduced by 75% (incrementally) from 2.7 to 3.11!

Cool talk, very interesting "under the hood stuff". Doesn't affect day to days but satiates curiosity.

## How To Keep A Secret ([link](https://us.pycon.org/2023/schedule/presentation/149/))

- Secret management in Python
- Use a password manager!
- CIA Triad: Confidentiality, integrity, availability
- USE THE LOCAL KEYRING MODULE ([link](https://pypi.org/project/keyring/))
- Encrypt disk

Cool talk. Glyph is a legend. Worth watching!

## Vectorize all the things! Using linear algebra and NumPy to make your Python code lightning fast. ([link](https://us.pycon.org/2023/schedule/presentation/140/))

Really good talk for motivating cases for vectorization in scientific code! Probably worth watching for anyone close to applications here
