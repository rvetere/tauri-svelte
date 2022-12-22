# Tauri Svelte

- **Tauri**
- **GitHub action** for cross-platform builds
- **Svelte**
- **Vite**
- **TypeScript**
- **`svelte-preprocess`** with Sass installed by default
- **Hot module replacement**
- **ESLint**
- **Prettier**

## Dev instructions

### Get started

1. Install Node.js
2. Install Rust
3. Follow the [Tauri setup guide](https://tauri.studio/en/docs/get-started/intro)
4. Run `npm install`
5. Find and replace the text `tauri-svelte-template` and `Tauri Svelte Template`.

### Commands

- `npm run dev`: Start app in dev mode
- `npm run build`: Build
- `npm run lint`: Lint
- `npm run format`: Format

### Release new version

1. Update `CHANGELOG.md`
2. Bump the version number in `src-tauri/Cargo.toml`
3. Run `cargo check` to update `Cargo.lock`
4. Create a git tag in the format `v#.#.#`
5. Add release notes to the generated GitHub release and publish it

### Release new version with changeset

1. Run `npx changeset` to add a changeset
2. Run `npx changeset version` to bump version (and change CHANGELOG.md)
3. Set the same version to `src-tauri/Cargo.toml`
4. Run `cargo check` in `src-tauri` to update Cargo.lock
5. Run `npx changeset publish` to add github tag
6. Push everything in a new PR - when merging this PR, release pipeline will be triggered (by the tag)
