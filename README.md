# PortTalbot
A telegram bot / DaisyGANv4.

The back-propagation was something to be desired in [PortTalbotv1](https://github.com/DaisyGAN/PortTalbot); this version is a re-code to fix all of the issues in the prior code base.

The discriminator this time is significantly better than in prior versions; however, the generator was still a resounding failure, probably due to the generator back-propagation; for some reason, I can only assume I am too inexperienced at this point to diagnose.

With the failure of the GAN I decided it would be a suitable alternative to generate random quotes/sentences using brute force, randomly generated and checked against the discriminator only outputting the generations with the specified maximum error.

As such I suggest using `./cfdgan genrnd 0.1` to `./cfdgan genrnd 0.001` to generate random quotes from the trained dataset.

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
- ```./cfdgan gen``` - The adversarial message/quote generator.
- ```./cfdgan genrnd <option max error>``` - The brute-force random message/quote generator.
- ```./cfdgan``` - Telegram bot service, will digest the tsmsg.log every x messages and generate a new set of 10,000 quotes.
