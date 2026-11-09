# InvestWood Capital Website

This is the website for InvestWood Capital, LLC (investwood.com). It is a simple one-page brochure site: three content sections (What We Do, Overview, Major Projects), with the contact email in the footer. It uses plain HTML and CSS only. There is no framework, no build step, and nothing to install. Every file can be opened and edited in Notepad.

This README is written for a non-developer. If you can edit a Word document, you can edit this site.

## What is in this repository

| File or folder | What it does |
| --- | --- |
| `index.html` | The page itself. All of the words on the site live here, along with the page title, the page description, the Aggie 100 link, and the footer with the contact email. |
| `style.css` | How the page looks: colors, fonts, spacing, and how it adapts to phones and tablets. No words from the site are in this file. |
| `images/` | Image files used on the page (currently the company logo, `logo.gif`). |
| `README.md` | This file. |

## How changes go live

1. The `main` branch is the live site. Whatever is on `main` is published automatically at https://investwood-site.pages.dev (and later at investwood.com).
2. `main` is protected. Nothing reaches it without a pull request that has been approved and merged by the site owner.
3. Every other branch gets its own private preview address in the form `https://BRANCH-NAME.investwood-site.pages.dev`. Open that address to check your work before it goes live. A pull request also shows the preview link.
4. Branch names are lowercase with hyphens and no spaces, for example `fix-footer` or `update-projects`.

The safe routine for any change: make a new branch, edit the file, check the preview address, open a pull request, get it approved, merge, then delete the branch.

## How to change a line of text

You can do this entirely on the GitHub website.

1. On GitHub, switch to a new branch (use the branch menu at the top left of the file list, type a new name, and choose "Create branch").
2. Click `index.html`, then click the pencil icon ("Edit this file").
3. Use your browser's find (Ctrl+F) to locate the sentence you want to change. Search for a few distinctive words from it.
4. Change only the words. Leave the angle brackets and tags around the text alone. For example, in `<p>We excel at underwriting...</p>` edit the words between `<p>` and `</p>`.
5. Click "Commit changes", write a short plain message such as "Update Overview paragraph", and keep the option to commit to your branch.
6. Open the branch's preview address and confirm the change looks right, on a phone-sized window too.
7. Open a pull request into `main`, paste the preview address, and ask for approval.

Approved wording should not be changed without the site owner's sign-off.

## How to add a project to Major Projects

Each project is one item in a bulleted list in `index.html`. Find the heading "Major Projects" and look just below it for a list that looks like this:

```html
<ul>
  <li>First project text.</li>
  <li>Second project text.</li>
</ul>
```

To add a project, copy one whole `<li>` line (from `<li>` to `</li>`), paste it where you want it in the list, and replace the words. Keep it on its own line, between other `<li>` lines and before the closing `</ul>`. New items pick up the same styling automatically.

To remove a project, delete its whole `<li>...</li>` line. To reorder, cut and paste a line to a new position.

## Special characters and writing rules

Please keep these rules when editing. They apply to all text on the site, including labels and image descriptions.

- **No em dashes** anywhere. Use a comma, a period, or a plain hyphen.
- Use curly quotes and apostrophes in visible text (“ ” ’), not straight ones (" '). Straight quotes are only for the code itself, such as `href="..."`.
- The company name is written **InvestWood Capital** with a capital W. The legal name in the footer and contact section is **InvestWood Capital, LLC**.
- Do not add other branding, logos, links, or company names to the site.
- Do not add analytics or tracking scripts.
- Do not add a street address, phone number, or fax number unless the site owner supplies confirmed current ones.

## The Aggie 100 link

In the Overview section, the words "Aggie 100" link to InvestWood's honoree page at Texas A&M's McFerrin Center for Entrepreneurship: `https://aggie100.com/honoree/investwood-capital/`. The link opens in a new tab. Do not link anywhere else and do not host a copy of the page. If the address ever stops working, tell the site owner rather than guessing a new one.

## Page title and description

Near the top of `index.html`, inside the `<head>` section, are two settings that control how the site appears in browser tabs and search results:

- The `<title>` line: InvestWood Capital - Commercial Real Estate Due Diligence Services
- The `<meta name="description" ...>` line: InvestWood Capital focuses on due diligence consulting services for commercial real estate.

## The footer year

The footer reads "© [year] InvestWood Capital, LLC". A small script at the bottom of `index.html` fills in the current year automatically, so it does not need yearly editing. If a visitor has scripts turned off, the year typed into the page is shown instead.

## Contact details

Contact is handled in the footer. There is no contact form. The footer has a line that begins "Contact:" followed by an email link for jim@investwood.com. Clicking it opens the visitor’s email program.

To change the contact email, edit the footer line in `index.html` (search for "Contact:"). An email link has the address in two places, the part after `mailto:` and the visible words, and both must be changed together. Contact details should only be changed with the site owner’s sign-off. Do not add a street address, phone number, or fax number unless the site owner supplies confirmed current ones.

## Colors

The site uses the official Texas A&M University palette, taken from the Texas A&M brand guide (brandguide.tamu.edu). Aggie Maroon is the accent and heading color. It is not used as a full-page background. Body text is dark gray on white. No other colors are used.

| Name | Hex value | Used for |
| --- | --- | --- |
| Aggie Maroon | `#500000` | Headings, links, accent lines, borders, focus outlines |
| Maroon, dark accent | `#3C0000` | Hover states (use sparingly) |
| Maroon, light accent | `#732F2F` | Occasional accent (use sparingly) |
| White | `#FFFFFF` | Page background |
| Light gray | `#F6F6F6` | Light background bands |
| Gray 300 | `#D1D1D1` | Thin lines and dividers |
| Gray 500 | `#707070` | Borders only, if needed (not for text) |
| Gray 700 | `#3E3E3E` | Secondary text |
| Gray 900 | `#202020` | Body text |

All of these are defined once at the top of `style.css`. To change a color everywhere, change its value there. Text colors must keep passing WCAG AA contrast (body text 4.5 to 1 or better).

## Fonts

Fonts come from Google Fonts, the only third-party service the page loads. They are Texas A&M brand fonts:

- **Oswald** for headings and navigation (shown in capital letters by the stylesheet).
- **Open Sans** for body text.

If Google Fonts is unavailable, the page falls back to Arial or a similar system font and remains readable.

## Images

Only use images supplied by the site owner. Do not use stock photos, AI-generated images, or images copied from the web. Every image needs a short description (the `alt` text) that follows the writing rules above. Do not stretch small images; if an image is too small to look sharp, ask for a larger version.

## Before any change goes live

- Only the approved sections and copy are on the page.
- The "Aggie 100" link works and opens in a new tab.
- The contact line in the footer shows jim@investwood.com and the link works.
- The page looks right on a phone, a tablet, and a desktop (check the Major Projects list at narrow widths especially).
- No em dashes and no other company's branding anywhere.
- No passwords, keys, or secrets anywhere in the repository.
- Page title and description are set as above.
- Every image has alt text.
- No red errors in the browser console (right-click the page, choose Inspect, then Console).

## Things that are handled separately

- **The domain (investwood.com):** DNS and the switch to this site are managed by the site owner, not through this repository.
- **The hosting account:** managed by the site owner. Preview and live addresses are the only part of the hosting you need to use.
