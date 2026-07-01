<!--
<snap-name>: This is the name of the snap. The name that is registered on the snap store and also the name of the cli command.
<snap-friendly-name>: This name is just a friendly name for the snap, it can be used in the README and nowhere else.
<api-port>: The port that the inference snap will use for its API server.
<webui-port>: The port that the inference snap will use for its webui server.
<http-host>: The host that the inference snap will use for its API and webui servers.
-->

# <snap-friendly-name> inference snap

Available engines:
* intel-cpu
* intel-gpu
* nvidia-cuda
* cpu

#### Install
```
sudo snap install <snap-name>
```
#### Use
```
<snap-name> --help
```


#### Default ports
| Configuration |              |
|---------------|--------------|
| http server   | <api-port>   |
| webui server  | <webui-port> |
| http host     | <http-host>  |

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

## Pack a snap with AI agents
Clone the [inference-snaps-sdk](https://github.com/canonical/inference-snaps-sdk) and build it:

```shell
git clone https://github.com/canonical/inference-snaps-sdk.git
cd inference-snaps-sdk
sdkcraft try
```

Then you can start the `workshop` environment and pack your snap with AI agents:

```shell
workshop launch
workshop shell
opencode
```

Choose the preferred LLM in opencode and prompt `start packing` to pack your snap with AI agents.
