# Utils for CI with Java programs

A generic ci-settings.xml file for Maven projects

## Usage

create and source an `env.sh` file with the following content:

```bash
# SonarQube configuration
SONAR_URL=              # URL of the SonarQube server
SONAR_TOKEN=            # User token for SonarQube authentication

# Maven proxy configuration
MAVEN_PROXY_URL=        # URL of the Maven proxy server
MAVEN_PROXY_USERNAME=   # Username for the Maven proxy (leave blank if not used)
MAVEN_PROXY_TOKEN=      # Token for the Maven proxy (leave blank if not used)

# GitHub configuration
GITHUBORG=              # Name of the GitHub organization or Account
GITHUBACTOR=            # GitHub username (leave blank if not used)
GITHUBTOKEN=            # GitHub access token (leave blank if not used)

# Docker Hub configuration
DOCKERHUB_TOKEN=        # Docker Hub token (leave blank if not used)

# Maven Central configuration
MAVEN_CENTRAL_USERNAME= # Username for Maven Central (leave blank if not used)
MAVEN_CENTRAL_TOKEN=    # Token for Maven Central (leave blank if not used)
```

Use this file with maven commands:

```bash
mvn -s ci-settings.xml clean install
```

