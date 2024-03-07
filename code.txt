from win32gui import *
from win32api import *
import time

hwnd = GetDesktopWindow()
hdc2 = GetWindowDC(0)
x2 = GetSystemMetrics(0)
y2 = GetSystemMetrics(0)
time.sleep(10)


def tunnel_effect():
    for i in range(100):
        StretchBlt(hdc2, 25, 25, x2 - 50, y2 - 50, hdc2, 0, 0, x2, y2, 0x563457)


def patinvert():
    for i in range(5):
        PatBlt(hdc2, 0, 0, x2, y2, 5898313)
        time.sleep(3)


def ered():
    for i in range(40):
        StretchBlt(hdc2, 25, 25, x2 - 50, y2 - 50, hdc2, 0, 0, x2, y2, 0x777777)
        time.sleep(1)
        StretchBlt(hdc2, 25, 25, x2 - 50, y2 - 50, hdc2, 0, 0, x2, y2, 0x000000)

def stretch_blt():
    for i in range(100):
        StretchBlt(hdc2, 0, 0, x2, y2 - 80, hdc2, 0, 0, x2, y2, 0x34323e)
for i in range(300):
    StretchBlt(hdc2, 25, 25, x2 - 80, y2 - 80, hdc2, 0, 0, x2, y2, 0x675667)
tunnel_effect()
patinvert()
ered()
for i in range(10):
    stretch_blt()

