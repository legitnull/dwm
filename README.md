```
    ..                         .colclll;.               .;,
   .x-1c                        .xNNkl:'.   .,,.        .dWK;
   .xW-1'        ....'..         .kNx.      :XNk'       .OWNx.
.,,'oNNd;:clodxkkkk-1XXo          'ONo.     'OWN0;      :XNW0,
:OK-1KNWXOxdlc:,'...oNXc,xl.    .. :XK:      oNNNK:   .cONXNXc
 ...,OWK:         ,-1Wx..lXx. .dXd..dNO.     ;KNNNKc .dNNOo0Wd.
     oNNl        'ONx.  .dNl ,-1WXx.'ONl     .xNK0NXloXWX:.xWO'
     ;XWx.      ;-1Nd.    '00':XKOXO,cX0,     cNKldNNNNXo  cNX:
     .OW-1'    .lKKl.      dNloNd.oX0ldXd.    '0Nl.oKKd:.  ,0Wd.
     .dWX:   ,kXk'        :XOOXc  cKKkKXc    .xWx. ..     .xW-1'
      cXWd.,xKO;          .ONNK,   ,ONNNK:   .dW-1,         cNNc
      ,0WKO0x;.           .dNWO.    .oXNWO'kX00NX;         'OWk.
;xkdllxXWNx.               lNNo       ;0NNd.l0NNX:          oNXc
,xO0Oxoll;.                :Kk.        .dOl  .d0d.          '0WO'
  ..                       ...           .     .             ,ol'
```


# dwm - dynamic window manager 
dwm is an extremely fast, small, and dynamic window manager for X.


## Requirements
In order to build dwm you need the Xlib header files.


## Installation
Edit config.mk to match your local setup (dwm is installed into
the /usr/local namespace by default).

Afterwards enter the following command to build and install dwm (if
necessary as root):

    make clean install


## Running dwm
Add the following line to your .xinitrc to start dwm using startx:

    exec dwm

In order to connect dwm to a specific display, make sure that
the DISPLAY environment variable is set correctly, e.g.:

    DISPLAY=foo.bar:1 exec dwm

(This will start dwm on display :1 of the host foo.bar.)

In order to display status info in the bar, you can do something
like this in your .xinitrc:

    while xsetroot -name "`date` `uptime | sed 's/.*,//'`"
    do
    	sleep 1
    done &
    exec dwm


## Configuration
The configuration of dwm is done by creating a custom config.h
and (re)compiling the source code.


## Keybinds
NOTE: Windows Key is Mod
````
Mod+H = Increase cfact   
Mod+L = Decrease cfact   
Mod+\ = Previously selected   
Mod+j = Next to selected   
Mod+k = Previous to selected   
Mod+q = First position   
Mod+a = Second position   
Mod+z = Third position   
Mod+x = Last position   
Mod+U = Bottom stack   
Mod+O = Bottom stack horizontal
MOD
```

## Added
https://dwm.suckless.org/patches/activetagindicatorbar/

Volume and Brightness Keys

https://dwm.suckless.org/patches/cfacts/

https://dwm.suckless.org/patches/stacker/

https://dwm.suckless.org/patches/bottomstack/

https://dwm.suckless.org/patches/fibonacci/