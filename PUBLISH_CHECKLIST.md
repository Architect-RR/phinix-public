# Publish Checklist

Before publishing this package, confirm the following.

## Repository

- A new GitHub repository exists.
- The repo name is final.
- Visibility is intentionally set to public or private.

## Content

- No tokens, secrets, or bridge credentials are included.
- No raw voice, dialogue, or training logs are included.
- No APK, SDK, JDK, or vendor blobs are included.
- No private bridge details are included.
- No unfinished capability is described as complete.

## Documentation

- README states the project clearly.
- PUBLIC_SCOPE defines the boundary clearly.
- CONTRIBUTING explains how to participate.
- ROADMAP shows a realistic direction.
- LICENSE is chosen intentionally.

## Community setup

- Issue templates are ready.
- PR template is ready.
- Expert invitation text is ready.
- Code of conduct is ready.

## First public release recommendation

Start with:

- this `github_public/` package
- cleaned architecture material
- abstract interfaces

Do not start with:

- the full private runtime
- sensitive embodiment chains
- training data
- vendor build artifacts
