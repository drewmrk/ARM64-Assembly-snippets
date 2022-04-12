# ARM64 Assembly snippets

## About

This is a VERY opinioniated snippets extension; it was mainly made for myself to maintain a consistent comment style while taking CSE 320 at Michigan State University, but perhaps other people would also benefit from these snippets.

## Prerequisites

This extension requires that either Dan Underwood's [Arm Assembly](https://marketplace.visualstudio.com/items?itemName=dan-c-underwood.arm), or maziac's [ASM Code Lens](https://marketplace.visualstudio.com/items?itemName=maziac.asm-code-lens), is installed in order for these snippets to work.

## Snippets

More snippets will be added soon, for the current snippets available, see below.

### Section

Prefix: `text`

```asm
//
// Text
//
.text

.global main
```

Prefix: `data`

```asm
//
// Data
//
.data
```

### Mode

Prefix: `thumb`

```asm
//
// Thumb
//
.thumb
```

### Standard

|  Prefix   |                                     Code                                      |
| :-------: | :---------------------------------------------------------------------------: |
|   `stp`   |        `stp x19, x20, [sp, #-16]! // Push x29 and x30 onto the stack`         |
|   `ldp`   |        `ldp x29, x30, [sp], #16 // Restore x29 and x30 from the stack`        |
|  `alias`  |                      `var .req x0 // Alias x0 as "var"`                       |
|   `mov`   |                        `mov x0, x1 // Copy x1 into x0`                        |
|  `fmov`   |                       `fmov d0, d1 // Copy d1 into d0`                        |
|   `mul`   |       `mul x0, x1, x2 // Multiply x1 by x2 and store the result in x0`        |
|  `fmul`   |       `fmul d0, d1, d2 // Multiply d1 by d2 and store the result in d0`       |
|   `lsl`   | `lsl x0, x1, x2 // Logically shift x1 left by x2 and store the result in x0`  |
|   `lsr`   | `lsr x0, x1, x2 // Logically shift x1 right by x2 and store the result in x0` |
|   `add`   |          `add x0, x1, x2 // Add x2 to x1 and store the result in x0`          |
|  `fadd`   |         `fadd d0, d1, d2 // Add d2 to d1 and store the result in d0`          |
|   `sub`   |      `sub x0, x1, x2 // Subtract x2 from x1 and store the result in x0`       |
|  `fsub`   |      `fsub d0, d1, d2 // Subtract d2 from d1 and store the result in d0`      |
|   `cmp`   |                     `cmp x0, x1 // Compare x0 against x1`                     |
|  `fcmp`   |                    `fcmp d0, d1 // Compare d0 against d1`                     |
|   `ret`   |                                `ret // Return`                                |
| `release` |                          `.unreq var // Release var`                          |
|   `bl`    |                            `bl free // Call free`                             |
|   `beq`   |                           `beq next // If x0 == x1`                           |
|   `ble`   |                           `ble next // If x0 <= x1`                           |
|   `blt`   |                           `blt next // If x0 < x1`                            |
|   `bge`   |                           `bge next // If x0 >= x1`                           |
|   `bgt`   |                           `bgt next // If x0 > x1`                            |
|   `bne`   |                           `bne next // If x0 != x1`                           |
|   `ldr`   |                  `ldr x0, [x1] // Load data from x1 into x0`                  |
|   `str`   |                 `str x1, [x0] // Store data from x1 into x0`                  |
|  `local`  |                   `.equ local, 8 // Local "local" variable`                   |
