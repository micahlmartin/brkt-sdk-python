# brkt-sdk-python

A python SDK for building against the Bracket Computing RESTful API.

## BRKT Requests

A library packaged as part of the SDK which handles low level HTTP requests
against the Bracket API.  The library is really just an authentication plugin to
[python requests](https://github.com/kennethreitz/requests).  Therefore
usage is similar:

    In [1]: import json
    In [2]: import brkt_requests
    In [3]: session = brkt_requests.APISession(
        access_token='********',
        mac_key='********')
    In [4]: resp = session.get(<API-url>)
    In [5]: resp.status_code
    Out[5]: 200
    In [6]: resp.json
    Out[6]:
        <json response>

### Command line tools

Additionally a small command line utility is included `brkt_api_client` which
can be used to conveniently interact with the Bracket API from the command
line:

    brkt_api_client GET <API-path>

Use the --help flag for usage
