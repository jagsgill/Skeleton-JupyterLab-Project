# Intended Use
Use for local, non-secured Jupyter Lab work.

# Why use this? 
This container-based project avoids the cumbersome setup of python, virtual environment, dependencies. 
It has a clean project structure, and is easily version-controlled.

# Usage
Run with `docker-compose up`. Open your browser to [https://localhost:8888](https://localhost:8888).

# Configuration 
Just modify the default [docker-compose.yml](docker-compose.yml) file or create a new compose file if required.

The default compose file:
  - uses the `jupyter/minimal-notebook` image.
  - uses port `8888` by default.
  - disables the default token-based authentication for convenience of local non-production use. 
  - mounts the working directory, [notebooks](notebooks), into the container in `rw` (read-write) mode.
    - File updates are live between the container and host filesystems. Filesystem changes persist 
      on the host filesystem after the container is stopped.
