# [model] inference snap

[description]


#### Default ports
| Configuration |  |
|---|---|
| http server | [port] |
| webui server | [port] |

## Resources

📚 **[Documentation](https://documentation.ubuntu.com/inference-snaps/)**, learn how to use inference snaps

💬 **[Discussions](https://github.com/canonical/inference-snaps/discussions)**, ask questions and share ideas

🐛 **[Issues](https://github.com/canonical/inference-snaps/issues)**, report bugs and request features

## Build and install from source

Clone this repo with its submodules:
```shell
git clone --recurse-submodules https://github.com/[repository]
```

Prepare the required models by running `make download-models`.

Build the snap and its component:
```shell
snapcraft pack -v
```

Refer to the `./dev` directory for additional development tools.
