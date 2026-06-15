 External files not loading correctly inside sandboxed `<iframes>` on Windows. 
 
 The  developers have implemented a simple script inlining step during build time that takes the content of scripts relative to the Isolation application and injects them inline.

Typical bundling or simple including of files like `<script src="index.js"></script>` still works properly, but newer mechanisms such as ES Modules will _not_ successfully load.