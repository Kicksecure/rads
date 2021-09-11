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

1\. Download Whonix's Signing Key.

```
wget https://www.whonix.org/patrick.asc
```

Users can [check Whonix Signing Key](https://www.whonix.org/wiki/Whonix_Signing_Key) for better security.

2\. Add Whonix's signing key.

```
sudo cp ~/derivative.asc /usr/share/keyrings/derivative.asc
```

3\. Add Whonix's APT repository.

```
echo "deb [signed-by=/usr/share/keyrings/derivative.asc] https://deb.whonix.org bullseye main contrib non-free" | sudo tee /etc/apt/sources.list.d/derivative.list
```

4\. Update your package lists.

```
sudo apt-get update
```

5\. Install `rads`.

```
sudo apt-get install rads
```

## How to Build deb Package from Source Code ##

Can be build using standard Debian package build tools such as:

```
dpkg-buildpackage -b
```

See instructions. (Replace `generic-package` with the actual name of this package `rads`.)

* **A)** [easy](https://www.whonix.org/wiki/Dev/Build_Documentation/generic-package/easy), _OR_
* **B)** [including verifying software signatures](https://www.whonix.org/wiki/Dev/Build_Documentation/generic-package)

## Contact ##

* [Free Forum Support](https://forums.whonix.org)
* [Professional Support](https://www.whonix.org/wiki/Professional_Support)

## Donate ##

`rads` requires [donations](https://www.whonix.org/wiki/Donate) to stay alive!
