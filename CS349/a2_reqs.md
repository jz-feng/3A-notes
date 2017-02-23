# CS349 A2 Requirements & Specs

(Will add/modify as I go along and as new info comes up from Piazza questions)

- each component (colour palette, canvas etc.) should be a separate View class

- menu bar
    - file menu
        - save & load to/from file
            - JFileChooser
            - save in text OR binary formats
            - create custom file extension, file chooser should only see this extension
        - create new
        - exit
        - remind to save before load, new & exit

- colour palette
    - colour selection
        - custom colour chooser (JColorChooser)
    - stroke thickness
    - new colour & thickness should not affect old strokes

- playback controls
    - playback bar
        - each stroke = 1 tick in the bar
        - scrubbing (drag back & forth)
        - should be able to scrub to the middle of a stroke
        - without enhancements:
            - each tick has the same size
            - each stroke takes the same duration to draw
            - each stroke is drawn out point-by-point (at constant speed) across the span of one tick
        - with enhancements:
            - each tick has size proportional to the time taken to draw it
            - each stroke is drawn out in the same amount of actual time to draw it
            - each stroke is still drawn out at constant speed
    - play button
        - draw stroke
    - start button
        - rewinds to beginning
        - may OR may not start playing automatically
    - end button
        - ff to end
    - can use icons (state in readme)
    - each stroke must be drawn point-by-point w.r.t. time
        - OPTIONAL: draw stroke as it was drawn in real-time

- drawing at a "frame" overwrites the frames (strokes) that followed
    - if drawing during the middle of a previous stroke:
        - "that stroke will truncated to just include points up to the new point where you start drawing (and the scrubber will update based on your new line length)"

- dynamic layout
    - "reasonable" minimum size, e.g. 400x300
    - no max size limit
    - canvas should be "fully accessible" regardless of size of window
    - image should **scale with the canvas**
    - left pane should expand & contract; all colours in the palette should be visible at all times
