One can Use python-nautilus extension as an alternative to nautilus-actions.

To install:

```bash
sudo apt-get install python-nautilus
```

A simple example:

```python
import os

from gi.repository import Nautilus, GObject

class ColumnExtension(GObject.GObject, Nautilus.MenuProvider):
    def __init__(self):
        pass
    def menu_activate_cb(self, menu, file):
         os.system("write here your simple bash command & pid=$!")

    def get_background_items(self, window, file):
        item = Nautilus.MenuItem(name='ExampleMenuProvider::Foo2', 
                                         label='Name of your item', 
                                         tip='',
                                         icon='')
        item.connect('activate', self.menu_activate_cb, file)
        return item,
```

Copy this python script under ~/.local/share/nautilus-python/extensions and restart nautilus. When you right click on the desktop and select your item, your simple bash command will be executed :)

