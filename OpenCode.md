## Build, Lint, and Test

1. **Build**:
   - Use the command `go build ./...` to compile all Go packages in the directory.

2. **Lint**:
   - Run `golint ./...` to analyze the Go source code and identify potential style issues.
   - Use `go vet ./...` for checking for suspicious constructs.

3. **Test**:
   - Execute `go test ./...` to run all tests.
   - To run a specific test, use `go test -run ^TestName$ ./...`.

## Code Style Guidelines

- **Imports**:
  - Group imports into standard library, third-party, and local packages.
  - Follow alphabetical order within each group.

- **Formatting**:
  - Use `go fmt ./...` to ensure consistent code formatting across files.

- **Types and Variables**:
  - Use `camelCase` for variable names and `PascalCase` for exported variables.
  - Prefer short names for local variables, longer names for global variables.

- **Naming Conventions**:
  - Use descriptive names for variables and functions.
  - Exported functions and types should have a comment documenting their purpose.

- **Error Handling**:
  - Check and handle errors immediately after function returns.
  - Use `errors.Wrap` for adding context to errors when handling them.
