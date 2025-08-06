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

1\. Download the APT Signing Key.

```
wget https://www.kicksecure.com/keys/derivative.asc
```

Users can [check the Signing Key](https://www.kicksecure.com/wiki/Signing_Key) for better security.

2\. Add the APT Signing Key.

```
sudo cp ~/derivative.asc /usr/share/keyrings/derivative.asc
```

3\. Add the derivative repository.

```
echo "deb [signed-by=/usr/share/keyrings/derivative.asc] https://deb.kicksecure.com trixie main contrib non-free" | sudo tee /etc/apt/sources.list.d/derivative.list
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

See instructions.

NOTE: Replace `generic-package` with the actual name of this package `rads`.

* **A)** [easy](https://www.kicksecure.com/wiki/Dev/Build_Documentation/generic-package/easy), _OR_
* **B)** [including verifying software signatures](https://www.kicksecure.com/wiki/Dev/Build_Documentation/generic-package)

## Contact ##

* [Free Forum Support](https://forums.kicksecure.com)
* [Premium Support](https://www.kicksecure.com/wiki/Premium_Support)

## Donate ##

`rads` requires [donations](https://www.kicksecure.com/wiki/Donate) to stay alive!
