# CSS `calc()` and `min-content` Inconsistency

This repository demonstrates an uncommon CSS bug related to the interaction between `calc()`, percentages, and `min-content` for the `min-width` property.

## Description
The issue arises when using a `calc()` expression with percentages to set the width and simultaneously specifying `min-width: min-content`. In certain circumstances, the element might not shrink to its intrinsic content size (`min-content`), even if the calculated width exceeds this size. This behavior is inconsistent and can be hard to debug.

## Reproduction
The `bug.css` file contains the problematic CSS code. You can test the behavior by creating a simple HTML file with a `div` element and applying the provided CSS. Observe the element's width in different scenarios, varying the parent container's width and the content inside the `div`.

## Solution
The `bugSolution.css` file illustrates a potential workaround to address this inconsistency.  The solution may involve avoiding the direct combination of `calc()` with percentages and `min-content`, or employing alternative sizing techniques based on the specific layout requirements.