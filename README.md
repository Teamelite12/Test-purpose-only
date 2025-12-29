# Test Purpose Only

A simple demonstration repository showcasing basic HTML structure and GitHub workflow practices.

## Overview

This repository contains a minimal HTML page (`index.html`) that demonstrates:
- Clean HTML5 document structure
- Basic text display using semantic HTML elements
- Proper use of `<span>` and `<p>` tags

## Contents

- **index.html** - A simple HTML page with "help" and "settings" span elements and a greeting message
- **package.json** - Node.js package configuration for dependency management
- **.github/workflows/Cache.yaml** - GitHub Actions workflow demonstrating dependency caching

## GitHub Actions - Dependency Caching

This repository includes a comprehensive GitHub Actions workflow (`.github/workflows/Cache.yaml`) that demonstrates dependency caching for multiple package managers following [GitHub's official documentation](https://docs.github.com/en/actions/using-workflows/caching-dependencies-to-speed-up-workflows).

### Supported Package Managers

The workflow includes examples for:

1. **NPM (Node Package Manager)**
   - Caches: `~/.npm`
   - Cache key: Based on `package-lock.json` hash
   - Speeds up Node.js dependency installation

2. **Yarn**
   - Caches: Yarn cache directory
   - Cache key: Based on `yarn.lock` hash
   - Alternative Node.js package manager caching

3. **Pip (Python)**
   - Caches: `~/.cache/pip`
   - Cache key: Based on `requirements.txt` hash
   - Speeds up Python package installation

4. **Maven (Java)**
   - Caches: `~/.m2/repository`
   - Cache key: Based on `pom.xml` hash
   - Speeds up Java dependency resolution

5. **Gradle (Java/Kotlin)**
   - Uses: `gradle/gradle-build-action@v2.4.2`
   - Automatic caching of Gradle dependencies
   - Optimized for Gradle builds

### How Dependency Caching Works

The workflow uses GitHub's `actions/cache@v4` action to:
1. Generate a unique cache key based on dependency lock files
2. Check if a cache exists for that key
3. Restore the cache if available, or download dependencies if not
4. Save the cache after successful dependency installation

This significantly reduces build times by avoiding redundant dependency downloads.

### Cache Key Strategy

Cache keys follow this pattern:
```
${{ runner.os }}-<package-manager>-${{ hashFiles('<lock-file>') }}
```

With fallback restore keys for partial cache hits:
```
${{ runner.os }}-<package-manager>-
```

## Usage

Open `index.html` in any web browser to view the page. The page displays:
- Two inline text elements: "help" and "settings"
- A greeting message: "Hi"

## Purpose

This repository is used for testing and demonstration purposes, including:
- HTML development basics
- Git workflow practices
- Pull request processes
- Code collaboration
- GitHub Actions dependency caching patterns

## License

This is a test repository for educational and demonstration purposes.
