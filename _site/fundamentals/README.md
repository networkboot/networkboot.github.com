Whenever you export from Dia to SVG, you must remove the width/height
attributes on the root <svg> element. If you forget to do that, it will not
resize dynamically.


```
dia --export=bios_post_and_bbs.svg -t svg bios_post_and_bbs.dia
sed --in-place '3s/svg width.*viewBox/svg viewBox/' bios_post_and_bbs.svg

mscgen -T svg -i classic_netboot.msc -o - | sed -e 4d > classic_netboot.svg
```
