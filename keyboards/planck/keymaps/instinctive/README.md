# Planck MTGAP layout

This is a variant [MTGAP](https://mathematicalmulticore.wordpress.com/) layout
for the Planck 4x12 ortho keyboard, restructured as a 2x(3x5+2) split layout.
That is, each hand has 3x5 keys for the fingers and two for the thumbs.

The layout has 4 layers, controlled by `LA1` and `LA2` keys, which when held
switch to layers ONE and TWO, respectively, and layer THREE when both are held.

Layer ZERO (default layer):

    y   p   o   u   j   _   _   k   d   l   c   w
    i   n   e   a   ,   _   _   m   h   t   s   r
    q   z   '   .   ;   _   _   b   f   g   v   x
    _   _   _   LA2 SFT _   _   SPC LA1 _   _   _

Layer ONE (`LA1` key is held):

    1   2   3   4   5   _   _   6   7   8   9   0
    ESC `   =   -   (   _   _   )   CMD ALT CTL SFT
    <   *   $   >   [   _   _   ]   .   ,   _   _
    _   _   _   LA2 TAB _   _   SPC XXX _   _   _

Layer TWO (`LA2` key is held):

    1   2   3   4   5   _   _   6   7   8   9   0
    SFT CTL ALT CMD (   _   _   )   -   /   \   ENT
    _   _   ,   .   [   _   _   ]   _   _   _   _
    _   _   _   XXX SFT _   _   BSP LA1 _   _   _

Layer THREE (`LA1` and `LA2` are both held):

    FN1 FN2 FN3 FN4 FN5 _   _  FN6 FN7 FN8 FN9 FN0
    HOM PGD PGU END DEL _   _  BSP LFT DWN UP  RGT
    _   _   _   _   _   _   _  _   _   _   _   _
    _   _   _   XXX SFT _   _  SPC XXX _   _   _

## Building

    $ qmk config user.keyboard=planck/rev6_drop
    $ qmk config user.keymap=instinctive
    $ qmk compile
    $ cd /path/to/qmk_firmware/.build
    $ qmk flash planck_rev6_drop_instinctive.bin

## Credits

The one-shot modifiers are taken directly from [users/callum](
https://github.com/qmk/qmk_firmware/tree/999008f0eb8204f2d6d99113ae45aad2337dcf28/users/callum).
