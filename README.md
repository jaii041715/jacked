<p align="center">
<img src="https://user-images.githubusercontent.com/60867540/202974737-11950c32-9ab4-480f-a3da-afebdaf6489c.svg" style="display: block; margin-left: auto; margin-right: auto; width: 50%;">
</p>

# Jacked

Jacked is a Vulnerability Container Image Scanner.
- 🧰 | [Install the Binary](https://github.com/jaii041715/jaii041715/blob/main/README.md#Installation)
- 🗂️ | Works with [Diggity](https://github.com/carbonetes/diggity) (SBOM Container Image and File System) 

## Installation

Copy to clipboard, paste it to the terminal.

``` curl
curl -sSfL https://raw.githubusercontent.com/carbonetes/jacked/main/install.sh | sh -s -- -b /usr/local/bin
```
## Usage
``` go
 jacked [image]
```
- 📥 | Jacked will check if Vulnerability Database exist, download / update action.
- 🐞 | Jacked will perform a Vulnerability Scan.
 
### Output formats
The output format for Jacked is configurable as well:

``` bash
jacked [image] -o [format]
```
Where the formats available are:

`table` A columnar summary, specified important details (default).
<br>
`json` Gives you a lot more detailed information in Jacked.
  
### Quiet mode
No UI loader for scanning images and removes unnecessary display that helps you when you're saving a JSON file.
``` bash
jacked [image] -q
```

### Combine output formats
Enable quiet mode together with preferred output.
``` bash
jacked [image] -q -o [format]
```

## Configuration
Configuration options (example values are the default):
``` yaml
# the output format of the vulnerability report (options: table, json)
# same as -o ; table/json output
# same as -q ; quiet mode
output:
 quiet: false
 type: "table"
```

## Features
- Scan the contents of a container image or filesystem to find known vulnerabilities.
- Find vulnerabilities for major operating system packages:
- Alpine
- Amazon Linux
- BusyBox
- CentOS
- Debian
- Distroless
- Oracle Linux
- Red Hat (RHEL)
- Ubuntu
- Find vulnerabilities for language-specific packages:
- Ruby (Gems)
- Java (JAR, WAR, EAR, JPI, HPI)
- JavaScript (NPM, Yarn)
- Python (Egg, Wheel, Poetry, requirements.txt/setup.py files)
- Dotnet (deps.json)
- Golang (go.mod)
- PHP (Composer)
- Rust (Cargo)
- Supports Docker, OCI and Singularity image formats.
- Consume SBOM attestations.
If you encounter an issue, please let us know using the [issue tracker](https://github.com/jaii041715/jaii041715/edit/main/README.md).
