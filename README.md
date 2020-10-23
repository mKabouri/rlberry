![rlberry](logo/berries.png)
![rlberry](logo/rlberry_logo.png)

# A Reinforcement Learning Library for Research and Education 

![pytest](https://github.com/rlberry-py/rlberry/workflows/test/badge.svg)

# Philosophy

* For each algorithm, write documentation/tutorial/examples.
* Provide a very general interface for agents, that
    * puts **minimal constraints** on the agent code (=> making it easy to include new algorithms and modify existing ones)
    * allows comparison between agents using a simple and unified evaluation interface (=> making it easy, for instance, to compare deep and "traditional" RL algorithms).
* Unified seeding mechanism: define only one global seed, from which all other seeds will inherit, enforcing independence of the random number generators (=> avoid seed "optimization"!)
* Simple interface for creating and **rendering** new environments. 


# Install

Creating a virtual environment and installing:

```
conda create -n rlberry python=3.7
conda activate rlberry
pip install -e .
```

# Tests

To run tests, run `pytest`.

With coverage: install and run pytest-cov
```
pip install pytest-cov
bash run_tests.sh
```

See coverage report in `cov_html/index.html`.


# Notes

* To save videos, installing [ffmpeg-python](https://github.com/kkroening/ffmpeg-python) is required:
```
pip install ffmpeg-python
```

* Convention for verbose:
    * `verbose<0`: nothing is printed
    * `verbose=0`: print only erros and importatnt warnings
    * `verbose>1`: print progress messages
