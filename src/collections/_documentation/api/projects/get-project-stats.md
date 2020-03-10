---
# This file is automatically generated from the API using `sentry/api-docs/generator.py.`
# Do not manually edit this file.
{
  "api_path": "/api/0/projects/{organization_slug}/{project_slug}/stats/", 
  "authentication": "required", 
  "description": "Return a set of points representing a normalized timestamp and the\nnumber of events seen in the period.\n\nQuery ranges are limited to Sentry's configured time-series\nresolutions.", 
  "example_request": "GET /api/0/projects/the-interstellar-jurisdiction/pump-station/stats/ HTTP/1.1\nHost: sentry.io\nAuthorization: Bearer <token>", 
  "example_response": "HTTP/1.1 200 OK\nContent-Length: 471\nX-XSS-Protection: 1; mode=block\nX-Content-Type-Options: nosniff\nContent-Language: en\nAccess-Control-Expose-Headers: X-Sentry-Error, Retry-After\nVary: Accept-Language, Cookie\nAccess-Control-Allow-Methods: GET, HEAD, OPTIONS\nAllow: GET, HEAD, OPTIONS\nAccess-Control-Allow-Origin: *\nAccess-Control-Allow-Headers: X-Sentry-Auth, X-Requested-With, Origin, Accept, Content-Type, Authentication, Authorization\nContent-Type: application/json\nX-Frame-Options: deny\n\n[\n  [\n    1583773200.0, \n    906\n  ], \n  [\n    1583776800.0, \n    846\n  ], \n  [\n    1583780400.0, \n    1240\n  ], \n  [\n    1583784000.0, \n    1200\n  ], \n  [\n    1583787600.0, \n    843\n  ], \n  [\n    1583791200.0, \n    953\n  ], \n  [\n    1583794800.0, \n    1117\n  ], \n  [\n    1583798400.0, \n    1716\n  ], \n  [\n    1583802000.0, \n    1924\n  ], \n  [\n    1583805600.0, \n    1912\n  ], \n  [\n    1583809200.0, \n    1012\n  ], \n  [\n    1583812800.0, \n    1449\n  ], \n  [\n    1583816400.0, \n    419\n  ], \n  [\n    1583820000.0, \n    637\n  ], \n  [\n    1583823600.0, \n    1678\n  ], \n  [\n    1583827200.0, \n    1286\n  ], \n  [\n    1583830800.0, \n    895\n  ], \n  [\n    1583834400.0, \n    1654\n  ], \n  [\n    1583838000.0, \n    1695\n  ], \n  [\n    1583841600.0, \n    936\n  ], \n  [\n    1583845200.0, \n    755\n  ], \n  [\n    1583848800.0, \n    708\n  ], \n  [\n    1583852400.0, \n    1562\n  ], \n  [\n    1583856000.0, \n    2293\n  ]\n]", 
  "method": "GET", 
  "parameters": null, 
  "path_parameters": [
    {
      "description": "the slug of the organization.", 
      "name": "organization_slug", 
      "type": "string"
    }, 
    {
      "description": "the slug of the project.", 
      "name": "project_slug", 
      "type": "string"
    }
  ], 
  "query_parameters": [
    {
      "description": "the name of the stat to query (`\"received\"`, `\"rejected\"`, `\"blacklisted\"`, `generated`)", 
      "name": "stat", 
      "type": "string"
    }, 
    {
      "description": "a timestamp to set the start of the query in seconds since UNIX epoch.", 
      "name": "since", 
      "type": "timestamp"
    }, 
    {
      "description": "a timestamp to set the end of the query in seconds since UNIX epoch.", 
      "name": "until", 
      "type": "timestamp"
    }, 
    {
      "description": "an explicit resolution to search for (one of `10s`, `1h`, and `1d`)", 
      "name": "resolution", 
      "type": "string"
    }
  ], 
  "sidebar_order": 18, 
  "title": "Retrieve Event Counts for a Project", 
  "warning": "This endpoint may change in the future without notice."
}
---