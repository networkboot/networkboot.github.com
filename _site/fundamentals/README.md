Whenever you export from Dia to SVG, you must remove the width/height
attributes on the root <svg> element. If you forget to do that, it will not
resize dynamically.
