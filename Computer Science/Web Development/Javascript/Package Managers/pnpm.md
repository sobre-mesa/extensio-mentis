Performant npm

- **Introduction**: Aimed at improving performance and disk space usage.
- **Features**:
    - Uses a unique approach by creating a single store of packages and linking dependencies, reducing disk space.
    - Efficient dependency resolution and installation.
    - `pnpm-lock.yaml` file ensures consistent installations.
    - Better support for monorepos with built-in workspaces.
- **Performance**: Typically faster than both npm and Yarn due to its efficient linking and storage mechanism.
- **Strictness**: Enforces stricter package management rules, which can help catch issues early but might require some adjustments in project setup.