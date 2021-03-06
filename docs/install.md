## Installing Cirq

Choose your operating system:

- [Installing on Linux](#installing-on-linux)
- [Installing on Mac OS X](#installing-on-mac-os-x)
- [Installing on Windows](#installing-on-windows)
- [Installing on Docker](#installing-on-docker)

If you want to create a development environment, see [development.md](development.md).

---

### Alpha Disclaimer

**Cirq is currently in alpha.**
We are still making breaking changes.
We *will* break your code when we make new releases.
We recommend that you target a specific version of Cirq, and periodically bump to the latest release.
That way you have control over when a breaking change affects you.

### Installing on Linux

0. Make sure you have python 3.5.2 or greater.

    See [Installing Python 3 on Linux](https://docs.python-guide.org/starting/install3/linux/) @ the hitchhiker's guide to python.

1. Consider using a [virtual environment](https://packaging.python.org/guides/installing-using-pip-and-virtualenv/).

2. Use `pip` to install `cirq`:

    ```bash
    python -m pip install --upgrade pip
    python -m pip install cirq
    ```

3. (Optional) install system dependencies that pip can't handle.

    ```bash
    sudo apt-get install python3-tk texlive-latex-base latexmk
    ```

    - Without `python3-tk`, plotting functionality won't work.
    - Without `texlive-latex-base` and `latexmk`, pdf writing functionality will not work.

4. Check that it works!

    ```bash
    python -c 'import cirq; print(cirq.google.Foxtail)'
    # should print:
    # (0, 0)───(0, 1)───(0, 2)───(0, 3)───(0, 4)───(0, 5)───(0, 6)───(0, 7)───(0, 8)───(0, 9)───(0, 10)
    # │        │        │        │        │        │        │        │        │        │        │
    # │        │        │        │        │        │        │        │        │        │        │
    # (1, 0)───(1, 1)───(1, 2)───(1, 3)───(1, 4)───(1, 5)───(1, 6)───(1, 7)───(1, 8)───(1, 9)───(1, 10)
    ```


### Installing on Mac OS X

0. Make sure you have python 3.5 or greater.

    See [Installing Python 3 on Mac OS X](https://docs.python-guide.org/starting/install3/osx/) @ the hitchhiker's guide to python.

1. Consider using a [virtual environment](https://packaging.python.org/guides/installing-using-pip-and-virtualenv/).

2. Use `pip` to install `cirq`:

    ```bash
    python -m pip install --upgrade pip
    python -m pip install cirq
    ```

3. Check that it works!

    ```bash
    python -c 'import cirq; print(cirq.google.Foxtail)'
    # should print:
    # (0, 0)───(0, 1)───(0, 2)───(0, 3)───(0, 4)───(0, 5)───(0, 6)───(0, 7)───(0, 8)───(0, 9)───(0, 10)
    # │        │        │        │        │        │        │        │        │        │        │
    # │        │        │        │        │        │        │        │        │        │        │
    # (1, 0)───(1, 1)───(1, 2)───(1, 3)───(1, 4)───(1, 5)───(1, 6)───(1, 7)───(1, 8)───(1, 9)───(1, 10)
    ```


### Installing on Windows

0. If you are using the [Windows Subsystem for Linux](https://docs.microsoft.com/en-us/windows/wsl/about), use the [Linux install instructions](#installing-on-linux) instead of these instructions.

1. Make sure you have python 3.5 or greater.

    See [Installing Python 3 on Windows](https://docs.python-guide.org/starting/install3/win/) @ the hitchhiker's guide to python.

2. Use `pip` to install `cirq`:

    ```bash
    python -m pip install --upgrade pip
    python -m pip install cirq
    ```

3. Check that it works!

    ```bash
    python -c "import cirq; print(cirq.google.Foxtail)"
    # should print:
    # (0, 0)───(0, 1)───(0, 2)───(0, 3)───(0, 4)───(0, 5)───(0, 6)───(0, 7)───(0, 8)───(0, 9)───(0, 10)
    # │        │        │        │        │        │        │        │        │        │        │
    # │        │        │        │        │        │        │        │        │        │        │
    # (1, 0)───(1, 1)───(1, 2)───(1, 3)───(1, 4)───(1, 5)───(1, 6)───(1, 7)───(1, 8)───(1, 9)───(1, 10)
    ```


### Installing on Docker

This will use a Docker image that will isolate Cirq's installation from the rest of the system.

0. [Install Docker](https://docs.docker.com/install/#supported-platforms) on your host sytem.

1. Pull the docker image:
    ```bash
    docker pull quantumlib/cirq
     ```

2. Check that it works!

    ```bash
    docker run -it quantumlib/cirq python -c "import cirq; print(cirq.google.Foxtail)"
    # should print:
    # (0, 0)───(0, 1)───(0, 2)───(0, 3)───(0, 4)───(0, 5)───(0, 6)───(0, 7)───(0, 8)───(0, 9)───(0, 10)
    # │        │        │        │        │        │        │        │        │        │        │
    # │        │        │        │        │        │        │        │        │        │        │
    # (1, 0)───(1, 1)───(1, 2)───(1, 3)───(1, 4)───(1, 5)───(1, 6)───(1, 7)───(1, 8)───(1, 9)───(1, 10)
    ```

3. To run the image:
    ```bash
    docker run -it quantumlib/cirq
     ```

