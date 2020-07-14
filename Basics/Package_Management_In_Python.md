# Package Management in Python (PIP)
---
- Installation, Upgrade and Removal of packages can be done using a **program** called **pip**.  
- PIP will install packages from the Python Package Index, http://pypi.org
- Similar to linux repository( YUM, APT), NPM for Node.js, etc

## The Basics
---

### Check if PIP is installed 


```python
pip --version
```

    pip 20.1.1 from D:\Python\WPy64-3820\python-3.8.2.amd64\lib\site-packages\pip (python 3.8)Note: you may need to restart the kernel to use updated packages.
    
    
    

### Installation
---
In case for installation download the PIP from https://pypi.org/project/pip/  

### List Packages
- ```pip list``` will display all of the packages installed in the current environment



```python
pip list
```

    Package                       Version
    ----------------------------- ------------
    adodbapi                      2.6.1.3
    affine                        2.3.0
    aiofiles                      0.4.0
    aiosqlite                     0.11.0
    alabaster                     0.7.12
    altair                        4.0.1
    altair-data-server            0.4.1
    altair-transform              0.2.0
    altair-widgets                0.2.2
    altgraph                      0.17
    aniso8601                     8.0.0
    ansiwrap                      0.8.4
    appdirs                       1.4.3
    asciitree                     0.3.3
    asteval                       0.9.18
    astroid                       2.3.3
    astroML                       0.4.1
    astropy                       4.0
    async-generator               1.10
    atomicwrites                  1.3.0
    attrs                         19.3.0
    autopep8                      1.5
    Babel                         2.8.0
    backcall                      0.1.0
    backports-abc                 0.5
    baresql                       0.7.6
    bcolz                         1.2.1
    bcrypt                        3.1.7
    beautifulsoup4                4.8.2
    black                         19.10b0
    bleach                        3.1.3
    blinker                       1.4
    blosc                         1.8.3
    bloscpack                     0.16.0
    bokeh                         2.0.0
    Bottleneck                    1.3.2
    bqplot                        0.12.6
    branca                        0.3.1
    brewer2mpl                    1.4.1
    Brotli                        1.0.7
    certifi                       2019.11.28
    cffi                          1.14.0Note: you may need to restart the kernel to use updated packages.
    cftime                        1.1.1.1
    
    chardet                       3.0.4
    click                         7.1.1
    click-default-group           1.2.2
    click-plugins                 1.1.1
    cligj                         0.5.0
    cloudpickle                   1.3.0
    clrmagic                      0.0.1a2
    colorama                      0.4.3
    colorcet                      2.0.2
    comtypes                      1.1.7
    cryptography                  2.8
    cvxopt                        1.2.4
    cvxpy                         1.0.28
    cx-Freeze                     6.1
    cycler                        0.10.0
    Cython                        0.29.15
    cytoolz                       0.10.1
    dask                          2.12.0
    dask-searchcv                 0.2.0
    databases                     0.2.6
    datasette                     0.38
    datashader                    0.10.0
    datashape                     0.5.2
    db.py                         0.5.3
    decorator                     4.4.2
    defusedxml                    0.6.0
    Deprecated                    1.2.7
    descartes                     1.1.0
    diff-match-patch              20181111
    dill                          0.3.1.1
    distributed                   2.12.0
    docopt                        0.6.2
    docrepr                       0.1.1
    docutils                      0.16
    ecos                          2.0.7.post1
    emcee                         3.0.2
    entrypoints                   0.3
    et-xmlfile                    1.0.1
    fast-histogram                0.8
    fasteners                     0.15
    fastparquet                   0.3.3
    feather-format                0.4.0
    Fiona                         1.8.13
    Flask                         1.1.1
    flask-accepts                 0.16.2
    flask-restplus                0.13.0
    flask-restx                   0.1.0
    flaskerize                    0.14.0
    folium                        0.10.1
    formlayout                    2.0.0a0
    fs                            2.4.11
    fsspec                        0.6.2
    future                        0.18.2
    fuzzywuzzy                    0.18.0
    GDAL                          3.0.4
    geographiclib                 1.50
    geopandas                     0.7.0
    geopy                         1.21.0
    gmpy2                         2.0.8
    greenlet                      0.4.15
    guidata                       1.7.7.dev1
    h11                           0.9.0
    h2                            3.2.0
    h5py                          2.10.0
    HeapDict                      1.0.1
    helpdev                       0.6.10
    holoviews                     1.13.0b12
    hpack                         3.0.0
    html5lib                      1.0.1
    hupper                        1.10.2
    husl                          4.0.3
    hvplot                        0.5.2
    Hypercorn                     0.9.2
    hyperframe                    5.2.0
    hypothesis                    5.6.0
    ibis-framework                1.3.0
    idlex                         1.18
    idna                          2.9
    imageio                       2.8.0
    imageio-ffmpeg                0.4.1
    imagesize                     1.2.0
    imbalanced-learn              0.6.2
    importlib-metadata            1.5.0
    intake                        0.5.4
    intervaltree                  3.0.2
    ipykernel                     5.1.4
    ipyleaflet                    0.12.3
    ipympl                        0.5.3
    ipyparallel                   6.2.4
    ipython                       7.13.0
    ipython-genutils              0.2.0
    ipython-sql                   0.3.9
    ipywidgets                    7.5.1
    isort                         4.3.21
    itsdangerous                  1.1.0
    janus                         0.4.0
    jdcal                         1.4.1
    jedi                          0.15.2
    Jinja2                        2.11.1
    joblib                        0.14.1
    json5                         0.9.3
    jsonschema                    3.2.0
    julia                         0.5.1
    jupyter                       1.0.0
    jupyter-client                6.1.0
    jupyter-console               6.1.0
    jupyter-core                  4.6.3
    jupyter-server                0.1.1
    jupyter-sphinx                0.2.3
    jupyterlab                    2.0.1
    jupyterlab-launcher           0.13.1
    jupyterlab-pygments           0.1.0
    jupyterlab-server             1.0.7
    keyring                       21.2.0
    kiwisolver                    1.1.0
    lazy-object-proxy             1.4.3
    llvmlite                      0.31.0
    lmfit                         1.0.0
    locket                        0.2.0
    loky                          2.6.0
    lxml                          4.5.0
    Markdown                      3.2.1
    MarkupSafe                    1.1.1
    marshmallow                   3.5.1
    matplotlib                    3.2.1
    mccabe                        0.6.1
    mercantile                    1.1.2
    metakernel                    0.24.3
    mistune                       0.8.4
    mizani                        0.6.0
    mkl-service                   2.3.0
    mlxtend                       0.17.2
    monotonic                     1.5
    more-itertools                8.2.0
    moviepy                       1.0.1
    mpl-scatter-density           0.6
    mpld3                         0.3
    mpldatacursor                 0.7.1
    mpmath                        1.1.0
    msgpack                       1.0.0
    multipledispatch              0.6.0
    multiprocess                  0.70.9
    munch                         2.5.0
    mypy                          0.770
    mypy-extensions               0.4.3
    mysql-connector-python        8.0.18
    nbclient                      0.1.0
    nbconvert                     5.6.1
    nbconvert-reportlab           0.2
    nbformat                      5.0.4
    netCDF4                       1.5.3
    networkx                      2.4
    nltk                          3.4.5
    notebook                      6.0.3
    numba                         0.48.0
    numcodecs                     0.6.4
    numdifftools                  0.9.39
    numexpr                       2.7.1
    numpy                         1.18.2+mkl
    numpydoc                      0.9.2
    oct2py                        5.0.4
    octave-kernel                 0.31.0
    openpyxl                      3.0.3
    osqp                          0.6.1
    packaging                     20.3
    palettable                    3.3.0
    pandas                        1.0.3
    pandas-datareader             0.8.1
    pandocfilters                 1.4.2
    panel                         0.9.2
    papermill                     2.0.0
    param                         1.9.3
    parambokeh                    0.2.3
    paramiko                      2.7.1
    paramnb                       2.0.4
    parso                         0.6.2
    partd                         1.1.0
    passlib                       1.7.1
    pathspec                      0.7.0
    pathtools                     0.1.2
    patsy                         0.5.1
    pdfrw                         0.4
    pdvega                        0.2.1.dev0
    pefile                        2019.4.18
    pep8                          1.7.1
    pexpect                       4.8.0
    pg8000                        1.13.1
    pickleshare                   0.7.5
    Pillow                        7.0.0
    Pint                          0.11
    pip                           20.1.1
    pkginfo                       1.5.0.1
    plotly                        4.5.4
    plotnine                      0.6.0
    pluggy                        0.13.1
    ply                           3.11
    portalocker                   1.5.2
    portpicker                    1.3.1
    ppci                          0.5.7
    prettytable                   0.7.2
    priority                      1.3.0
    proglog                       0.1.9
    prometheus-client             0.7.1
    prompt-toolkit                3.0.4
    protobuf                      3.11.3
    psutil                        5.7.0
    ptpython                      3.0.1
    ptyprocess                    0.6.0
    PuLP                          1.6.11
    py                            1.8.1
    pyaml                         20.3.1
    pyarrow                       0.16.0
    PyAudio                       0.2.11
    pybars3                       0.9.7
    pybind11                      2.4.3
    pycodestyle                   2.5.0
    pycosat                       0.6.3
    pycparser                     2.20
    pyct                          0.4.6
    pydeck                        0.2.1
    pyepsg                        0.4.0
    pyflakes                      2.1.1
    pyflux                        0.4.17
    pygame                        1.9.6
    pygbm                         0.1.0
    Pygments                      2.6.1
    pyhdf                         0.10.2
    PyInstaller                   3.6
    pylint                        2.4.4
    pymc                          2.3.7
    PyMeta3                       0.5.1
    pymongo                       3.10.1
    PyNaCl                        1.3.0
    pyodbc                        4.0.30
    PyOpenGL                      3.1.5
    pypandoc                      1.3.2
    pyparsing                     2.4.6
    pyproj                        2.6.0
    PyQt5                         5.14.1
    PyQt5-sip                     12.7.1
    pyqtgraph                     0.11.0rc0
    PyQtWebEngine                 5.14.0
    pyrsistent                    0.15.7
    pyserial                      3.4
    pystache                      0.5.4
    pytest                        5.4.1
    python-dateutil               2.8.1
    python-hdf4                   0.10.0+dummy
    python-jsonrpc-server         0.3.4
    python-language-server        0.31.9
    python-Levenshtein            0.12.0
    python-snappy                 0.5.4
    pythonnet                     2.4.1.dev0
    PythonQwt                     0.5.6.dev0
    pytz                          2019.3
    pyviz-comms                   0.7.4
    PyWavelets                    1.1.1
    pywin32                       227
    pywin32-ctypes                0.2.0
    pywinpty                      0.5.7
    pywinusb                      0.4.2
    PyYAML                        5.3.1
    pyzmq                         19.0.0
    pyzo                          4.10.2
    QDarkStyle                    2.8
    QtAwesome                     0.7.0
    qtconsole                     4.7.1
    QtPy                          1.9.0
    quantecon                     0.4.6
    Quart                         0.11.3
    rasterio                      1.1.3
    readme-renderer               25.0
    redis                         3.4.1
    regex                         2020.2.20
    reportlab                     3.5.42
    requests                      2.23.0
    requests-toolbelt             0.9.1
    retrying                      1.3.3
    rise                          5.6.1
    Rtree                         0.9.4
    ruamel.yaml                   0.16.10
    ruamel.yaml.clib              0.2.0
    Rx                            3.1.0
    scikit-fuzzy                  0.4.1
    scikit-image                  0.16.2
    scikit-learn                  0.22.2.post1
    scikit-optimize               0.7.4
    scilab2py                     0.6.2
    scipy                         1.4.1
    scs                           2.1.1.post2
    seaborn                       0.10.0
    Send2Trash                    1.5.0
    setuptools                    46.0.0
    shap                          0.35.0
    Shapely                       1.7.0
    simplegeneric                 0.8.1
    simplejson                    3.17.0
    simpy                         3.0.12
    six                           1.14.0
    snakeviz                      2.0.1
    snowballstemmer               2.0.0
    snuggs                        1.4.7
    sortedcontainers              2.1.0
    sounddevice                   0.3.15
    soupsieve                     2.0
    Sphinx                        2.4.4
    sphinx-rtd-theme              0.4.3
    sphinxcontrib-applehelp       1.0.2
    sphinxcontrib-devhelp         1.0.2
    sphinxcontrib-htmlhelp        1.0.3
    sphinxcontrib-jsmath          1.0.1
    sphinxcontrib-qthelp          1.0.3
    sphinxcontrib-serializinghtml 1.1.4
    spyder                        4.1.1
    spyder-kernels                1.9.0
    SQLAlchemy                    1.3.15
    sqlite-bro                    0.9.1
    sqlparse                      0.3.1
    statsmodels                   0.11.1
    streamz                       0.5.0
    supersmoother                 0.4
    swifter                       0.297
    sympy                         1.5.1
    tables                        3.6.1
    tblib                         1.6.0
    tenacity                      6.1.0
    termcolor                     1.1.0
    terminado                     0.8.3
    testpath                      0.4.4
    textwrap3                     0.9.2
    thrift                        0.13.0
    toml                          0.10.0
    toolz                         0.10.0
    torch                         1.4.0+cpu
    torchvision                   0.5.0+cpu
    tornado                       6.0.4
    tqdm                          4.43.0
    traitlets                     4.3.3
    traittypes                    0.2.1
    tranquilizer                  0.4.1
    twine                         3.1.1
    twitter                       1.17.1
    typed-ast                     1.4.1
    typing-extensions             3.7.4.1
    tzlocal                       1.5.1
    uncertainties                 3.1.2
    urllib3                       1.25.8
    uvicorn                       0.11.3
    vega                          3.1.0
    vega-datasets                 0.8.0
    ViTables                      3.0.2
    voila                         0.1.21
    watchdog                      0.10.2
    wcwidth                       0.1.8
    webencodings                  0.5.1
    websockets                    8.1
    Werkzeug                      1.0.0
    wheel                         0.34.2
    widgetsnbextension            3.5.1
    winpython                     2.3.20200319
    wordcloud                     1.6.0
    wrapt                         1.11.2
    wsproto                       0.15.0
    xarray                        0.15.0
    xlrd                          1.2.0
    XlsxWriter                    1.2.8
    xlwings                       0.18.0
    zarr                          2.4.0
    zict                          2.0.0
    zipp                          3.1.0
    

