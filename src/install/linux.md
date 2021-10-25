# Installing MCsniperGO on Linux

> ⚠️ This *brief* guide will assume you know how to navigate the Linux command line.


## READ. ALL. THE. TEXT.
it's not hard, read it all. it's all important.

## Connect to VPS

> ⚠️ *skip this if you're doing this on a main computer*

The first step for most people is to connect to their Linux VPS. I recommend using Ubuntu as a host operating system for VPS. If you don't have any VPS at the moment, you can use my affiliate codes for [DigitalOcean](https://m.do.co/c/c6b4729acf8c) and [Vultr](https://www.vultr.com/?ref=8671284-6G) for free (with credit card linked) VPS.

To connect to your vps, open a terminal or command prompt and type `ssh root@ip` and press enter, replace `root` with a different user if you changed users (if you don't know, leave as root) and replace `ip` with the ip address of your vps. Next, paste in your VPS password when asked (you can paste into command prompt on windows with right click).

## Install

Here's a one-liner to run that will download or update your MCsniperGO whenever run:

`wget -q $(curl -s "https://api.github.com/repos/Kqzz/MCsniperGO/releases" | tac | grep "browser_download_url" | grep "Linux_64-bit" | tail -n 1 | awk -F '"' '{print $4}') && chmod +x $(ls -l | grep "MCsniperGO" | awk '{print $NF}') && echo "MCsniperGO successfully set up"`

^ Just paste that into your VPS shell and press enter.


For that to work, you need `wget`, `curl`, `grep`, `awk`, and `tail` installed. Those all should be installed by default, but if they're not, type `sudo apt update && sudo apt install wget curl grep awk tail`.

## Running the sniper

To run that executable that was installed from the one-liner, just type `./executable-name-here`. If you don't know the executable name, type `ls` and locate it (it should be named something along the lines of `MCsniperGO_X.XX_Linux_64-bit`).

This will create `accounts.txt` and `config.toml`, you can leave `config.toml` alone unless you know you absolutely want to change something. `accounts.txt` **MUST** be edited, since you need to input your accounts there. Refer to the [accounts](../accounts.md) section for that.

> ⚠️  THE VPS SHELL / TERMINAL MUST BE OPEN FOR THE SNIPER TO CONTINUE RUNNING

## Sniping Again

The next time you want to snipe, connect to your vps according to the "Connect to VPS" section and run the sniper according to the "Running the sniper" section
