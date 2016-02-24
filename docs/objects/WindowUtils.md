# WindowUtils class

All methods of this class are static. Many of the Windows-only functions here are utilized in the PyWin32 example.

<!-- START doctoc -->
<!-- END doctoc -->

## Methods

### OnSetFocus (Win)

| Parameter | Type |
| --- | --- |
| windowHandle | int |
| msg | long |
| wparam | long |
| lparam | long |
| __Return__ | void |

Windows-only. This method processes WM_SETFOCUS message which is sent to a window after it has gained the keyboard focus.

### OnSize (Win)

| Parameter | Type |
| --- | --- |
| windowHandle | int |
| msg | long |
| wparam | long |
| lparam | long |
| __Return__ | void |

Windows-only. This method processes WM_SIZE message which is sent to a window after its size has changed.

### OnEraseBackground (Win)

| Parameter | Type |
| --- | --- |
| windowHandle | int |
| msg | long |
| wparam | long |
| lparam | long |
| __Return__ | void |

Windows-only. This method processes WM_ERASEBKGND message which is sent when the window background must be erased (for example, when a window is resized).

### SetTitle (Win)

| Parameter | Type |
| --- | --- |
| browser | [Browser](Browser.md) |
| title | str |
| __Return__ | void |

Windows-only. Set the title for the main window or popup window. The default implementation of [DisplayHandler](../handlers/DisplayHandler.md).OnTitleChange() calls this method to set the title for a window.

### SetIcon (Win)

| Parameter | Type |
| --- | --- |
| browser | [Browser](Browser.md) |
| icon="inherit" | string |
| __Return__ | void |

Windows-only. Set the icon for the popup window. The default implementation of [DisplayHandler](../handlers/DisplayHandler.md).OnTitleChange() calls this method to set the icon for a window that wasn't created explicitily (for example a popup window), the icon is inherited from the parent window. Icon parameter accepts only "inherit", you cannot pass here a path to an icon (currently not implemented).

### GetParentHandle

| Parameter | Type |
| --- | --- |
| windowHandle | int |
| __Return__ | void |

Get a parent handle.

On Linux and Mac this method always returns 0. @TODO.

### IsWindowHandle

| Parameter | Type |
| --- | --- |
| windowHandle | int |
| __Return__ | void |

Check whether this is a valid window handle.

On Linux and Mac this method always returns True. @TODO.

### gtk_plug_new (Linux)

| Parameter | Type |
| --- | --- |
| long GdkNativeWindow | long |
| __Return__ | void |

Linux-only. This method is utilized in the PyQt example.

### gtk_widget_show (Linux)

| Parameter | Type |
| --- | --- |
| long GtkWidget* | long |
| __Return__ | void |

Linux-only. This method is utilized in the PyQt example.