### Search Packages
---
- Searching a package can be done either by browsing the url : https://pypi.org or by using the pip's limited search feature


```python
pip search requests
```

    requests-hawk (1.0.1)                - requests-hawk
    requests-auth (5.1.0)                - Authentication for Requests
    requests-dump (0.1.3)                - `requests-dump` provides hook functions for requests.
    requests-foauth (0.1.1)              - Requests TransportAdapter for foauth.org!
    pydantic-requests (0.1.3)            - A pydantic integration with requests.
    arcane-requests (0.1.1)              - Utility functions for requests
    Requests-OpenTracing (0.2.0)         - OpenTracing support for Requests
    yamlsettings-requests (1.0.0)        - YamlSettings Request Extension
    requests-aws4auth (1.0)              - AWS4 authentication for Requests
    requests-middleware (0.1.2)          - Composable HTTP middleware for requests
    jupyter-requests (0.0.3)             - Send requests to a Jupyter server.
    requests-custom (0.0.4)              - Python's requests with custom configuration
    requests-oauthlib (1.3.0)            - OAuthlib authentication support for Requests.
    requests-async (0.6.2)               - async-await support for `requests`.
    pycopy-requests (0.0.0)              - Dummy requests module for Pycopy
    requests-twisted (0.1.2)             - Twisted adapter for the requests library.
    requests-ftp (0.3.1)                 - FTP Transport Adapter for Requests.
    requests-file (1.5.1)                - File transport adapter for Requests
    pycurl-requests (0.1.1)              - A Requests-compatible interface for pycURL
    micropython-requests (0.0.0)         - Dummy requests module for MicroPython
    requests-cache (0.5.2)               - Persistent cache for requests library
    requestor-requests (0.1.0)           - Requestor Helper to request package
    patch-requests (0.2.0)               - Simple patching of `requests` calls
    requests-core (0.0.0)                - A minimal HTTP Client, for Requests.
    pyfortified-requests (0.3.6)         - Extension to Python `requests` functionality.
    requests-dump2 (0.2)                 - dump requests' requests http message content to stderr or your custom file
    selenium-requests (1.3)              - Extends Selenium WebDriver classes to include the request function from the Requests library, while doing all the needed cookie and request headers handling.
    requests-kerberos (0.12.0)           - A Kerberos authentication handler for python-requests
    requests-aeaweb (0.0.1)              - Requests wrapper to log onto AEAweb.org.
    requests-lb (0.3.2)                  - A load-balancing wrapper around requests
    requests-magpie (0.1.1)              - A Magpie authentication handler for python-requests
    requests-vzauth (0.1.0)              - Verizon Cloud authentication handler for requests.
    requests-f5auth (0.1.2)              - F5 REST Authentication support for Requests.
    requests-gssapi (1.2.1)              - A GSSAPI authentication handler for python-requests
    requests-credssp (1.1.1)             - HTTPS CredSSP authentication with the requests library.
    newio-requests (0.6.0)               - Newio + Requests: Async HTTP for Humans.
    monitor-requests (2.1.1)             - Check remote calls via request
    requests-crtauth (0.4)               - A crtauth authentication plugin for Python Requests.
    proxy-requests (0.5.1)               - Make HTTP requests with scraped proxies
    nidhoggr-requests (0.5.0)            - Requests-based repository implementation for nidhoggr
    splitio-requests (1.0.0)             - Split.io Admin API requests for humans
    requests-nber (0.0.1)                - Requests wrapper to log onto NBER.org.
    requests-staticmock (1.4.0)          - A static HTTP mock interface for requests
    requests-client (0.0.14)             - http://github.com/vgavro/requests-client
    stripe-requests (1.9.1-rc1)          - Stripe python bindings using requests
    requests-raw-logger (0.0.2)          - A request and response logger for requests
    requests-guard (0.1.0)               - requests-guard is a small library that allows you to impose size and time limits on your HTTP requests.
    fed-requests (0.0.30)                - A python package for managing requests to the FEDBIONET API
    aiohttp-requests (0.1.3)             - A thin wrapper for aiohttp client with Requests simplicity
    requests-negotiate (1.5)             - Negotiate authentication for the requests HTTP client library
    jsonrpc-requests (0.4.0)             - A JSON-RPC client library, backed by requests
    openpgp-requests (0.5)               - A wrapper to the requests module adding OpenPGP support.
    requests-ecp (0.2.1)                 - SAML/ECP authentication handler for python-requests
    requests-toolbelt (0.9.1)            - A utility belt for advanced users of python-requests
      INSTALLED: 0.9.1 (latest)
    requests-robotstxt (0.1.0)           - Brings automatic support for robots.txt files in requests.
    requests-oauth2 (0.3.0)              - OAuth2 support to Python-Requests HTTP library.
    retry-requests (1.0.1)               - Make requests's sessions auto-retry on failure.
    vk-requests (1.2.0)                  - vk.com requests for humans. API library for vk.com
    requests-chef (0.1.7)                - Chef Authentication protocol support for Python-Requests
    shopify-requests (0.4.0)             - Wrapper around the Shopify API using requests.
    requests-mock (1.8.0)                - Mock out responses from the requests package
    simple-requests (1.1.1)              - Asynchronous requests in Python without thinking about it.
    requests-httpsproxy (1.0.6)          - allow http/https requests through https proxy
    robotframework-requests (0.7.0)      - Robot Framework keyword library wrapper around requests
    requests-cpp (0.1.0)                 - Use c ++ multi-threaded http request library
    requests-gcp (0.2.0)                 - Python requests wrapper for service-to-service auth on GCP
    careful-requests (0.1.4)             - Requests for header-sensitive servers (like Accept-Encoding)
    requests-mauth (1.1.0)               - An MAuth client based around the excellent requests library.
    requests-aws (0.1.8)                 - AWS authentication for Amazon S3 for the python requests module
    requests-testing (0.2.0)             - A utility library for mocking out the `requests` Python library.
    requests-raven (0.0.1)               - Requests wrapper to log onto Raven (University of Cambridge).
    requests-runscope (0.1.6)            - This package adds Runscope support to the Python Requests library.
    requests-sigv4 (0.1.5)               - Library for making sigv4 requests to AWS API endpoints
    pylint-requests (0.1.1)              - A pylint plugin to check for common issues with usage of requests
    requests-oauth2client (0.4.0)        - An OAuth 2.0 client library for Python, with requests integration.
    requests-cloudkit (1.0.1)            - Apple CloudKit server-to-server support for the requests Python library.
    requests-unixsocket (0.2.0)          - Use requests to talk HTTP via a UNIX domain socket
    requests-asserts (0.1.2)             - The library to help test your HTTP requests using unittests
    crawl-requests (2.2.8)               - crawl_requests(like requests) can update ua and proxy automatically.
    requests-safe (0.2)                  - Provides an adapter for requests that won't allow connections to "unsafe" networks.
    flake8-requests (0.4.0)              - Checks for the requests module, by r2c. Available in Bento (https://bento.dev).
    requests-testadapter (0.3.0)         - Provides an adapter for mocking HTTP requests for unit test purposes.
    requests-threads (0.1.1)             - A Requests session that returns awaitable Twisted Deferreds instead of response objects.
    requests-bearer (0.5.1)              - An implementation of JSON Web Tokens using the Bearer authentication scheme for Requests.
    requests-fortified (0.3.1)           - Extension of Python HTTP `requests` with verbose logging using `logging-fortified`.
    requests-oauth (0.4.1)               - Hook for adding Open Authentication support to Python-requests HTTP library.
    requests-raw (0.2.1)                 - Use requests to talk HTTP via a Raw sockets (To Test RFC Compliance)
    requests-crawler (0.5.4)             - A web crawler based on requests-html, mainly targets for url validation test.
    requests-etag-cache (2020.7.1)       - requests etag cache
    opencensus-ext-requests (0.7.3)      - OpenCensus Requests Integration
    falcon-signed-requests (1.0.0)       - falcon-signed-requests
    opentelemetry-ext-requests (0.10b0)  - OpenTelemetry requests integration
    requests-auth-mashery (0.0.4)        - Mashery authentication for requests
    django-requests-logger (0.1.3)       - A django integration for requests.
    requests-aws4auth-redux (0.40)       - AWS4 authentication for Requests
    requests (2.24.0)                    - Python HTTP for Humans.
      INSTALLED: 2.23.0
      LATEST:    2.24.0
    play-requests (0.0.5)                - pytest-play plugin driving the famous Python requests library for making HTTP calls
    requests-jwt (0.5.3)                 - This package allows for HTTP JSON Web Token (JWT) authentication using the requests library.
    django-requests-tracker (2.10.4)     - Tracking http requests send by python-requests inside a Django application
    requests-aws-sign (0.1.6)            - This package provides AWS V4 request signing using the requests library.
    Note: you may need to restart the kernel to use updated packages.
    

### Install Packages
---
Install the latest version of a package by specifying a package's name:



```python
pip install requests
```

    Requirement already satisfied: requests in d:\python\wpy64-3820\python-3.8.2.amd64\lib\site-packages (2.23.0)Note: you may need to restart the kernel to use updated packages.
    
    Requirement already satisfied: certifi>=2017.4.17 in d:\python\wpy64-3820\python-3.8.2.amd64\lib\site-packages (from requests) (2019.11.28)
    Requirement already satisfied: idna<3,>=2.5 in d:\python\wpy64-3820\python-3.8.2.amd64\lib\site-packages (from requests) (2.9)
    Requirement already satisfied: chardet<4,>=3.0.2 in d:\python\wpy64-3820\python-3.8.2.amd64\lib\site-packages (from requests) (3.0.4)
    Requirement already satisfied: urllib3!=1.25.0,!=1.25.1,<1.26,>=1.21.1 in d:\python\wpy64-3820\python-3.8.2.amd64\lib\site-packages (from requests) (1.25.8)
    

or specify the version as below : 


```python
pip install requests==2.6.0
```

    Collecting requests==2.6.0Note: you may need to restart the kernel to use updated packages.
    

      WARNING: Retrying (Retry(total=4, connect=None, read=None, redirect=None, status=None)) after connection broken by 'ConnectTimeoutError(<pip._vendor.urllib3.connection.VerifiedHTTPSConnection object at 0x000002472452D7F0>, 'Connection to files.pythonhosted.org timed out. (connect timeout=15)')': /packages/73/63/b0729be549494a3e31316437053bc4e0a8bb71a07a6ee6059434b8f1cd5f/requests-2.6.0-py2.py3-none-any.whl
    ERROR: twine 3.1.1 has requirement requests>=2.20, but you'll have requests 2.6.0 which is incompatible.
    ERROR: moviepy 1.0.1 has requirement requests<3.0,>=2.8.1, but you'll have requests 2.6.0 which is incompatible.
    

    
      Downloading requests-2.6.0-py2.py3-none-any.whl (469 kB)
    Installing collected packages: requests
      Attempting uninstall: requests
        Found existing installation: requests 2.23.0
        Uninstalling requests-2.23.0:
          Successfully uninstalled requests-2.23.0
    Successfully installed requests-2.6.0
    

### Upgrade Packages
---
```pip install --upgrade``` can be used to upgrade the package


```python
pip install --upgrade  requests
```

    Collecting requestsNote: you may need to restart the kernel to use updated packages.
    
      Downloading requests-2.24.0-py2.py3-none-any.whl (61 kB)
    Requirement already satisfied, skipping upgrade: idna<3,>=2.5 in d:\python\wpy64-3820\python-3.8.2.amd64\lib\site-packages (from requests) (2.9)
    Requirement already satisfied, skipping upgrade: chardet<4,>=3.0.2 in d:\python\wpy64-3820\python-3.8.2.amd64\lib\site-packages (from requests) (3.0.4)
    Requirement already satisfied, skipping upgrade: certifi>=2017.4.17 in d:\python\wpy64-3820\python-3.8.2.amd64\lib\site-packages (from requests) (2019.11.28)
    Requirement already satisfied, skipping upgrade: urllib3!=1.25.0,!=1.25.1,<1.26,>=1.21.1 in d:\python\wpy64-3820\python-3.8.2.amd64\lib\site-packages (from requests) (1.25.8)
    Installing collected packages: requests
      Attempting uninstall: requests
        Found existing installation: requests 2.6.0
        Uninstalling requests-2.6.0:
          Successfully uninstalled requests-2.6.0
    Successfully installed requests-2.24.0
    

### Remove Package
---
- ```pip uninstall <package_name>``` can be used to uninstall the package

### Display Package Information
---
- ```pip show <package_name>``` displays the information about the mentioned package.



```python
pip show requests
```

    Name: requests
    Version: 2.24.0
    Summary: Python HTTP for Humans.
    Home-page: https://requests.readthedocs.io
    Note: you may need to restart the kernel to use updated packages.
    Author: Kenneth Reitz
    Author-email: me@kennethreitz.org
    License: Apache 2.0
    Location: d:\python\wpy64-3820\python-3.8.2.amd64\lib\site-packages
    Requires: chardet, certifi, urllib3, idna
    Required-by: twine, Sphinx, requests-toolbelt, quantecon, pyepsg, papermill, pandas-datareader, moviepy, intake, folium
    

### Freeze Packages
---
- ```pip freeze``` produces a list of installed packages, the output of the command uses the format that ```pip install``` expects.


```python
pip freeze
```

    adodbapi==2.6.1.3
    affine==2.3.0
    aiofiles==0.4.0
    aiosqlite==0.11.0
    alabaster==0.7.12
    altair==4.0.1
    altair-data-server==0.4.1
    altair-transform==0.2.0
    altair-widgets==0.2.2
    altgraph==0.17
    aniso8601==8.0.0
    ansiwrap==0.8.4
    appdirs==1.4.3
    asciitree==0.3.3
    asteval==0.9.18
    astroid==2.3.3
    astroML==0.4.1
    astropy==4.0
    async-generator==1.10
    atomicwrites==1.3.0
    attrs==19.3.0
    autopep8==1.5
    Babel==2.8.0
    backcall==0.1.0
    backports-abc==0.5
    baresql==0.7.6
    bcolz==1.2.1
    bcrypt==3.1.7
    beautifulsoup4==4.8.2
    black==19.10b0
    bleach==3.1.3
    blinker==1.4
    blosc==1.8.3
    bloscpack==0.16.0
    bokeh==2.0.0
    Bottleneck==1.3.2
    bqplot==0.12.6
    branca==0.3.1
    brewer2mpl==1.4.1
    Brotli==1.0.7
    certifi==2019.11.28
    cffi==1.14.0
    cftime==1.1.1.1
    chardet==3.0.4
    click==7.1.1
    click-default-group==1.2.2
    click-plugins==1.1.1
    cligj==0.5.0
    cloudpickle==1.3.0
    clrmagic==0.0.1a2
    colorama==0.4.3
    colorcet==2.0.2
    comtypes==1.1.7
    cryptography==2.8
    cvxopt==1.2.4
    cvxpy==1.0.28
    cx-Freeze==6.1
    cycler==0.10.0
    Cython==0.29.15
    cytoolz==0.10.1
    dask==2.12.0
    dask-searchcv==0.2.0
    databases==0.2.6
    datasette==0.38
    datashader==0.10.0
    datashape==0.5.2
    db.py==0.5.3
    decorator==4.4.2
    defusedxml==0.6.0
    Deprecated==1.2.7
    descartes==1.1.0
    diff-match-patch==20181111
    dill==0.3.1.1
    distributed==2.12.0
    docopt==0.6.2
    docrepr==0.1.1
    docutils==0.16
    ecos==2.0.7.post1
    emcee==3.0.2
    entrypoints==0.3
    et-xmlfile==1.0.1
    fast-histogram==0.8
    fasteners==0.15
    fastparquet==0.3.3
    feather-format==0.4.0
    Fiona==1.8.13
    Flask==1.1.1
    flask-accepts==0.16.2
    flask-restplus==0.13.0
    flask-restx==0.1.0
    flaskerize==0.14.0
    folium==0.10.1
    formlayout==2.0.0a0
    Note: you may need to restart the kernel to use updated packages.
    fs==2.4.11
    fsspec==0.6.2
    future==0.18.2
    fuzzywuzzy==0.18.0
    GDAL==3.0.4
    geographiclib==1.50
    geopandas==0.7.0
    geopy==1.21.0
    gmpy2==2.0.8
    greenlet==0.4.15
    guidata==1.7.7.dev1
    h11==0.9.0
    h2==3.2.0
    h5py==2.10.0
    HeapDict==1.0.1
    helpdev==0.6.10
    holoviews==1.13.0b12
    hpack==3.0.0
    html5lib==1.0.1
    hupper==1.10.2
    husl==4.0.3
    hvplot==0.5.2
    Hypercorn==0.9.2
    hyperframe==5.2.0
    hypothesis==5.6.0
    ibis-framework==1.3.0
    idlex==1.18
    idna==2.9
    imageio==2.8.0
    imageio-ffmpeg==0.4.1
    imagesize==1.2.0
    imbalanced-learn==0.6.2
    importlib-metadata==1.5.0
    intake==0.5.4
    intervaltree==3.0.2
    ipykernel==5.1.4
    ipyleaflet==0.12.3
    ipympl==0.5.3
    ipyparallel==6.2.4
    ipython==7.13.0
    ipython-genutils==0.2.0
    ipython-sql==0.3.9
    ipywidgets==7.5.1
    isort==4.3.21
    itsdangerous==1.1.0
    janus==0.4.0
    jdcal==1.4.1
    jedi==0.15.2
    Jinja2==2.11.1
    joblib==0.14.1
    json5==0.9.3
    jsonschema==3.2.0
    julia==0.5.1
    jupyter==1.0.0
    jupyter-client==6.1.0
    jupyter-console==6.1.0
    jupyter-core==4.6.3
    jupyter-server==0.1.1
    jupyter-sphinx==0.2.3
    jupyterlab==2.0.1
    jupyterlab-launcher==0.13.1
    jupyterlab-pygments==0.1.0
    jupyterlab-server==1.0.7
    keyring==21.2.0
    kiwisolver==1.1.0
    lazy-object-proxy==1.4.3
    llvmlite==0.31.0
    lmfit==1.0.0
    locket==0.2.0
    loky==2.6.0
    lxml==4.5.0
    Markdown==3.2.1
    MarkupSafe==1.1.1
    marshmallow==3.5.1
    matplotlib==3.2.1
    mccabe==0.6.1
    mercantile==1.1.2
    metakernel==0.24.3
    mistune==0.8.4
    mizani==0.6.0
    mkl-service==2.3.0
    mlxtend==0.17.2
    monotonic==1.5
    more-itertools==8.2.0
    moviepy==1.0.1
    mpl-scatter-density==0.6
    mpld3==0.3
    mpldatacursor==0.7.1
    mpmath==1.1.0
    msgpack==1.0.0
    multipledispatch==0.6.0
    multiprocess==0.70.9
    munch==2.5.0
    mypy==0.770
    mypy-extensions==0.4.3
    mysql-connector-python==8.0.18
    nbclient==0.1.0
    nbconvert==5.6.1
    nbconvert-reportlab==0.2
    nbformat==5.0.4
    netCDF4==1.5.3
    networkx==2.4
    nltk==3.4.5
    notebook==6.0.3
    numba==0.48.0
    numcodecs==0.6.4
    numdifftools==0.9.39
    numexpr==2.7.1
    numpy==1.18.2+mkl
    numpydoc==0.9.2
    oct2py==5.0.4
    octave-kernel==0.31.0
    openpyxl==3.0.3
    osqp==0.6.1
    packaging==20.3
    palettable==3.3.0
    pandas==1.0.3
    pandas-datareader==0.8.1
    pandocfilters==1.4.2
    panel==0.9.2
    papermill==2.0.0
    param==1.9.3
    parambokeh==0.2.3
    paramiko==2.7.1
    paramnb==2.0.4
    parso==0.6.2
    partd==1.1.0
    passlib==1.7.1
    pathspec==0.7.0
    pathtools==0.1.2
    patsy==0.5.1
    pdfrw==0.4
    pdvega==0.2.1.dev0
    pefile==2019.4.18
    pep8==1.7.1
    pexpect==4.8.0
    pg8000==1.13.1
    pickleshare==0.7.5
    Pillow==7.0.0
    Pint==0.11
    pkginfo==1.5.0.1
    plotly==4.5.4
    plotnine==0.6.0
    pluggy==0.13.1
    ply==3.11
    portalocker==1.5.2
    portpicker==1.3.1
    ppci==0.5.7
    prettytable==0.7.2
    priority==1.3.0
    proglog==0.1.9
    prometheus-client==0.7.1
    prompt-toolkit==3.0.4
    protobuf==3.11.3
    psutil==5.7.0
    ptpython==3.0.1
    ptyprocess==0.6.0
    PuLP==1.6.11
    py==1.8.1
    pyaml==20.3.1
    pyarrow==0.16.0
    PyAudio==0.2.11
    pybars3==0.9.7
    pybind11==2.4.3
    pycodestyle==2.5.0
    pycosat==0.6.3
    pycparser==2.20
    pyct==0.4.6
    pydeck==0.2.1
    pyepsg==0.4.0
    pyflakes==2.1.1
    pyflux==0.4.17
    pygame==1.9.6
    pygbm==0.1.0
    Pygments==2.6.1
    pyhdf==0.10.2
    PyInstaller==3.6
    pylint==2.4.4
    pymc==2.3.7
    PyMeta3==0.5.1
    pymongo==3.10.1
    PyNaCl==1.3.0
    pyodbc==4.0.30
    PyOpenGL==3.1.5
    pypandoc==1.3.2
    pyparsing==2.4.6
    pyproj==2.6.0
    PyQt5==5.14.1
    PyQt5-sip==12.7.1
    pyqtgraph==0.11.0rc0
    PyQtWebEngine==5.14.0
    pyrsistent==0.15.7
    pyserial==3.4
    pystache==0.5.4
    pytest==5.4.1
    python-dateutil==2.8.1
    python-hdf4==0.10.0+dummy
    python-jsonrpc-server==0.3.4
    python-language-server==0.31.9
    python-Levenshtein==0.12.0
    python-snappy==0.5.4
    pythonnet==2.4.1.dev0
    PythonQwt==0.5.6.dev0
    pytz==2019.3
    pyviz-comms==0.7.4
    PyWavelets==1.1.1
    pywin32==227
    pywin32-ctypes==0.2.0
    pywinpty==0.5.7
    pywinusb==0.4.2
    PyYAML==5.3.1
    pyzmq==19.0.0
    pyzo==4.10.2
    QDarkStyle==2.8
    QtAwesome==0.7.0
    qtconsole==4.7.1
    QtPy==1.9.0
    quantecon==0.4.6
    Quart==0.11.3
    rasterio==1.1.3
    readme-renderer==25.0
    redis==3.4.1
    regex==2020.2.20
    reportlab==3.5.42
    requests==2.24.0
    requests-toolbelt==0.9.1
    retrying==1.3.3
    rise==5.6.1
    Rtree==0.9.4
    ruamel.yaml==0.16.10
    ruamel.yaml.clib==0.2.0
    Rx==3.1.0
    scikit-fuzzy==0.4.1
    scikit-image==0.16.2
    scikit-learn==0.22.2.post1
    scikit-optimize==0.7.4
    scilab2py==0.6.2
    scipy==1.4.1
    scs==2.1.1.post2
    seaborn==0.10.0
    Send2Trash==1.5.0
    shap==0.35.0
    Shapely==1.7.0
    simplegeneric==0.8.1
    simplejson==3.17.0
    simpy==3.0.12
    six==1.14.0
    snakeviz==2.0.1
    snowballstemmer==2.0.0
    snuggs==1.4.7
    sortedcontainers==2.1.0
    sounddevice==0.3.15
    soupsieve==2.0
    Sphinx==2.4.4
    sphinx-rtd-theme==0.4.3
    sphinxcontrib-applehelp==1.0.2
    sphinxcontrib-devhelp==1.0.2
    sphinxcontrib-htmlhelp==1.0.3
    sphinxcontrib-jsmath==1.0.1
    sphinxcontrib-qthelp==1.0.3
    sphinxcontrib-serializinghtml==1.1.4
    spyder==4.1.1
    spyder-kernels==1.9.0
    SQLAlchemy==1.3.15
    sqlite-bro==0.9.1
    sqlparse==0.3.1
    statsmodels==0.11.1
    streamz==0.5.0
    supersmoother==0.4
    swifter==0.297
    sympy==1.5.1
    tables==3.6.1
    tblib==1.6.0
    tenacity==6.1.0
    termcolor==1.1.0
    terminado==0.8.3
    testpath==0.4.4
    textwrap3==0.9.2
    thrift==0.13.0
    toml==0.10.0
    toolz==0.10.0
    torch==1.4.0+cpu
    torchvision==0.5.0+cpu
    tornado==6.0.4
    tqdm==4.43.0
    traitlets==4.3.3
    traittypes==0.2.1
    tranquilizer==0.4.1
    twine==3.1.1
    twitter==1.17.1
    typed-ast==1.4.1
    typing-extensions==3.7.4.1
    tzlocal==1.5.1
    uncertainties==3.1.2
    urllib3==1.25.8
    uvicorn==0.11.3
    vega==3.1.0
    vega-datasets==0.8.0
    ViTables==3.0.2
    voila==0.1.21
    watchdog==0.10.2
    wcwidth==0.1.8
    webencodings==0.5.1
    websockets==8.1
    Werkzeug==1.0.0
    widgetsnbextension==3.5.1
    winpython==2.3.20200319
    wordcloud==1.6.0
    wrapt==1.11.2
    wsproto==0.15.0
    xarray==0.15.0
    xlrd==1.2.0
    XlsxWriter==1.2.8
    xlwings==0.18.0
    zarr==2.4.0
    zict==2.0.0
    zipp==3.1.0
    

Save the output in a file like below  
```pip freeze > requirements.txt```  
and the same packages can be installed in another environment like below  
```pip install -r requirements.txt```
