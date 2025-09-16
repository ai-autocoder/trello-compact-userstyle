**Trello Compact Userstyle**

- **Goal:** Maximize usable space on Trello UI by trimming excess paddings/margins, repositioning the navbar and footer nav.
- **Why:** Trello's brand styling favors airy padding that looks calm but pushes content off-screen. This userstyle tightens headers, margins, and the card modal chrome so work stays visible, navigation stays close, and you scroll less.

**Features**

- **Top Navbar:** Repositions Trello's island/view navbar to the top center.
- **Compact Spacing:** Reduces paddings and margins across header, board, and card back.
- **Cleaner Modals:** Tightens card back layout and tucks the internal nav strip halfway into the card bottom so there is no wasted footer bar.
- **Safe Defaults:** Minimal visual changes, no functional behavior changes.

**Install**

- **With Stylus (Chrome/Firefox):**
  - Install the Stylus extension ([Chrome Web Store](https://chromewebstore.google.com/detail/clngdbkpkpeebahjckkjfobafhncgmne?utm_source=item-share-cb)).
  - Create a new style and paste the contents of `src/trello-compact.user.css`.
  - Save; ensure it's enabled for `trello.com`.

- **With "User JavaScript and CSS" (Chrome):**
  - Extension link: [Chrome Web Store](https://chromewebstore.google.com/detail/user-javascript-and-css/nbhcbdghjpllgmfilhnhkllmkecfmpld)
  - Add a new CSS rule for `https://trello.com/*` and paste `src/trello-compact.user.css`.

**What It Changes**

- **Navbar:** `#island-nav` becomes fixed at the top with a subtle translucent background.
- **Board:** Trims board and header padding; reduces empty space below the board.
- **Card Modal:** Shrinks outer margins, limits max height to viewport, repositions the internal nav bar halfway inside the card bottom, keeps cover area compact.

**Notes**

- If Trello updates their DOM, selectors may need slight adjustments. The current rules favor stability with explicit selectors.

**Development**

- Main stylesheet: `src/trello-compact.user.css`
- The CSS avoids nesting for maximum compatibility with userstyle managers.
- Feel free to open issues or propose tweaks (spacing, z-index, offsets) to suit different UI densities.