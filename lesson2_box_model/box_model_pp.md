# Q1
- `img`, being `content-box`, will have its box sized as its `height` / `width` plus appropriate `margin`, `padding`, and `border`
- `height` = 300 + 10 + 10 + 20 + 10 + 4 + 4 = 358
- `width` = 500 + 19 + 11 + 20 + 20 + 4 + 4 = 578
- `div` is `border-box`, and so will have its contents resized to fit its `margin`, `padding`, and `border`
- to fit `img`, `div`'s `height` needs to be 360 (358 + 1 + 1) and its `width` needs to be 580 (578 + 1 + 1)


# Q2
- Same as Q1: 360 `height` and `580` width, the difference is that `section` here is `block` display and will always be on its own line, whereas `img` being `inline-block` means it may have other elements on the same line if they fit

# Q3
- cannot calculate because `inline` means browser will ignore `height` and `width`
- assuming content `width` of 50:
  - 50 for content
  - 20 + 20 for padding
  - 19 + 11 for margin
  - 4 + 4 for `em` border
  - 1 + 1 for `div` border
  - 130 total needed for `div`'s `width`
- assuming content `height` of 20:
  - 20 for content
  - 10 + 10 for padding
  - margin ignored
  - 4 + 4 for `em` borders
  - 1 + 1 for `div` borders
  - 50 total needed for `div`'s `height`

# Q4
- since `article` is `border-box`, that means its `width` and `height` properties are inclusive of its `border`, and `padding`
- `article`'s `width`will be 
  - 500 for content
  - 19 + 11 for margin
  - 530 total
- `article`'s `height` will be 
  - 300 for content
  - 20 + 10 for margin
  - 330
- since `div` is `border-box` as well, to fit its contents, its `width` and `height` will need to include the space need for `article` as well as the 1 px border, so:
  - `width`: 530 + 1 + 1 = 532
  - `height`: 330 + 1 + 1 = 332

# Q5
- `div` is `content-box` and so its entire `width` of 720 can be used to fit its contents (i.e. no need to reserve space for its 1px `border`)
- `tag1` and `tag2` are `border-box`, which means its actual width will be determined by its content width of 360
- `tag1` and `tag2` will show side-by-side in: 2, 3, 6
- all the other configurations have at least one of the elements being `block` which means it will show on a line by itself

# Q6
- no they won't because:
  1. they are both `block` elements by default, and will show up on their own lines
  2. default `box-sizing` is set to `content-box`, which means an `article` element's actual box size will be 22 pixels too large to fit into any container 
- to fit them side-by-side, add `box-sizing: border-box` to `article`, and also add `display: inline-block`

# Q7
- because they are `display:inline-block`, they will still appear on the same line