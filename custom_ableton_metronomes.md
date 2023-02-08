# Custom Ableton Metronomes

## You'll need:

1. To create an `.adg` with 2 chains
2. Two sample files named `Metronome.wav` and `MetronomeUp.wav`


The metronomes live at:

```
/Applications/Ableton Live 11 Suite.app/Contents/App-Resources/Core Library/Defaults/Metronomes
```

### 1. Create your metronome samples

They should be of equal gain and start on a transient. Crop/clip or Consolidate. They don't work well if they're too long. Ideally, a single transient. 

### 2. Create an `.adg` with 2 chains

In Ableton, make a new **Instrument Rack** add a second chain, and label the first `MetronomeUp` and the second `Metronome`.
Add one sample to each chain. For some of the stock Ableton metronomes, they use a **Pitch** Audio Effect on the `Metronome` chain. 


### 3. Add your custom `metronome.adg` to the app dir

Your `.adg` file can be called anything that's ASCII characters. You could even call it `ö.õ.adg` 🤷‍♂️ 
The name of the file will show up as the selectable name in Ableton. 

You should also add the Sample files and their corresponding `.asd` to the metronome folder. For instance, if your metronome was called `ö.õ`

```
/Applications/Ableton Live 11 Suite.app/Contents/App-Resources/Core Library/Defaults/Metronomes/Samples/ö.õ
    +- Metronome.wav
    +- Metronome.wav.asd
    +- MetronomeUp.wav
    +- MetronomeUp.wav.asd
```

### 4. Restart Ableton and it should take effect


### Bonus:

If you want, you can check the stock Ableton `.adg` Metronomes by copying them from the app's metronome folder, then adding it to an Ableton project like any other `.adg` file. 
For example: `/Applications/Ableton Live 11 Suite.app/Contents/App-Resources/Core Library/Defaults/Metronomes/Click.adg`.
