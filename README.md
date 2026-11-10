# SkillPilot Project - Multi-Step Sign-Up Page

A multi-step sign-up page built as part of my SkillPilots program. The form is split into three steps, and each step is a Flexbox-styled form section. The steps change with navigation buttons, and the page uses **no JavaScript**.

## Features

- Three separate form sections: User Info, Address, and Password
- Fields aligned with Flexbox (two fields per row on desktop, one per row on phones)
- The form itself is a Flexbox row, with each step taking the full width
- **Next** and **Back** navigation buttons that move between the steps without JavaScript
- Step indicator at the top that also jumps to a step and highlights the current one
- HTML5 validation with `required`, `pattern`, and input types (`email`, `tel`, `password`)
- Red border on invalid fields
- If an earlier step is incomplete, the browser takes the user back to the first empty field when submitting
- Responsive layout for desktop and mobile screens

## Task Steps

| Step | Where it is done |
|---|---|
| 1. Create separate form sections for user info, address, and password | Three `<section>` elements in `index.html`: `#step1`, `#step2`, and `#step3` |
| 2. Use Flexbox to align fields within each section | `.fields` and `.field` rules in `style.css` (`display: flex` and `flex-wrap: wrap`) |
| 3. Add navigation buttons to move between steps (no JavaScript required) | **Next** and **Back** links such as `href="#step2"`, and a **Create Account** submit button on the last step |

## The Three Steps

| Step | Fields |
|---|---|
| 1. User Info | First Name, Last Name, Email, Phone Number |
| 2. Address | Street Address, City, State, PIN Code, Country |
| 3. Password | Password, Terms and Conditions checkbox |

## How the Steps Work Without JavaScript

- The form is a Flexbox row (`display: flex; overflow: hidden`), and each step is one item that takes the full width (`flex: 0 0 100%`), so only one step is visible at a time.
- The **Next** and **Back** buttons are links to the ID of the next or previous step, for example `href="#step2"`. The browser scrolls the row to that step.
- All three steps stay in the same form, so a single **Create Account** button submits everything.

## Validation Rules

| Field | Rule |
|---|---|
| Names, Email, Address fields | Required. Email must be a valid email address |
| Phone Number | 10 digits, starting with 6, 7, 8 or 9 |
| PIN Code | 6 digits |
| Password | At least 8 characters, with letters and numbers |
| Terms and Conditions | Must be checked |

## Technologies Used

- HTML5
- CSS3 (Flexbox, `:target` and `:has()` selectors, media queries)

## How to Run

1. Download or clone this repository.
2. Keep `index.html` and `style.css` in the same folder.
3. Open `index.html` in any web browser.
4. Use **Next** and **Back** to move between the steps.

## Project Structure

```
multistep-signup/
├── index.html
├── style.css
└── README.md
```

