
- **Introduction**: Developed by Facebook to address some of npm's shortcomings.
- **Features**:
    - Faster dependency installation due to parallelism and caching.
    - `yarn.lock` file ensures consistent dependency versions across installations.
    - Checks for package integrity to avoid corrupted dependencies.
    - Improved command output and more readable error messages.
- **Workspaces**: Supports monorepo setups by managing multiple packages within a single repository.
- **Performance**: Generally faster than older versions of [[npm]] due to its caching mechanism and parallel installation.

#### **Yarn Berry PnP: A New Approach to Package Management**

Yarn Berry introduced the Plug'n'Play (PnP), eliminating the node_modules directory. Instead of installing each package's files to a node_modules directory, Yarn PnP creates a single **.pnp.js** file containing a map of package names to package locations on the disk. This approach leads to installation times and faster disk space usage.

	# To enable PnP in a new Yarn Berry project 
	yarn set version berry
	yarn config set pnpMode loose

