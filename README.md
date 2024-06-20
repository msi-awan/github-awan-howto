# Steps setup github cli


## 1. Install Github CLI

### macOS


#### Homebrew

| Install:          | Upgrade:          |
| ----------------- | ----------------- |
| `brew install gh` | `brew upgrade gh` |

#### MacPorts

| Install:               | Upgrade:                                       |
| ---------------------- | ---------------------------------------------- |
| `sudo port install gh` | `sudo port selfupdate && sudo port upgrade gh` |

#### Conda

| Install:                                 | Upgrade:                                |
|------------------------------------------|-----------------------------------------|
| `conda install gh --channel conda-forge` | `conda update gh --channel conda-forge` |

Additional Conda installation options available on the [gh-feedstock page](https://github.com/conda-forge/gh-feedstock#installing-gh).

#### Spack

| Install:           | Upgrade:                                 |
| ------------------ | ---------------------------------------- |
| `spack install gh` | `spack uninstall gh && spack install gh` |

#### Webi

| Install:                            | Upgrade:         |
| ----------------------------------- | ---------------- |
| `curl -sS https://webi.sh/gh \| sh` | `webi gh@stable` |

For more information about the Webi installer see [its homepage](https://webinstall.dev/).

### Linux & BSD

`gh` is available via:
- [our Debian and RPM repositories](./docs/install_linux.md);
- community-maintained repositories in various Linux distros;
- OS-agnostic package managers such as [Homebrew](#homebrew), [Conda](#conda), [Spack](#spack), [Webi](#webi); and
- our [releases page][] as precompiled binaries.

For more information, see [Linux & BSD installation](./docs/install_linux.md).

### Windows

#### WinGet

| Install:            | Upgrade:            |
| ------------------- | --------------------|
| `winget install --id GitHub.cli` | `winget upgrade --id GitHub.cli` |

> **Note**  
> The Windows installer modifies your PATH. When using Windows Terminal, you will need to **open a new window** for the changes to take effect. (Simply opening a new tab will _not_ be sufficient.)

#### scoop

| Install:           | Upgrade:           |
| ------------------ | ------------------ |
| `scoop install gh` | `scoop update gh`  |

#### Chocolatey

| Install:           | Upgrade:           |
| ------------------ | ------------------ |
| `choco install gh` | `choco upgrade gh` |


## 2. Create Personal Access Token 


##### 1. In the upper-right corner of any page on GitHub, click your profile photo, then click **Settings** 


##### 2. In the left sidebar, click **<> Developer settings**.

##### 3. In the left sidebar, click Personal access tokens.

##### 4. Click **Token(classic)**.

##### 5. Click Generate new token.

##### 6. In the **"Note"** field, give your token a descriptive name.

##### 7. To give your token an expiration, select **Expiration**, then choose a default option or click **Custom** to enter a date.

##### 8. Select the scopes you'd like to grant this token. To use your token to access repositories from the command line, select **repo**. A token with no assigned scopes can only access public information. For more information, see ["Scopes for OAuth apps"](https://docs.github.com/en/enterprise-server@3.9/apps/oauth-apps/building-oauth-apps/scopes-for-oauth-apps#available-scopes).

##### 9. Click Generate **token**.

##### 10. Optionally, to copy the new token to your clipboard

## 3. Authenticate with a GitHub Login via CLI 
##### 1. Enter this command on your cli 
```bash
gh auth login
```

##### 2. Fullfill this output :
```bash
? What account do you want to log into? [Choose GitHub.com]
? What is your preferred protocol for Git operations on this host? [Choose HTTPS]
? Authenticate Git with your GitHub credentials? [Choose Yes]
? How would you like to authenticate GitHub CLI? [Paste an authentication token]
```
