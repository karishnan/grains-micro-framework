## Micro-service based Framework Developed under PHP 7.3+

### list:

#### Features list 
#### when and why should select 
#### Basic API config 
#### Template Tree 
#### Full API config 
#### Sample API development 
#### Configuration Details 
#### Versioning and It's benefits explained 
#### Documents

<br /><br />


### Feature:

#### Cache Feature provides high Calibration and TP
#### Easily scale-able
#### Quick Go for PHP enterprise applications
#### Simple and light
#### Write and forget
#### Versioning - develop as you go
#### Multiple DB support
#### Readily available sub-modules as plugins

security - WIP
<br /><br />

### Basic API:
<pre>
{
    "Constants": {},
    "Codes": {},
    "Objects": {},
    "Workers": {
        "CalenderAPI": [
            {
                "seq": 0,
                "workerName": [
                    "printStartDate"
                ],
                "result": {
                    "success": 1,
                    "failure": -1
                }
            }
        ]
    },
    "APIs": {
        "CalenderAPI": {
            "inputs": {
                "post": [
                    "start_date",
                    "end_data"
                ]
            },
            "async": false,
            "events": false,
            "auth": {
                "jwt": false
            },
            "validate": {
                "rules": {
                    "start_date": "required|notEmpty"
                }
            },
            "objects": [
                "Callers"
            ],
            "external_apis": {
                "api_url": "inputs|values"
            },
            "configuration": [],
            "helpers": [],
            "injectors": [],
            "storage": [
                "s3",
                "local"
            ],
            "Workers": [
                "CalenderV1API"
            ],
            "output": ["json"]
        }
    }
}

</pre>
<br /><br />
### Template Tree:
<pre>
rock
├── App
│   ├── Auth
│   ├── Bootstrap
│   ├── Broadcasting
│   ├── Bus
│   ├── Cache
│   ├── Callers
│   ├── Config
│   ├── Console
│   ├── Container
│   ├── Context
│   ├── Contracts
│   ├── Cookie
│   ├── Core
│   │   ├── Callers
│   │   ├── Configuration
│   │   ├── ErrorHandler
│   │   ├── Request
│   │   ├── Log
│   │   ├── Response
│   │   ├── Url
│   │   └── Validator
│   ├── Database
│   ├── Dispatchers
│   ├── Encryption
│   ├── Events
│   ├── Exceptions
│   ├── Extensions
│   ├── Factory
│   ├── Filesystem
│   ├── Gates
│   ├── Generator
│   ├── Handler
│   ├── Hashing
│   ├── Job
│   ├── Lang
│   ├── Loader
│   ├── Log
│   ├── Mail
│   ├── Module
│   ├── Observer
│   ├── Pagination
│   ├── Pipeline
│   ├── Profile
│   ├── Provider
│   ├── Queue
│   ├── Redis
│   ├── Register
│   ├── Routing
│   ├── Server
│   ├── Session
│   ├── Shared
│   ├── Support
│   ├── Testing
│   ├── Translation
│   ├── Validation
│   ├── vendor
│   │
│   ├── View
│   └── Websocket
├── Arch
│   └── ScehdulePlanner
│       └── Src
│           ├── APIs
│           ├── Helper
│           ├── Interface
│           └── Workers
└── Storage
    ├── Css
    ├── Html
    ├── Js
    ├── Public
    └── Template

</pre>
<br /><br />
### Full API - Example Config File Per MicroService:
<pre>
{
    "Constants": {},
    "Codes": {},
    "Objects": {},
    "Workers": {
        "CalenderAPI": [
            {
                "seq": 0,
                "workerName": [
                    "printStartDate"
                ],
                "result": {
                    "success": 1,
                    "failure": -1
                }
            },
            {
                "seq": 1,
                "workerName": [
                    "printendDate"
                ],
                "result": {
                    "success": 2,
                    "failure": -1
                }
            },
            {
                "seq": 2,
                "workerName": [
                    "printStartToEndDateMonths"
                ],
                "result": {
                    "success": -1,
                    "failure": -1
                }
            }
        ]
    },
    "APIs": {
        "CalenderAPI": {
            "inputs": {
                "post": [
                    "start_date",
                    "end_data"
                ]
            },
            "relation": [],
            "plugin": false,
            "stream": false,
            "async": false,
            "events": false,
            "intenal": false,
            "scaled": false,
            "auth": {
                "jwt": false
            },
            "type": "api",
            "group": [],
            "lang": [
                "en"
            ],
            "validate": {
                "rules": {
                    "start_date": "required|notEmpty"
                }
            },
            "objects": [
                "Callers"
            ],
            "external_apis": {
                "api_url": "inputs|values"
            },
            "configuration": [],
            "helpers": [],
            "injectors": [],
            "storage": [
                "s3",
                "local"
            ],
            "Workers": [
                "CalenderV1API"
            ],
            "output": ["json"]
        }
    }
}
</pre>
