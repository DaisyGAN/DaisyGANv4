# PortTalbot
A telegram bot / DaisyGANv3.

My backprop was something to be desired in (PortTalbotv1)[https://github.com/DaisyGAN/PortTalbot], this version is a re-code to fix all of the issues in my prior code base.

## Install
- Compile `main.c` by running `compile.sh`
- Update the BOT KEY / ID in the `tgmain.php` and copy over to your `www` directory.
- Copy over one of the `main.c` binaries, such as `cfdgan` to the `www` directory
- `cd` into the `www` diretory and execute `cfdgan` as sudo.

## Example Usage
- ```./cfdgan retrain <optional file path>``` - Train the network from the provided dataset.
- ```./cfdgan "this is an example scentence"``` - Get a percentage of likelyhood that the sampled dataset wrote the provided message.
- ```./cfdgan rnd``` - Get the percentage of likelyhood that the sampled dataset wrote a provided random message.
- ```./cfdgan ask``` - A never ending console loop where you get to ask what percentage likelyhood the sampled dataset wrote a given message.
- ```./cfdgan gen``` - The adversarial message generator.
- ```./cfdgan``` - Telegram bot service, will digest the tsmsg.log every x messages and generate a new set of 10,000 quotes.
