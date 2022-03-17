<div align=center>
  <h1>Langtons ant</h1>
  <b>Langtons ant simulation made in C using SDL2.</b><br>
  Based on <a href="https://github.com/r4v10l1/LangtonsAnt">r4v10l1/LangtonsAnt</a>.
</div>

# Table of contents
1. [Description](https://github.com/r4v10l1/langtons-ant-c#Description)
2. [Possible settings](https://github.com/r4v10l1/langtons-ant-c#Possible-settings)
    - [General](https://github.com/r4v10l1/langtons-ant-c#General)
    - [Colors](https://github.com/r4v10l1/langtons-ant-c#Colors)
    - [Color list](https://github.com/r4v10l1/langtons-ant-c#Possible-colors)
4. [TODO](https://github.com/r4v10l1/langtons-ant-c#TODO)


## Description
The program creates a window with SDL2 and renders the langtons ant in real time.

## Possible settings

Can be edited in `config.cfg`

### General

Setting         | Description                                                  | Default value
----------------|--------------------------------------------------------------|----------------
`WINDOW_W`      | Window width                                                 | 1200
`WINDOW_H`      | Window height                                                | 750
`CELL_SIZE`     | Cell size in pixels                                          | 10
`FPS`           | Frames per seccond when space is not pressed                 | 750
`DELAY`         | Time that the program will wait when holding the space (ms)  | 100
`DEBUG_PRINT`   | Will display debug information if **1**                      | 0

### Colors

Setting         | Description                                                     | Default value
----------------|-----------------------------------------------------------------|----------------
`COLOR_NUMBER`  | Number of color asociations that the program will use (Max 9)   | 2
`BACKGROUND_R`  | Red value used for the background                               | 0
`BACKGROUND_G`  | Green value used for the background                             | 0
`BACKGROUND_B`  | Blue value used for the background                              | 0
`GRID_COLOR`    | Color of the grid if active. RGB (Grayscale)                    | 100

### Possible rotations
`0` for *ClockWise* and `1` for *CounterClockWise*.
```cfg
# 0 - CW
# 1 - CCW
rotation_0 = 0
rotation_1 = 1
rotation_2 = 0
rotation_3 = 1
...
```

### Possible colors
Possible colors for the configuration file.

Each color will replace the last one (2 will replace 1; 1 will replace 0...).
The first one (0) will replace the last one, wich is determined by `COLOR_NUMBER`.

Example:

```cfg
color_0 = 1             # Will set color 0 (FIRST) to Black. Will replace the last one (delends on COLOR_NUMBER).
color_1 = 3             # Will set color 1 (SECCOND) to Red. Will replace Black.
color_3 = 5             # Will set color 3 to Yellow. Will replace Red.
```

Code  | Color       | RGB value
------|-------------|-------------
**1** | Black       | (0,0,0)
**2** | White       | (255,255,255)
**3** | Red         | (255,0,0)
**4** | Orange      | (255,165,0)
**5** | Yellow      | (255,255,0)
**6** | Green       | (0,255,0)
**7** | Blue        | (0,0,255)
**8** | Purple      | (160,32,240)
**9** | Pink        | (255,68,204)

## TODO
- [ ] Multiple ants with Mouse1
