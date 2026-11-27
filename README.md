# Research Link Checker

## Project Overview

This project explores how automated tools can identify broken links
in research documentation using GitHub Actions.

## Why This Matters

Research projects often rely on external sources, scientific papers,
datasets, and documentation. Over time, some links may become
unavailable or redirect to different pages.

## Project Objectives

- Understand how GitHub Actions works.
- Set up an automated link-checking workflow.
- Test working and broken links.
- Evaluate the usefulness and limitations of automated checking.

## Status

Currently in development.
## Test Links

- GitHub: https://github.com/
- Python: https://www.python.org/
## Test Results

### Test 1 — Broken Link Detection

- Two links returned successful responses.
- The intentionally broken HTTPBin URL returned `404 Not Found`.
- Lychee reported one error.
- GitHub Actions failed with exit code 2.

### Test 2 — Clean Repository

- The broken test URL was removed.
- Both remaining links passed validation.
- Lychee reported 2 successful links and 0 errors.
- GitHub Actions completed successfully.

### Conclusion

The experiment demonstrated that Lychee can detect an HTTP 404 response in a README file and that GitHub Actions can use the result to determine whether a workflow passes or fails.  
## Workflow Evidence

### Test 1: Broken Link Detection

![Failed workflow showing HTTP 404 detection](<ChatGPT Image Nov 27, 2026, 10_37_43 PM.png>)

The workflow detected the HTTP 404 response and failed with exit code 2.

### Test 2: Successful Link Validation

![Successful workflow showing two valid links](image.png)

After removing the broken URL, both remaining links passed validation.

