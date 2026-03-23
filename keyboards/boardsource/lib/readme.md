# QMK Oled images - 32x128 display

## Use
rules.mk

`OLED_ENABLE = yes`

keymap.c

`#include "oled.c"`

Create a file called oled.c
 
```
  static void render_logo(void) {
    ... YOUR IMAGE
    oled_write_raw_P(raw_logo, sizeof(raw_logo));
  };
```

If the image have rotation replace <YOUR_ROTATION> with the value
```
  oled_rotation_t oled_init_user(oled_rotation_t rotation) {
        return <YOUR_ROTATION>;
  }
```
### Horizontal

![batman](https://gist.github.com/assets/17733906/767a5325-fa5f-4a35-8df7-772eeb6a9fc4)
![cat](https://gist.github.com/assets/17733906/922f87c8-3f53-4c40-91ed-5df04de2c429)

### Vertical

![punisher](https://gist.github.com/assets/17733906/c5ca6de5-6f2c-43f5-88a2-e5dba3a5b6d4)
![skull](https://gist.github.com/assets/17733906/73fb1fc9-47f8-4623-a1d0-d50090bdb2f8)
![darkmark](https://gist.github.com/assets/17733906/a062aa2e-6271-49a1-b4b2-b6dd2b13274b)


- https://javl.github.io/image2cpp/
- https://joric.github.io/qle/

Vertical
punisher skull darkmark

https://javl.github.io/image2cpp/
https://joric.github.io/qle/
