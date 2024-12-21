# Expo CLI Metro Bundler Error: Unclear Dependency Conflict

This repository demonstrates a bug encountered while using the Expo CLI, specifically an unclear error from the Metro bundler caused by a deeply nested dependency conflict. The conflict was difficult to diagnose due to its indirect nature.

## Bug Description

The error manifested as a vague Metro bundler error message that didn't directly point to the root cause. The actual problem was a conflict between two packages requiring different versions of a core dependency. This conflict was obscured by the nested structure of the dependencies within the project's `package.json`.

## Reproduction Steps

1. Clone this repository.
2. Navigate to the project directory.
3. Attempt to run the Expo CLI development server (`expo start`).
4. Observe the vague Metro bundler error message.

## Solution

The solution involves using the `resolutions` field in the `package.json` file to explicitly specify a compatible version of the conflicting dependency.  Refer to `bugSolution.js` for the corrected `package.json` file which resolves this conflict.

## Note

This bug highlights the importance of carefully examining dependencies in complex projects and utilizing tools to analyze dependency trees effectively to identify and resolve conflicts promptly.