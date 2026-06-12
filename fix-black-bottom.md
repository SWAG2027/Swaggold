# Fix: Black Bottom Area

## Problem
`body::after` has a 60vh dark gradient that darkens "Our Location" button and footer.

## Fix in index.html — Two changes:

### 1. Remove or reduce body::after (line ~30)
Change:
```css
body::after{content:'';position:fixed;bottom:0;left:0;right:0;height:60vh;
  background:linear-gradient(to bottom,transparent,#1a0f07 60%,#120b04 100%);
  z-index:0;pointer-events:none}
```
To (remove entirely OR reduce to subtle):
```css
body::after{content:'';position:fixed;bottom:0;left:0;right:0;height:20vh;
  background:linear-gradient(to bottom,transparent,rgba(26,15,7,0.3) 100%);
  z-index:0;pointer-events:none}
```

### 2. Reduce .scrim bottom opacity
Change `.30` to `.10` at bottom of scrim gradient.
