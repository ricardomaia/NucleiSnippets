# NucleiSnippets

```text
                     __     _               _                  __      
   ____  __  _______/ /__  (_)  _________  (_)___  ____  ___  / /______
  / __ \/ / / / ___/ / _ \/ /  / ___/ __ \/ / __ \/ __ \/ _ \/ __/ ___/
 / / / / /_/ / /__/ /  __/ /  (__  ) / / / / /_/ / /_/ /  __/ /_(__  ) 
/_/ /_/\__,_/\___/_/\___/_/  /____/_/ /_/_/ .___/ .___/\___/\__/____/  
                                         /_/   /_/                     
```

## Overview

NucleiSnippets is repository dedicated to serving as a quick reference for creating templates in the Nuclei vulnerability scanner.  The main goal is to provide a swift guide, showcasing protocols, functions, regex tips and unusual uses for this tool.

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
   docker exec -it nuclei-snippets nuclei -t /nuclei-snippets/templates -u http://target.local
   ```
   

   
