# Tailwind CSS Deep-Dive

## Intro to Tailwind CSS

1. What is Tailwind CSS?

- Utility-first CSS framework
- Rapidly build custom designs
- Low-level framework (no pre-built components)
- Building blocks, full creative freedom
- Highly customizable

2. Advantages of Tailwind CSS

- Minimal custom CSS (if ever)
- Easy designes from the view files
- Better developer experience
- Mobile-first designs from the start
- A "polished" and "designed" look and feel

3. Tailwind CSS vs Bootstrap

- No pre-built components
  - Easier to achieve a custom look
- Looks messy vs. 1 class per element
- Easy to parse look from the code
- Highly customizable with config

4. Resources
- Official documentation
  - [https://tailwindcss.com](https://tailwindcss.com)
- PDF Companion Cheat Sheet

## Background Classes & Shades

5. Background Classes & Shades
-  This set of classes change the background color of an element using a scale of 100-900 for shades and a palette of over 90 shades.

```
.bg-*-{100-900} {}
black, white, gray, red, orange,
yellow, green
```

## Element Sizing & Tailwind's Numbering System

6. Element sizing with REM

- 1 rem = document base font
  - If base font is 16px, then 1rem = 16px
  - Deduce that 20px = 1.25rem
- No decimals in Tailwind's numbering system

7. Tailwind's Numbering System

- 1 rem = 4 in Tailwind (multiplied by 4)
  - If base font is 16px = 1 rem =  4 in Tailwind
  - Example, width of 16px in Tailwind
    - .w-4
  - 1.25 rem = 5 in Tailwind (20px)

8. Element sizing is achieved using the `w-` and `h-` classes.
- All of the numbers in Tailwind are based around the `rem` unit of measurement. `1 rem` is equal to the size of the base font of the document. As an example, if the base font size is 16px then `1 rem` is equal to 16px and we can deduce that `1.25 rem` is equal to `20px` . To help with these fractional numbers, Tailwind's numbered classes are multiplied by 4 to avoid having numbers with decimal places.

9. Tailwind's Numbering System
- Assuming the base font of the document is 16px
- | Pixels | rem | Tailwind |
  |:------:|:---:|:--------:|
  | 0px | 0 rem | 0 |
  | 4px | 0.25 rem | 1 |
  | 8px | 0.5 rem | 2 |
  | 12px | 0.75 rem | 3 |
  | 16px | 1 rem | 4 |
  | 20px | 1.25 rem | 5 |
  | 24px | 1.5 rem | 6 |
  | 32px | 2 rem | 8 |
  | 40px | 2.5 rem | 10 |
- Continues to all of the available default sizes 12, 16, 20, 24, 32, 40, 48, 56, 64

10. Sizing with `w-*` and `h-*` classes
```
.w-* {}
.h-* {}
Available sizes in REM
0, 1, 2, 3, 4, 5, 6, 8, 10, 12,
16, 20, 24, 32, 40, 48, 56, 64,
Sizing in percentages
1/2... 1/{3, 4, 5, 6, 12)
Sizing utilities
```

## Padding & Margin

11. Padding and margins with `p-*`, `m-*`, `py-*` and `my-*`
-  These classes add padding and margin to an element using the Tailwind numbering system.
```
.p-* {}
.m-* {}
.p{x, y}-* {}
.m{x, y}-* {}
.{p|m{l|r|t|b}}-{size}
.{p|m{x|y}}-{size}
```
## Styling Text - Font Family

12. Font Family
- `.font-{family}`
- Families
  - sans
  - serif
  - mono
- Apply to body

13. Text Size
- `.text-{size}`
- | Sizes | rem | Pixels |
  |:------:|:---:|:--------:|
  | xs | .75 rem | 12px |
  | sm | .875 rem | 14px |
  | base | 1 rem | 16px |
  | lg | 1.125 rem | 18px |
  | xl | 1.25 rem | 20px |
  | 2xl | 1.5 rem | 24px |
  | 3xl | 1.875 rem | 30px |
  | 4xl | 2.25 rem | 36px |
  | 5xl | 3 rem | 48px |
  | 6xl | 4 rem | 64px |

14. Text Alignment
- `.text-{align}`
  - left
  - center
  - right
  - justify

15. Text Color
- `.text-{color}-{shade}`
- apply to body as well

16. Text - Italics
- `.italic`
- `.not-italic`

17. Text - Font Weight
- `.font-{weight}`
  | Weights | Font Weight |
  |:------:|:--------:|
  | hairline | 100 |
  | thin | 200 |
  | light | 300 |
  | normal | 400 |
  | medium | 500 |
  | semibold | 600 |
  | bold | 700 |
  | extrabold | 800 |
  | black | 900 |

18. Text - Letter Spacing
- `.tracking-{spacing}`
- | Spacings | Font Weight |
  |:------:|:--------:|
  | tighter | -0.05em |
  | tight | -0.025em |
  | normal | 0 |
  | wide | 0.025em |
  | wider | 0.05em |
  | widest | 0.1em |
- __Note:__ Tracking is in __em__ units not in __rem__.
- __em__ units is base on the parent element's font size, not the document.

19. Text - Line height
- `.leading-{spacing}`
- | Spacings | Font Weight |
  |:------:|:--------:|
  | none | 1 |
  | tight | 1.25 |
  | snug | 1.375 |
  | normal | 1.5 |
  | relaxed | 1.625 |
  | loose | 2 |

20. Text Decorations
- `.underline`
- `.no-underline`
- `.line-through`

21. Text Transform
- `.uppercase`
- `.lowercase`
- `.capitalize`
- `.normal-case`

