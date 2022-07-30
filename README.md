# Chalk

A terminal string colorizer for the [V language](https://vlang.io).


## Installation

With vpm:
```
v install mewzax.chalk
```

## Usage

Chalk offers three functions:
- `chalk.fg(text string, color string)` - To change the foreground color.
- `chalk.bg(text string, color string)` - To change the background color.
- `chalk.style(text string, style string)` - To change the text style.

You can also use RGB and HEX values:
- `chalk.fg_rgb(text string, r int, g int, b int)`
- `chalk.bg_hex(text string, hex string)`

Example:

```v
import chalk

# basic usage
println('I am really ' + chalk.fg('happy', 'green'))

# you can also nest them
println('I am really ' + chalk.fg(chalk.style('ANGRY', 'bold'), 'red'))
```

Available colors:
- black
- red
- green
- yellow
- blue
- magenta
- cyan
- default
- light_gray
- dark_gray
- light_red
- light_green
- light_yellow
- light_blue
- light_magenta
- light_cyan
- white

Available styles:
- bold
- dim
- underline
- blink
- reverse
- hidden
