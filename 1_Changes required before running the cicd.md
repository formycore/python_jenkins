# Changes required before running the cicd
```
- in src/requiremnets.txt
Flask>=2.2.2
--------------------
- in the makefile
  - IMAGE_REG ?= docker.io
  - IMAGE_REPO ?= formycore/python-demoapp
-------------------------
- build/Dockerfile
  - LABEL org.opencontainers.image.source = "https://github.com/formycore/python_jenkins.git"
-----------------------------------------------------------
