Normal scrollbar in Ubuntu
==========================
When I left-click anywhere above or below the thumb, it jumps to that position and starts dragging from there. The expected behavior is to scroll one page up or down. To change that:

```
sudo gedit /etc/gtk-3.0/settings.in
```

And add the following:

```
[Settings]
gtk-primary-button-warps-slider = false
```
