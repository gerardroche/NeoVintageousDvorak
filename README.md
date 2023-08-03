# NeoVintageous Dvorak

Dvorak key mappings for [NeoVintageous](https://github.com/NeoVintageous/NeoVintageous).

Inspired by [vim-dvorak](https://github.com/agentlewis/vim-dvorak/blob/master/plugin/dvorak.vim).

## Installation

### Package Control installation

**Pending availability**

Install NeoVintageousDvorak via [Package Control](https://packagecontrol.io/packages/NeoVintageousDvorak).

### Manual installation

Close Sublime Text, then download or clone this repository to a directory named **NeoVintageousDvorak** in the Sublime Text Packages directory for your platform:

**Linux**

`git clone https://github.com/gerardroche/NeoVintageousDvorak.git ~/.config/sublime-text-3/Packages/NeoVintageousDvorak`

**OSX**

`git clone https://github.com/gerardroche/NeoVintageousDvorak.git ~/Library/Application\ Support/Sublime\ Text\ 3/Packages/NeoVintageousDvorak`

**Windows**

`git clone https://github.com/gerardroche/NeoVintageousDvorak.git %APPDATA%\Sublime/ Text/ 3/Packages/NeoVintageousDvorak`

## Setup

### NeoVintageous &gt;= v1.32

Configure NeoVintageous to source the Dvorak mappings **before** the neovintageousrc file is sourced.

| Setting | Description
| :------ | :----------
| `vintageous_source` | Read Ex commands from a resource before the neovintageourc resource is sourced. This means you can still override these ex commands in your neovintageousrc file. <br>Example: Packages/NeoVintageousDvorak/dvorak.neovintageous

Command Palette → Preferences: NeoVintageous Settings

```json
{
    "vintageous_source": "Packages/NeoVintageousDvorak/dvorak.neovintageous"
}
```

Reload your neovintageousrc file for changes to take effect.

Command Palette → NeoVintageous: Reload .neovintageousrc File

### NeoVintageous &lt; v1.32

Manually copy the contents of [dvorak.neovintageous](dvorak.neovintageous) into your neovintageousrc file and reload it for changes to take effect.

Command Palette → NeoVintageous: Open .neovintageousrc File

Command Palette → NeoVintageous: Reload .neovintageousrc File

## Key mappings

```
Dvorak layout:                   |                 QWERTY layout:
`12345 67890[]     Move around:  |  (instead of)   `12345 67890-=
 ',.py fgcrl/=\         n        |       k          qwert yuiop[]\
 aoeui dHTNS-         h   s      |     h   l        asdfg HJKL;'
 ;qjkx bmwvz            t        |       j          zxcvb nm,./

(  novx)  h = h (Left)     s = l= (Right)     n = k (Up)     t = j (Down)

(  novx)  l = b (Back word)            L = B (Back WORD)
(  novx)  y = w (Forward word)         Y = W (Forward WORD)
(  novx)  u = e (Forward end of word)  U = E (Forward end of WORD)

(c     )  <C-L> = <C-Left> (Back WORD)
(c     )  <C-Y> = <C-Right> (Seems to equal forward WORD minus 1 character)

(  n  x)  a = v (Visual)   A = V (Visual line)
(  n   )  r = r (Replace)  R = R (Replace)
(  n   )  s = i (Insert)   S = I (Insert before first non-blank of line)
(  n   )  t = a (Append)   T = A (Append at end of line)
(  n   )  w = c (Change)   W = C (Change to end of line)  ww = cc (Change line)

(  n  x)  z = u (Undo)    Z = <C-R> (Redo)  gz = U (Undo all latest changes on line)
(  n  x)  x = x (Cut)     X = dd (Cut line)
(  n  x)  c = y (Copy)    C = yy (Copy line)
(  n  x)  v = p (Paste)   V = P (Paste)
(  n  x)  gv = gp (Paste) gV = gP (Paste)

(   o  )  r = i (Example: dip -> drp (Delete inner paragraph))

(  no x)  p = t{char} (Before next {char})  P = T{char} (After previous {char})
(  no x)  b = ; (Repeat latest f or t)  B = , (Repeat latest f or t reversed)
(  no x)  k = n (Repeat latest / or ?)  K = N (Repeat latest / or ? reversed)

(  n  x)  j = z
(  n  x)  jn = zj (Next fold) [Also jj = zj]
(  n  x)  je = zk (Previous fold) [Also jk = zk]

(  n   )  ga = gv (Reselect last visual selection)
(  n  x)  gK = K (Lookup)
(  n  x)  gL = L (To line [count] from bottom of window)

(  n  x)  <C-W>h = <C-W>h (Window left)
(  n  x)  <C-W>n = <C-W>j (Window down)
(  n  x)  <C-W>e = <C-W>k (Window up)
(  n  x)  <C-W>i = <C-W>l (Window right)

Lost:
(  n  x)  H (To line [count] from top of window)
(  n  x)  s (Substitute [count] characters) [Use wi = cl]
(  n  x)  S (Substitute [count] lines) [Use ww = cc]
(  n  x)  X (Cut [count] characters backwards) [Use dh = dh]
(  n   )  Z (Quit)
(  n  x)  <C-W>n (Window down) [Use <C-W><C-N> = <C-W><C-N>]
(  n  x)  <C-W>i (Window down) [Use <C-W><C-I> = <C-W><C-I>]

Legend:
<C-X>     Ctrl-X
(c     )  Command-line mode
( i    )  Insert mode
(  n   )  Normal mode
(   o  )  Operator pending
(    v )  Visual+Select mode
(     x)  Visual mode
```
## License

Released under the [GPL-3.0-or-later License](LICENSE).
