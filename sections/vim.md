# Vim

#### Insert text

- **i** - insert before the cursor;
- **I** - insert at the beginning of the line;
- **a** - insert after the cursor;
- **A** - insert at the end of the line;
- **o** - insert line below;
- **O** - insert line above;
- **:r [file]** - insert [file] below the cursor;
- **:r ![command]** - insert [command] output below the cursor;
- **u** - undo changes;
- **Ctrl-R** - redo changes;


#### Moving around

- **\*** - go to the next occurence of the word under the cursor;
- **#** - go to the previous occurence of the word under the cursor;
- **e** - go to the end of the word;
- **w** - go to next word;
- **b** - go to previous word;
- **$** - go to the end of the line;
- **0** - go to the beginning of the line;
- **%** - go to corresponding item ({ => }, ( => ));
- **f [character]** - go to the next occurence of the [character];
- **F [character]** - go to the previous occurence of the [character];
- **t [character]** - go to the next occurence of the [character], but one character before;
- **T [character]** - go to the previous occurence of the [character], but one character before;
- **;** - repeat previous f or t command;
- **m[character]** - mark cursor to [character];
- **'[character]** - go to the beginning of the file of mark [character];
- **`[character]** - go to the cursor positon of mark [character];
- **Ctrl-O** - go to the previous location;
- **Ctrl-I** - go to the next location;


#### Scrolling

- **Ctrl-E** - scroll lines downwards;
- **Ctrl-Y** - scroll lines upwards;
- **Ctrl-D** - scroll lines and cursor downwards following the 'scroll' option;
- **Ctrl-U** - scroll lines and cursor upwards following the 'scroll' option;
- **}** - go to the next paragraph;
- **{** - go to the previous paragraph;
- **)** - go to the next sentence;
- **(** - go to the previous sentence;
- **gg** - go to the beginning of the file;
- **G** - go to the end of the file;


#### Switching case

- **~** - toggle case;
- **g~iw** - toggle case of the current word;
- **g~~** - toggle case of the current line;
- **gUiw** - upper case current word;
- **guiw** - lower case current word;


#### Splitting windows

- **:split [file]** - horizontal split the [file];
- **:vsplit [file]** - vertical split the [file];
- **Ctrl-W, n | :new** - create new horizontal split;
- **:vnew** - create new vertical split;
- **Ctrl-W, S** - create horizontal split of the current window;
- **Ctrl-W, v** - create vertical split of the current window;
- **Ctrl-W, Q** - close window;
- **Ctrl-W, W** - change cycle through windows;
- **Ctrl-W, O** - show only the current window on the screen;
- **Ctrl-W, R** - rotate windows upwards/downwards;
- **Ctrl-W, h j k l** - move to window;
- **Ctrl-W, H J K L** - move window;
- **Ctrl-W, T** - move current window to a new tab; 


#### Buffers

- **:ls** - list buffers;
- **:bn** - go to next buffer;
- **:bp** - go to previous buffer;
- **:bd [buffer]** - remove a [buffer] and keep it in memory;
- **:bw [buffer]** - completely wipe out a [buffer];


#### Clipboard

- **gg"+yg** - copy the entire buffer;
- **"+y** - copy current line;
- **"+y** - copy selected text;
- **"+dd** - cut current line;
- **"+p"** - paste after the cursor;


#### Surroundings

- **ysiw]** - insert [] surronding the current word without space;
- **ysiw[** - insert [] surronding the current word with space;
- **ds[** - delete [] surronding the current word;
- **cs[)** - change [] surronding the current word to ();


#### Macros

- **q[character]** - start recording macro to be store on [character];
- **q[character]** - stop recording macro and store on [character];
- **@[character]** - run macro stored on [character];
- **:norm! @[character]** - run macro stored on [character] on all lines selected;
