Prezto - Matt's Fork
===================

This is my fork of Prezto with customized configurations, modules, and themes.

See the original repo and associated readme [here](https://github.com/sorin-ionescu/prezto).

Prezto will work with any recent release of Zsh, but the minimum required
version is 4.3.17.

  1. Launch Zsh:

        `zsh`

  2. Clone the repository:

        `git clone --recursive https://github.com/sorin-ionescu/prezto.git "${ZDOTDIR:-$HOME}/.zprezto"`

  3. Create a new Zsh configuration by copying the Zsh configuration files
     provided:

        ```
        setopt EXTENDED_GLOB
        for rcfile in "${ZDOTDIR:-$HOME}"/.zprezto/runcoms/^README.md(.N); do
          ln -s "$rcfile" "${ZDOTDIR:-$HOME}/.${rcfile:t}"
        done
        ```

     Note: If you already have any of the given config files, ln will error. In
     simple cases you can add `source "${ZDOTDIR:-$HOME}/.zprezto/init.zsh"` to
     the bottom of your `.zshrc` to load prezto but keep your config intact. For
     more complicated setups, it is recommended that you back up your original
     configs and replace them with the provided prezto runcoms.

  4. Set Zsh as your default shell:

        `chsh -s /bin/zsh`

  5. Open a new Zsh terminal window or tab.

### Troubleshooting

If you are not able to find certain commands after switching to *Prezto*,
modify the `PATH` variable in *~/.zprofile* then open a new Zsh terminal
window or tab.

Updating
--------

Pull the latest changes and update submodules.

    git pull && git submodule update --init --recursive

Usage
-----

Prezto has many features disabled by default. Read the source code and
accompanying README files to learn of what is available.

### Modules

  1. Browse */modules* to see what is available.
  2. Load the modules you need in *~/.zpreztorc* then open a new Zsh terminal
     window or tab.

### Themes

  1. For a list of themes, type `prompt -l`.
  2. To preview a theme, type `prompt -p name`.
  3. Load the theme you like in *~/.zpreztorc* then open a new Zsh terminal
     window or tab.

     ![sorin theme][2]

Customization
-------------

The project is managed via [Git][3]. It is highly recommended that you fork this
project; so, that you can commit your changes and push them to [GitHub][4] to
not lose them. If you do not know how to use Git, follow this [tutorial][5] and
bookmark this [reference][6].

Resources
---------

The [Zsh Reference Card][7] and the [zsh-lovers][8] man page are indispensable.

License
-------
This project is licensed under the MIT License.

