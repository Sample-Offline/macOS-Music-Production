# macOS-Music-Production
My guide (mostly to myself) for setting up plugins/music production tools on macOS.

## macOS VST2/VST3 install guide (for custom folders)

```
Tested on macOS 13.2 Ventura
```

For this example, I'll use [Serum VST](https://xferrecords.com/product_downloads/serum)

### 1. Install `.pkg` file using built-in installer

Install should put the `.vst3` file in either:

```
/Library/Audio/Plug-Ins/VST2
/Library/Audio/Plug-Ins/VST3
```

As well as some `.component` files in:

```
/Library/Audio/Plug-Ins/Components
```

### 2. Copy the files to a local user folder. 

```
mv /Library/Audio/Plug-Ins/VST3/* ~//Music/Ableton/Plugins/VST3 
mv /Library/Audio/Plug-Ins/VST/* ~//Music/Ableton/Plugins/VST2
```

If there are any `.component` files added, I copy those too:

```
mv /Library/Audio/Plug-Ins/Components/* ~/Music/Ableton/Plugins/VST2/Components
```

### 3. Change the user presets to use a local user directory  

Now to make the user presets local and not have them be in the `Macintosh HD/ Library/` dir, I create a softlink to my custom folder in the default location Serum expects. For this example, I used Ableton's User Lib folder:

```
mkdir -p ~/Music/Ableton/User\ Library\Presets\Third-party/Serum/User
ln -s ~Music/Ableton/User\ Library/Presets/Third-party/Serum/User /Library/Audio/Presets/Xfer\ Records/Serum\ Presets/Presets/User
```

### 4. Point Ableton or whatever to the custom folders

In Ableton:

**Settings** > **Use VST3 Plug-in Custom Folder**:  ☑️

**VST3 Plug-In Custom Folder**: `/Users/<username>/Music/Ableton/Plugins/VST3`

Click **Rescan Plug-Ins** and it should load correctly. To get the custom Presets folder to appear in Serum, I had to restart Ableton. 
