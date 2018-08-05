### DESCRIPTION

# Installation

Installation requires [`wx-pm`](https://github.com/RaffaeleCanale/wx-pm)

`cd` to the project directory and run:
```
wx install
```

# Usage
```
deploy <project> --targets <targets...> --dry-run
```
| Options | Description |
| :-------------: |:-------------|
| `project` | Name of the project to deploy (as defined in `.projects.json`) |
| `--targets` | Override the target(s) to deploy to (default: read from config) |
| `--dry-run` | Print deploy commands without executing them |

# Configuration

### Projects

Located at `./projects.json`
```json
{
    "<id>": {
        "name": "<project name (default: id)>",
        "type": "<project type>",
        "targets": "<target1>,<target2>,..."
    }
}
```

### Targets

Located at `./targets.json`
```json
{
    "<name>": {
        "user": "<ssh username>",
        "host": "<ssh hostname>",
        "workingDirectory": "<working directory in target device>"
    }
}
```
