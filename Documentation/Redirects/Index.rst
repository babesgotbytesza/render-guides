..  include:: /Includes.rst.txt

..  _redirects:

=========
Redirects
=========

You can create redirects by calling:

..  code-block:: shell

    docker run --rm --pull always -v $(pwd):/project -it ghcr.io/typo3-documentation/render-guides:latest create-redirects-from-git -b 8faf68f9b0d2a6037c86300536eca52287150b43

Changes are saved to :file:`redirects.nginx.conf` and you need to make a manual PR at
https://github.com/TYPO3GmbH/site-intercept/blob/develop/config/nginx/redirects.conf

..  _redirects-options:

Options
=======

``-b``, ``--base-branch``
    The base branch to compare changes against. Default: ``main``.

``-d``, ``--docs-path``
    Path to the Documentation directory. Default: ``Documentation``.

``-o``, ``--output-file``
    Path to the nginx redirect configuration output file. Default:
    ``redirects.nginx.conf``.

``-r``, ``--versions``
    Regular expression of the versions to include. Default:
    ``(main|13.4|12.4)``.

``-p``, ``--path``
    Path of the manual, for example ``/m/typo3/reference-coreapi/``. Default:
    ``/``.
