# Build notes

## Local Build

### one time

* install local pip venv (or whatever) environment as in only to step 3!: <https://zmk.dev/docs/development/local-toolchain/setup/native>
* then `paru -S zephyr-sdk-bin`

```bash
mkdir ~/Development/github/petejohanson
git clone https://github.com/petejohanson/cirque-input-module ~/Development/github/petejohanson/cirque-input-module
```

### then Build

```bash
cd ~/Development/github/zmkfirmware/zmk/app
west build -p -b nice_nano_v2 -- -DSHIELD=raveniung -DZMK_EXTRA_MODULES="/home/spiff/Development/github/petejohanson/cirque-input-module;/home/spiff/Development/github/FearlessSpiff/raveniung-zmk-config"

```
