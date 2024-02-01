# NucleiSnippets

<pre>
                     __     _               _                  __
   ____  __  _______/ /__  (_)  _________  (_)___  ____  ___  / /______
  / __ \/ / / / ___/ / _ \/ /  / ___/ __ \/ / __ \/ __ \/ _ \/ __/ ___/
 / / / / /_/ / /__/ /  __/ /  (__  ) / / / / /_/ / /_/ /  __/ /_(__  )
/_/ /_/\__,_/\___/_/\___/_/  /____/_/ /_/_/ .___/ .___/\___/\__/____/
                                         /_/   /_/
</pre>

## Overview

NucleiSnippets is repository dedicated to serving as a quick reference for creating templates in the Nuclei vulnerability scanner. The main goal is to provide a swift guide, showcasing protocols, functions, regex tips and unusual uses for this tool.

## What is Nuclei?

[Nuclei](https://nuclei.projectdiscovery.io/) is a versatile and fast vulnerability scanner that allows you to define scanning templates for various security checks.

## Getting Started

To dive into the world of NucleiSnippets, follow these steps:

## Requirements to test locally

- Git
- Docker / Docker Compose

**Clone the Repository:**

```bash
   git clone https://github.com/ricardomaia/NucleiSnippets.git
   cd NucleiSnippets
   docker-compose up -d
   docker exec -it nuclei-snippets-scanner nuclei -t /nuclei-snippets/templates -u http://host.docker.internal:1337 -nh -vv -v
```

## Examples

### HTTP

```bash
docker exec -it nuclei-snippets-scanner nuclei -t /nuclei-snippets/templates/http.yaml -u http://target.local -nh -vv -v
```

### CVE-2024-XXXX

The passphrase for the private key in this project is an empty string ``.

By default, Nuclei ignore template execution with tags: "fuzz", "dos", "local" or "privesc".

To execute this template, you need set the flag `-itags` (include tags) for "local" and "privesc". For code templates you need to include the flag `-code` as well.

So the complete command to execute the template is:

```bash
docker exec -it nuclei-snippets-scanner nuclei -t /nuclei-snippets/templates/cve-2024-XXXX.yaml -vv -v -code -itags local -itags privesc -debug
```

## Roadmap

- [x] Create a Docker environment to test the templates
- [ ] API consuption template
  - [ ] IP Reputation
  - [ ] Phishing URL
  - [ ] Site Health
- [ ] Data Leak
  - [ ] PII
  - [ ] Financial
  - [ ] Confidential documents
  - [ ] Credentials
  - [ ] API Keys
  - [ ] Sensible database information
- [ ] Forensics
  - [ ] Windows Registry
  - [ ] Linux Logs
