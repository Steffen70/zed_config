## My personal Zed configuration files

### Installation

Unfortunatelly is Zed not in the official Ubuntu or Debian extrepos, so you have to install it manually.
I usually install it with the tarball to the `/opt/` directory.

After installing Zed to the `/opt/` directory, you need to create the symbolic links to have it available in your `$PATH` and make it available in the KDE menu.

```bash
# To create the symbolic links
sudo ln -s /opt/zed/zed /usr/local/bin/zed

# To create the desktop file
cp /opt/zed/share/applications/zed.desktop ~/.local/share/applications/dev.zed.Zed.desktop
sed -i "s|Icon=zed|Icon=/opt/zed/share/icons/hicolor/512x512/apps/zed.png|g" ~/.local/share/applications/dev.zed.Zed.desktop
sed -i "s|Exec=zed|Exec=/opt/zed/libexec/zed-editor|g" ~/.local/share/applications/dev.zed.Zed.desktop
```
