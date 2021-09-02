# Jules custom keyboard

## installation

Copy `symbols` into `/usr/share/X11/xkb/symbols`.

```.bash
cp ./symbols/* /usr/share/X11/xkb/symbols/
```

Change `/usr/share/X11/xkb/rules` according to files in `rules`:
 * add 
   
   ```
     custom          Custom (US)
   ```

    under `! layout` in `base.lst` and `evdev.lst`
 * and in `base.xml` and `evdev.xml` add the corresponding

   ```
   <layout>
      <configItem>
        <name>custom</name>
        <shortDescription>custom</shortDescription>
	  <description>Custom</description>
        <languageList><iso639Id>eng</iso639Id></languageList>
      </configItem>
      <variantList/>
    </layout>
   ```
   
   in the `<layoutList>` element


## Usage

Select the layout in your OS config.

## Credits

<https://ubuntu-mate.community/t/make-your-own-custom-keyboard-layout-for-linux/19733>
