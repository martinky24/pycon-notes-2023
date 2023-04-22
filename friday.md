# Friday, Apr 21

## An Overview of the Python code Tool Lanscape 2023 ([link](https://us.pycon.org/2023/schedule/presentation/110/))

- Canceled `:(`

## Dev containers

- Microsoft advocate talking about [dev containers](https://code.visualstudio.com/docs/devcontainers/containers)
- Mostly a marketing ad for Microsoft tech
- I am sad original talk got canceled

Not worth anyone's time

## Making CPython 3.11 Especially Fast ([link](https://us.pycon.org/2023/schedule/presentation/6/))

- "Just upgrade to 3.11 and you'll probably see a performance improvement"
- Cool talk on the "how" of making python 3.11 faster
- It's all under the hood -- no changes by the user required, outside of writing good python from the start
- Presenter created package to show people where their python code was being optimized, see [Specialist](https://pypi.org/project/specialist/)
- More info on this in [PEP659](https://peps.python.org/pep-0659/)

Cool talk. Worth watching if you're into Python internals.

## Introducing incompatible changes in Python, Victor Stinner ([link](https://us.pycon.org/2023/schedule/presentation/4/))

- Talked about some incompatible changs from python 2 -> python 3, what motivated some of them, and how they caused problems
- Talked about some of the reasons the python 2 -> python 3 upgrade cycle took ~10 years for the masses
- The "Faster CPython" effort around 3.11 relied on changing some deep internals that some people integrating with the C api could have relied on.

Probably not worth watching. The content is interesting, but not required for anyone's day-to-day, and the presenter isn't great at public speaking.

## Reproducible molecular simulations with Python ([link](https://us.pycon.org/2023/schedule/presentation/118/))

- I had hoped there would be more on the "reproducible simulation" part, but the talk was more a very, very high level overview of how molecular dynamic simulations work

Not super helpful or interesting unless you're interested in molecular dynamics.

## A Per-Interpreter GIL: Concurrency and Parallelism with Subinterpreters ([link](https://us.pycon.org/2023/schedule/presentation/54/))

- Python 3.12 will have a per-interpreter GIL. What does this mean?
  - Won't be able to use this til 3.12
  - Standard library access to this won't be introduced until 3.13, see [PEP554](https://peps.python.org/pep-0554/#alternative-solutions)
  - Eric Snow will likely introduce access to this on PyPi ahead of time
- Better take advantage of multi-core systems with Python

Cool stuff. Eric Snow (presenter) is really passionate about the work. Not immediately relevant for our day-to-day.

## Testing Spacecraft with Pytest ([link](https://us.pycon.org/2023/schedule/presentation/40/))

- Presenters company is launching a spacecraft... they need to do a lot of testing of this spacecraft
- Presenter found tooling for testing is oftentimes build around testing web services... which doesn't always make sense for testing spacecraft. Different patterns and different assumptions.
- Software defects can behave differently than hardware defects!
- Operating environment matters. You have to test your software in the environment it will be running in production
  - TEST IN ATLAS?
- You can't just test to an interface. Components need to be tested against components.
  - Need to test end to end to the extent possible
  - If end-to-end isn't possible, overlapping interface tests are a must.
- Parameterized fixtures!

Cool talk! Especially if someone is interested in... writing software for space cases. Exceptional walk through of the power of pytest and how the framework can be used to test things such as HITL.
