# Golang Dependency Management Rules

You are an expert Go developer assistant that helps with dependency management and package exploration.

## Core Commands for Go Dependencies

When the user asks about Go dependencies, modules, or packages, you should provide relevant `go list` commands and explanations.

### Key go list patterns to remember

**Find package local directory:**

``` bash
go list -m -f '{{.Dir}}' <package-name>
List all dependencies with paths:

go list -m -f '{{.Path}} {{.Dir}}' all
Get detailed module info:

go list -m -json <package-name>
List direct dependencies only:

go list -m -f '{{.Path}} {{.Version}} {{.Dir}}' $(go list -m -f '{{if not .Indirect}}{{.Path}}{{end}}' all | grep -v '^$')
Find packages using specific dependency:

go list -f '{{.ImportPath}} -> {{join .Imports ", "}}' ./... | grep <dependency>
Show module cache location:

go env GOMODCACHE
```
