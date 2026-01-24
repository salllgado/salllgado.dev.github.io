# Quick Mobile Testing Guide

## How to Test Your Mobile Responsive Design

### Using Browser DevTools (Chrome/Firefox/Edge)

1. Open your website in browser
2. Press `F12` to open Developer Tools
3. Click the **device toggle icon** (phone/tablet icon) in top-left
4. Select different devices from dropdown menu
5. Rotate device to test landscape orientation

### Quick Device Sizes to Test

| Device | Width | What to Check |
|--------|-------|--------------|
| iPhone 12/13 | 390px | Is text readable? Do buttons fit? |
| Samsung S21 | 360px | Are images scaled? Is nav accessible? |
| iPad | 768px | Do tabs look good? Proper spacing? |
| iPad Pro | 1024px | Tablets should show wider layout |

### Key Areas to Test

#### Header/Hero Section
- ✅ Profile image scales properly
- ✅ Name and title are readable
- ✅ Social icons display correctly
- ✅ Navigation is accessible

#### Career Section (Tabs)
- ✅ Tab buttons are clickable/tappable
- ✅ Content displays below tabs on mobile
- ✅ Text is fully visible

#### Portfolio Section (Apps)
- ✅ App buttons wrap nicely
- ✅ Content scrolls smoothly
- ✅ Download buttons are large enough to tap

#### Overall
- ✅ No horizontal scrolling needed
- ✅ Text is readable (not too small)
- ✅ Touch targets are ≥44px (accessibility standard)

## CSS Classes Used

Your responsive design uses these Bootstrap classes:
- `col-12` = full width on mobile
- `col-md-*` = specific width on tablets+
- `col-lg-*` = specific width on desktops
- `px-3 px-md-0` = padding on mobile, none on desktop
- `container-fluid` = full width container

## Media Queries Added

```css
/* Tablets and down */
@media (max-width: 768px) { ... }

/* Mobile phones */
@media (max-width: 480px) { ... }

/* Very small devices */
@media (max-width: 320px) { ... }

/* Large screens */
@media (min-width: 992px) { ... }
```

## Common Issues & Fixes

**Issue**: Text too small on mobile
**Status**: ✅ Fixed - Font sizes scale down appropriately

**Issue**: Buttons not clickable
**Status**: ✅ Fixed - All buttons now ≥44px touch target

**Issue**: Layout breaks on small screens
**Status**: ✅ Fixed - Columns now stack vertically

**Issue**: Images overflow container
**Status**: ✅ Fixed - Images now max-width: 100%

---

**Need Help?** Open your browser console (F12) to check for any JavaScript errors.
