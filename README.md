# CAVE for VS Code

Check your project for Clean Architecture violations without leaving your editor.

Run one command and CAVE underlines every import that breaks a dependency rule, with an explanation of why.

> **Status:** In development (MVP).

## Usage

1. Open your project in VS Code.
2. Download the extension
3. Go into the file you want to check.
4. WINDOWS: ctrl + shift + p, MAC: command + shift + p. You should see “>” at the top. 
5. Type CAVE after the “>”, click on it, and any errors will display a pop up and show in the terminal. 

Example warning:

```
CAVE 11:15:18 AM 
⚠ CAVE found 1 Clean Architecture violation(s):

  ⚠ src\main\java\entity\Student.java:3
    Clean Architecture Violation: Student (entities) depends on controller. In Clean Architecture, entities must not depend on any other Clean Architecture component. (entities → controller)
```

## Settings
WIP

## Supported languages

Java, Python, JavaScript, and TypeScript. Java works best!

## How it works

The extension runs the [CAVE engine](./clean-architecture-visualizer) as a bundled child process (`cave verify --json`) and turns its results into VS Code. No separate install needed.

## Limitations
WIP

## Future Implementations
WIP
- Run on save
- Quick fixes

# Testing
 
You can also run CAVE's checks from the command line, no VS Code needed:
 
```bash
cave verify --json
```
 
Run it from the root of the project you want to check. Replace this with your actual test command if it differs.

