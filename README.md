# Jules custom keyboard

```
┌─────┬─────┬─────┬─────┬─────┬─────┬─────┬─────┬─────┬─────┬─────┬─────┬─────┲━━━━━━━━━┓
│ ~ ̃  │ 1 ¹ │ 2 ̋  │ 3 ̄  │ 4 £ │ 5 ¸ │ 6 ̂  │ 7 ̛ │ 8 × │ 9 ÷ │ 0 ° │ _ – │ + ̛ ┃         ┃
│ ` ̀  │ ! ¡ │ @ ² │ # ³ │ $ ¤ │ % € │ ^ ¼ │ & ½ │ * ¾ │ ( ‘ │ ) ’ │ - — │ = ̋  ┃Backspace┃
┢━━━━━┷━┱───┴─┬───┴─┬───┴─┬───┴─┬───┴─┬───┴─┬───┴─┬───┴─┬───┴─┬───┴─┬───┴─┬───┺━┳━━━━━━━┫
┃       ┃ Q Ä │ W Â │ E É │ R È │ T Ê │ Y Ü │ U Ù │ I Û │ O Œ │ P Ô │ { “ │ } ” ┃Entrée ┃
┃ Tab   ┃ q ä │ w â │ e é │ r è │ t ê │ y ü │ u ù │ i û │ o œ │ p ô │ [ « │ ] » ┃       ┃
┣━━━━━━━┻┱────┴┬────┴┬────┴┬────┴┬────┴┬────┴┬────┴┬────┴┬────┴┬────┴┬────┴┬────┺┓      ┃
┃        ┃ A À │ S § │ D Ð │ F   │ G   │ H   │ J   │ K Œ │ L Ø │ : ̈  │ " ̈  │ | ¦ ┃      ┃
┃ Maj    ┃ a à │ s ß │ d ð │ f   │ g   │ h   │ j   │ k œ │ l ø │ ; ̨  │ ' ́  │ \ ’ ┃      ┃
┣━━━━━━━┳┹────┬┴────┬┴────┬┴────┬┴────┬┴────┬┴────┬┴────┬┴────┬┴────┬┴────┲┷━━━━━┻━━━━━━┫
┃       ┃ > ≥ │ Z Æ │ X   │ C Ç │ V   │ B   │ N Ñ │ M µ │ < ̌  │ > ̂  │ ? ̉  ┃             ┃
┃ Shift ┃ < ≤ │ z æ │ x   │ c ç │ v   │ b   │ n ñ │ m µ │ , ̧  │ . · │ / ¿ ┃ Shift       ┃
┣━━━━━━━╋━━━━━┷━┳━━━┷━━━┱─┴─────┴─────┴─────┴─────┴─────┴───┲━┷━━━━━╈━━━━━┻━┳━━━━━━━┳━━━┛
┃       ┃       ┃       ┃ Space              no break space ┃       ┃       ┃       ┃
┃Ctrl   ┃ Meta  ┃ Alt   ┃ Space              no break space ┃ AltGr ┃ Menu  ┃ Ctrl  ┃
┗━━━━━━━┻━━━━━━━┻━━━━━━━┹───────────────────────────────────┺━━━━━━━┻━━━━━━━┻━━━━━━━┛
```

## installation

Copy `symbols` into `/usr/share/X11/xkb/symbols`.

```.bash
sudo cp ./symbols/* /usr/share/X11/xkb/symbols/
setxkbmap -layout custom
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
