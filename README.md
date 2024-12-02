20241203 0811 Try using uv to pass Python dependencies in a virtual environment

```bash
(base) johng@ReachLP031:~/daily/20241203$ cd uv_test_20241203/
(base) johng@ReachLP031:~/daily/20241203/uv_test_20241203$ uv init
Initialized project `uv-test-20241203`
(base) johng@ReachLP031:~/daily/20241203/uv_test_20241203$ tree
.
├── LICENSE
├── README.md
├── hello.py
└── pyproject.toml

1 directory, 4 files
(base) johng@ReachLP031:~/daily/20241203/uv_test_20241203$ uv python list
cpython-3.13.0+freethreaded-linux-x86_64-gnu    <download available>
cpython-3.12.7-linux-x86_64-gnu                 <download available>
cpython-3.12.4-linux-x86_64-gnu                 /home/johng/anaconda3/bin/python3.12
cpython-3.12.4-linux-x86_64-gnu                 /home/johng/anaconda3/bin/python3 -> python3.12
cpython-3.12.4-linux-x86_64-gnu                 /home/johng/anaconda3/bin/python -> python3.12
cpython-3.12.3-linux-x86_64-gnu                 /usr/bin/python3.12
cpython-3.12.3-linux-x86_64-gnu                 /usr/bin/python3 -> python3.12
cpython-3.12.3-linux-x86_64-gnu                 /bin/python3.12
cpython-3.12.3-linux-x86_64-gnu                 /bin/python3 -> python3.12
cpython-3.11.10-linux-x86_64-gnu                <download available>
cpython-3.10.15-linux-x86_64-gnu                <download available>
cpython-3.9.20-linux-x86_64-gnu                 <download available>
cpython-3.8.20-linux-x86_64-gnu                 <download available>
cpython-3.7.9-linux-x86_64-gnu                  <download available>
pypy-3.10.14-linux-x86_64-gnu                   <download available>
pypy-3.9.19-linux-x86_64-gnu                    <download available>
pypy-3.8.16-linux-x86_64-gnu                    <download available>
pypy-3.7.13-linux-x86_64-gnu                    <download available>
(base) johng@ReachLP031:~/daily/20241203/uv_test_20241203$ uv python install
Installed Python 3.12.7 in 2.96s
 + cpython-3.12.7-linux-x86_64-gnu
(base) johng@ReachLP031:~/daily/20241203/uv_test_20241203$ uv python list
cpython-3.13.0+freethreaded-linux-x86_64-gnu    <download available>
cpython-3.12.7-linux-x86_64-gnu                 /home/johng/.local/share/uv/python/cpython-3.12.7-linux-x86_64-gnu/bin/python3.12
cpython-3.12.4-linux-x86_64-gnu                 /home/johng/anaconda3/bin/python3.12
cpython-3.12.4-linux-x86_64-gnu                 /home/johng/anaconda3/bin/python3 -> python3.12
cpython-3.12.4-linux-x86_64-gnu                 /home/johng/anaconda3/bin/python -> python3.12
cpython-3.12.3-linux-x86_64-gnu                 /usr/bin/python3.12
cpython-3.12.3-linux-x86_64-gnu                 /usr/bin/python3 -> python3.12
cpython-3.12.3-linux-x86_64-gnu                 /bin/python3.12
cpython-3.12.3-linux-x86_64-gnu                 /bin/python3 -> python3.12
cpython-3.11.10-linux-x86_64-gnu                <download available>
cpython-3.10.15-linux-x86_64-gnu                <download available>
cpython-3.9.20-linux-x86_64-gnu                 <download available>
cpython-3.8.20-linux-x86_64-gnu                 <download available>
cpython-3.7.9-linux-x86_64-gnu                  <download available>
pypy-3.10.14-linux-x86_64-gnu                   <download available>
pypy-3.9.19-linux-x86_64-gnu                    <download available>
pypy-3.8.16-linux-x86_64-gnu                    <download available>
pypy-3.7.13-linux-x86_64-gnu                    <download available>
(base) johng@ReachLP031:~/daily/20241203/uv_test_20241203$ uv run hello.py
Using CPython 3.12.7
Creating virtual environment at: .venv
Hello from uv-test-20241203!
(base) johng@ReachLP031:~/daily/20241203/uv_test_20241203$ tree -a
.
├── .git
│   ├── HEAD
│   ├── config
│   ├── description
│   ├── hooks
│   │   ├── applypatch-msg.sample
│   │   ├── commit-msg.sample
│   │   ├── fsmonitor-watchman.sample
│   │   ├── post-update.sample
│   │   ├── pre-applypatch.sample
│   │   ├── pre-commit.sample
│   │   ├── pre-merge-commit.sample
│   │   ├── pre-push.sample
│   │   ├── pre-rebase.sample
│   │   ├── pre-receive.sample
│   │   ├── prepare-commit-msg.sample
│   │   ├── push-to-checkout.sample
│   │   ├── sendemail-validate.sample
│   │   └── update.sample
│   ├── index
│   ├── info
│   │   └── exclude
│   ├── logs
│   │   ├── HEAD
│   │   └── refs
│   │       ├── heads
│   │       │   └── main
│   │       └── remotes
│   │           └── origin
│   │               └── HEAD
│   ├── objects
│   │   ├── info
│   │   └── pack
│   │       ├── pack-4f6291f03e71b5d2a18990351aaaf56addc4ad8c.idx
│   │       ├── pack-4f6291f03e71b5d2a18990351aaaf56addc4ad8c.pack
│   │       └── pack-4f6291f03e71b5d2a18990351aaaf56addc4ad8c.rev
│   ├── packed-refs
│   └── refs
│       ├── heads
│       │   └── main
│       ├── remotes
│       │   └── origin
│       │       └── HEAD
│       └── tags
├── .gitignore
├── .python-version
├── .venv
│   ├── .gitignore
│   ├── CACHEDIR.TAG
│   ├── bin
│   │   ├── activate
│   │   ├── activate.bat
│   │   ├── activate.csh
│   │   ├── activate.fish
│   │   ├── activate.nu
│   │   ├── activate.ps1
│   │   ├── activate_this.py
│   │   ├── deactivate.bat
│   │   ├── pydoc.bat
│   │   ├── python -> /home/johng/.local/share/uv/python/cpython-3.12.7-linux-x86_64-gnu/bin/python3.12
│   │   ├── python3 -> python
│   │   └── python3.12 -> python
│   ├── lib
│   │   └── python3.12
│   │       └── site-packages
│   │           ├── __pycache__
│   │           │   └── _virtualenv.cpython-312.pyc
│   │           ├── _virtualenv.pth
│   │           └── _virtualenv.py
│   ├── lib64 -> lib
│   └── pyvenv.cfg
├── LICENSE
├── README.md
├── hello.py
├── pyproject.toml
└── uv.lock

24 directories, 53 files
(base) johng@ReachLP031:~/daily/20241203/uv_test_20241203$ uv add streamlit pandas numpy
Resolved 43 packages in 481ms
Prepared 32 packages in 3.06s
Installed 41 packages in 42ms
...
(base) johng@ReachLP031:~/daily/20241203/uv_test_20241203$ source .venv/bin/activate
(uv-test-20241203) (base) johng@ReachLP031:~/daily/20241203/uv_test_20241203$ python --version
Python 3.12.7
(uv-test-20241203) (base) johng@ReachLP031:~/daily/20241203/uv_test_20241203$ uv pip list
Package                   Version
------------------------- -----------
altair                    5.5.0
attrs                     24.2.0
blinker                   1.9.0
cachetools                5.5.0
certifi                   2024.8.30
charset-normalizer        3.4.0
click                     8.1.7
gitdb                     4.0.11
gitpython                 3.1.43
idna                      3.10
jinja2                    3.1.4
jsonschema                4.23.0
jsonschema-specifications 2024.10.1
markdown-it-py            3.0.0
markupsafe                3.0.2
mdurl                     0.1.2
narwhals                  1.15.1
numpy                     2.1.3
packaging                 24.2
pandas                    2.2.3
pillow                    11.0.0
protobuf                  5.29.0
pyarrow                   18.1.0
pydeck                    0.9.1
pygments                  2.18.0
python-dateutil           2.9.0.post0
pytz                      2024.2
referencing               0.35.1
requests                  2.32.3
rich                      13.9.4
rpds-py                   0.22.0
six                       1.16.0
smmap                     5.0.1
streamlit                 1.40.2
tenacity                  9.0.0
toml                      0.10.2
tornado                   6.4.2
typing-extensions         4.12.2
tzdata                    2024.2
urllib3                   2.2.3
watchdog                  6.0.0  
(uv-test-20241203) (base) johng@ReachLP031:~/daily/20241203/uv_test_20241203$ streamlit run '20241203 0826 streamlit_hello.py'

  You can now view your Streamlit app in your browser.

  Local URL: http://localhost:8501
  Network URL: http://172.20.204.78:8501
```

The browser now displays "Hello".
