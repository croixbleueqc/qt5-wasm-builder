qt5-wasm-builder (docker)
=========================

Docker image to compile a Qt 5 application in WebAssembly

Build
-----

Precompiled qt5-wasm package
^^^^^^^^^^^^^^^^^^^^^^^^^^^^

.. code:: bash

    # Instruction for archlinux OS
    # Build qt5-wasm from AUR (https://aur.archlinux.org/packages/qt5-wasm/)
    git clone https://aur.archlinux.org/qt5-wasm.git
    cd qt5-wasm
    makepkg -s
    python -m http.server

    docker build --build-arg=SERVER=<IP>:8000 -t qt5-wasm-builder:latest -t qt5-wasm-builder:5.15.0 -f Dockerfile.precompiled .

From scratch
^^^^^^^^^^^^

TODO
