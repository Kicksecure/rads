# RAM Adjusted Desktop Starter #

If there is more than X MB RAM in total, the desktop environment will be
started.

If less than X MB RAM in total (for example, only 196 MB RAM in total), no
desktop environment will be started.

This should be quite convenient, because users with low RAM could reduce Y MB
and even if they sometimes wanted to configure/check something, they could
assign 512 RAM and automagically boot into the graphical desktop. There are
also many settings in /etc/rads.d/ (stackable) to configure this feature, so
if you want, you can also add a lot RAM, but not boot into a desktop
environment, or use different display managers and so on.

Most useful in virtual machines.
## How to install `rads` using apt-get ##

1\. Add [Whonix's Signing Key](https://www.whonix.org/wiki/Whonix_Signing_Key).

```
sudo apt-key --keyring /etc/apt/trusted.gpg.d/whonix.gpg adv --keyserver hkp://ipv4.pool.sks-keyservers.net:80 --recv-keys 916B8D99C38EAF5E8ADC7A2A8D66066A2EEACCDA
```

3\. Add Whonix's APT repository.

```
echo "deb http://deb.whonix.org buster main contrib non-free" | sudo tee /etc/apt/sources.list.d/whonix.list
```

4\. Update your package lists.

```
sudo apt-get update
```

5\. Install `rads`.

```
sudo apt-get install rads
```

## How to Build deb Package ##

Replace `apparmor-profile-torbrowser` with the actual name of this package with `rads` and see [instructions](https://www.whonix.org/wiki/Dev/Build_Documentation/apparmor-profile-torbrowser).

## Contact ##

* [Free Forum Support](https://forums.whonix.org)
* [Professional Support](https://www.whonix.org/wiki/Professional_Support)

## Donate ##

`rads` requires [donations](https://www.whonix.org/wiki/Donate) to stay alive!
