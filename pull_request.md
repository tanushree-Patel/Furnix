# [PR] Fix: Center align "Add to Cart" button on hover and active states

## Description
This pull request fixes the alignment issue where the "Add to Cart" button shifts to the side of the product card when hovered or clicked (active state).

## Related Issue
Closes # (issue described in [issue.md](file:///d:/open-Source/Furnix/issue.md))

## Proposed Changes
We override the hover and active states specifically for buttons inside `.product-image` to preserve the `translateX(-50%)` centering transform along with the `scale` animations.

### Files Modified:
1. **[style.css](file:///d:/open-Source/Furnix/style.css)** (around line 676)
2. **[Furnix-main/style.css](file:///d:/open-Source/Furnix/Furnix-main/style.css)** (around line 600)

### Code Diff:
```css
.product-image .btn:hover {
  transform: translateX(-50%) scale(1.1);
}

.product-image .btn:active {
  transform: translateX(-50%) scale(0.97);
}
```

## Checklist
- [x] Verified centering behavior on hover and active states.
- [x] Applied updates to both main and duplicate stylesheet files.
- [x] Code style guidelines followed.
