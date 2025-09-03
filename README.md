**Trello Compact Userstyle**

- **Goal:** Maximize usable space on Trello boards by trimming excess paddings/margins and moving the view navbar from the bottom to the top.
- **Why:** Laptop screens have limited vertical real estate; this makes Trello feel lighter and more focused.

**Features**

- **Top Navbar:** Repositions Trello’s island/view navbar to the top center.
- **Compact Spacing:** Reduces paddings and margins across header, board, and card back.
- **Cleaner Modals:** Tightens card back layout and hides the internal nav strip.
- **Safe Defaults:** Minimal visual changes, no functional behavior changes.

**Install**

- **With Stylus (Chrome/Firefox):**
  - Install the Stylus extension (Chrome: https://chromewebstore.google.com/detail/clngdbkpkpeebahjckkjfobafhncgmne?utm_source=item-share-cb).
  - Create a new style and paste the contents of `src/trello-compact.user.css`.
  - Save; ensure it’s enabled for `trello.com`.

- **With “User JavaScript and CSS” (Chrome):**
  - Extension link: https://chromewebstore.google.com/detail/user-javascript-and-css/nbhcbdghjpllgmfilhnhkllmkecfmpld
  - Add a new CSS rule for `https://trello.com/*` and paste `src/trello-compact.user.css`.

**What It Changes**

- **Navbar:** `#island-nav` becomes fixed at the top (`top: 33px`) with a subtle translucent background.
- **Board:** Trims board and header padding; reduces empty space below the board.
- **Card Back:** Shrinks outer margins, limits max height to viewport, hides the internal nav bar, keeps cover area compact.

**Notes**

- This userstyle targets only `trello.com` using the `@-moz-document` scope, so it won’t affect other sites.
- If Trello updates their DOM, selectors may need slight adjustments. The current rules favor stability with explicit selectors.

**Development**

- Main stylesheet: `src/trello-compact.user.css`
- The CSS avoids nesting for maximum compatibility with userstyle managers.
- Feel free to open issues or propose tweaks (spacing, z-index, offsets) to suit different UI densities.

**Roadmap Ideas**

- Optional density levels (compact / ultra-compact).
- A toggle for showing/hiding the card back’s internal nav.
- Theming touches (subtle borders/shadows) while keeping focus on space efficiency.
