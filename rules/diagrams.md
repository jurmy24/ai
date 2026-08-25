# Diagrams

Apply this when drawing or editing architecture diagrams for research writeups,
READMEs, and papers, especially for learning systems with encoders, world
models, policies, and planners.

## What goes in the image

- Put the heading and explanation in the surrounding document. Do not add a
  header or subheader inside the image.
- Show one concept or training phase per image. Split representation learning,
  world-model training, policy training, planning, and inference into separate
  images when combining them would make the flow harder to read.
- Show architecture and data flow only. Keep ablations, result tables, metrics,
  and long commentary in the prose next to the image.
- Keep labels short. Include a symbol, tensor shape, or parameter count only
  when it helps explain the interface, for example `z_t (256)` on an encoder
  output.

## Layout

- Make the main path read from left to right.
- Put target branches underneath the main path.
- Route feedback loops around the outside of the diagram.
- Arrows must not cross boxes, labels, or unrelated arrows. If an arrow has to
  cross something, the layout is wrong; move the box instead of bending the
  arrow.

## Visual language

- Off-white background, near-black text, muted secondary labels.
- One accent color per phase. A reader should be able to tell which phase an
  image belongs to from the accent alone.
- Lightly tinted rounded boxes and thin arrows.
- Dashed lines mean EMA updates, stop-gradient paths, or optional runtime paths.
  Do not use dashed lines for anything else.

## Shape carries meaning

Do not draw every component as the same generic box. Use:

| shape                         | meaning                                   |
| ----------------------------- | ----------------------------------------- |
| stacked frames                | image observations                        |
| stacked grids                 | latent feature maps                       |
| trapezium narrowing rightward | encoder (wide input, narrow latent)       |
| trapezium widening rightward  | decoder (narrow latent, wide output)      |
| rounded box                   | recurrent or predictive module            |
| circle                        | loss                                      |

Encoders narrow toward their latent output and decoders widen toward their
reconstructed output, so the direction of the taper alone tells the reader
which way data flows through it.

## Before finishing

- Render every diagram and inspect it at README width.
- If a label needs the surrounding paragraph to remain readable, remove it from
  the image and explain it in the prose.
- Check that each image answers "what connects to what" and nothing more. Move
  anything else into the text next to it.
