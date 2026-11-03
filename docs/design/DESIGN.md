# SwiftDrop Design System (v1.0)

Source of truth for all UI. Screen references: `docs/design/01 Login.png`, `02 Register.png`, `03 Dashboard shell.png`.
White surfaces, neutral greys, ONE orange accent for actions and active states, thin borders instead of shadows.
No gradients, no glass effects, no emoji, no decorative illustrations.

## 1. Colour tokens

### Accent (orange) - the only accent colour
| Token | Hex | Use |
|---|---|---|
| orange-50  | #FFF4EC | Active nav item fill |
| orange-100 | #FFE3CF | Focus ring on inputs (3px) |
| orange-500 | #FF6A00 | Brand: logo and large fills (auth side panel) ONLY - never text/buttons |
| orange-600 | #E55400 | Focus border, checked checkbox, selected states, active nav icon |
| orange-700 | #CC4A00 | Primary button fill, text links |
| orange-800 | #A33A00 | Primary button hover, active nav label |

Why: white text on #FF6A00 is only 2.9:1 contrast. Buttons use orange-700 (4.6:1).

### Neutrals (grey)
| Token | Hex | Use |
|---|---|---|
| white    | #FFFFFF | All page surfaces |
| grey-50  | #F7F8F9 | Hover, subtle fills, disabled input fill, segmented track |
| grey-100 | #EFF1F3 | Row dividers, disabled button fill |
| grey-200 | #E3E6EA | Default borders (cards, sidebar, top bar) |
| grey-300 | #CDD2D8 | Control borders (inputs, secondary buttons) |
| grey-400 | #A3AAB3 | Disabled text, unchecked |
| grey-500 | #6B737D | Placeholder, nav group labels |
| grey-600 | #59616B | Secondary text |
| grey-700 | #3F4650 | Icons, quiet labels, default nav label |
| grey-800 | #272C33 | Strong text on fills |
| grey-900 | #15181D | Primary text |

### Functional (validation and delivery outcomes only - never decorative)
| Token | Hex | Use |
|---|---|---|
| error        | #B42318 | Field errors, error border |
| error-tint   | #FEF3F2 | Error notice fill |
| success      | #157347 | Delivered |
| success-tint | #EEF8F2 | Delivered badge fill |

## 2. Typography
Font: **IBM Plex Sans** (Google Fonts), weights 400 / 500 / 600 only.
Tracking numbers, phone numbers, amounts: `font-variant-numeric: tabular-nums`.

| Style | Size / line-height / weight |
|---|---|
| Display   | 32 / 40 / 600 |
| Heading 1 | 24 / 32 / 600 |
| Heading 2 | 20 / 28 / 600 |
| Heading 3 | 16 / 24 / 600 |
| Body      | 16 / 24 / 400 |
| Body small| 14 / 20 / 400 |
| Label     | 14 / 20 / 500 |
| Caption   | 12 / 16 / 500 |
| Tabular   | 14 / 20 / 500, tabular-nums |

## 3. Spacing (8px grid, 4px half-step)
| Token | px | Use |
|---|---|---|
| space-0.5 | 4  | Icon to label, label to helper |
| space-1   | 8  | Between related items |
| space-2   | 16 | Control padding |
| space-3   | 24 | Between form fields |
| space-4   | 32 | Page padding, form groups |
| space-5   | 40 | Between heading and form |
| space-6   | 48 | Between sections |
| space-8   | 64 | Auth panel padding |
| space-10  | 80 | Large page margins |

## 4. Layout
- Sidebar: 248px, white, 1px right border (grey-200)
- Top bar: 64px, white, 1px bottom border (grey-200)
- Content: max 1200px, left-aligned
- Page padding: 32px desktop, 16px phone
- Form column: max 400px (auth), 640px (in app)
- Auth pages: split screen - form on white left half, solid orange-500 right panel with white logo. Right panel hidden on mobile.

## 5. Radius, borders, elevation
- Radius: sm 4px (badges, checkbox) · md 6px (buttons, inputs) · lg 8px (panels, menus)
- Borders: default 1px grey-200 · control 1px grey-300 · focus/selected 1px orange-600 · error 1px error
- Elevation: level 0 flat (all page surfaces) · level 1 `0 4px 16px rgba(21,24,29,0.08)` for menus, popovers, dialogs only

## 6. Buttons
- Large 48px (auth screens, page-level actions); default 40px (in app)
- Primary: orange-700 fill, white text; hover orange-800; focus 2px orange ring. One primary button per view.
- Secondary: white, 1px grey-300 border, grey-900 text; hover grey-50
- Tertiary: text only, grey-700
- Disabled: grey-100 fill, grey-400 text
- Icon button: 40px square, secondary style
- "Continue with Google": secondary style, full form width, official multicolour G at 20px, below primary button after an "or" divider
- Labels are verbs: "Create delivery", "Book pickup", "Log in"

## 7. Form fields
- Label above (Label style), helper/error below, 4px apart; 24px between fields
- Input height 48px (auth), 1px grey-300 border, md radius, placeholder grey-500
- Focus: orange-600 border + 3px orange-100 ring
- Error: error border + error icon + message saying how to fix ("Enter a full email address, like name@example.com")
- Disabled: grey-50 fill
- Phone input: "+94" prefix segment
- Select: native, chevron grey-600
- Password: show/hide eye icon

## 8. Selection controls
- Segmented switch (e.g. Customer / Merchant): track grey-50; selected item white with orange-600 border
- Checkbox: checked orange-600, sm radius

## 9. Navigation (sidebar)
- Items 40px tall, 20px stroke icon
- Active: orange-50 fill, orange-800 label weight 600, orange-600 icon
- Hover: grey-50 fill, grey-900 label
- Default: no fill, grey-700 label, grey-600 icon
- Group labels: 12px uppercase, grey-500, 24px above

## 10. Status and feedback
- Parcel status badge = dot + word (readable without colour). Orange is NEVER used for status.
  Pending pickup (hollow dot, white) · Picked up / In transit / Out for delivery (grey) · Delivered (success-tint) · Delivery failed (error-tint)
- Inline notice: grey-50 fill, info icon, bold title + body. Error notice: error-tint fill, error text.
- Empty state: icon in grey box, Heading 3 title, one-line explanation, one primary button.

## 11. Writing
Plain, specific wording about the task ("Track a parcel", "We couldn't log you in"). No marketing phrases.
Sri Lankan context: +94 phone numbers, Rs. amounts, district names.