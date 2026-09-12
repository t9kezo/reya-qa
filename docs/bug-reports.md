# Bug Reports — REYA (Part 1: BUG-001 to BUG-055)

> Product: REYA (women-only ride booking platform) • Tested by: Abhishek Kanwar
> Environment (unless noted): Web — Chrome 120, Windows 11; Android 14; iOS 17 • Status legend: Open

---

## BUG-001: Heading/Subheading boxes have no character limit

| Module | Severity | Priority |
| --- | --- | --- |
| Header Content Page | Minor | Medium |

**Steps**
1. Open a Header Content page editor. 2. Type beyond any reasonable length into Heading / Subheading.
**Expected:** A character limit is enforced per spec.
**Actual:** Users can type unlimited text.

---

## BUG-002: Heading/Subheading accept whitespace-only input

| Module | Severity | Priority |
| --- | --- | --- |
| Header Content Page | Minor | Medium |

**Steps**
1. Open Header Content. 2. Fill Heading/Subheading with empty spaces only.
**Expected:** Empty/whitespace input rejected.
**Actual:** Fields accept standalone spacebar entries.

---

## BUG-003: Banner Image accepts invalid file formats

| Module | Severity | Priority |
| --- | --- | --- |
| Header Content Page | Major | High |

**Steps**
1. Open Header Content. 2. Upload a non-image file (e.g. PDF/DOC) into Banner Image.
**Expected:** Only image formats accepted.
**Actual:** Invalid formats are accepted.

---

## BUG-004: No error when updating section with whitespace-only headings

| Module | Severity | Priority |
| --- | --- | --- |
| Header Content Page | Major | High |

**Steps**
1. Fill Heading/Subheading with spaces only. 2. Click "Update Section".
**Expected:** Validation error is shown.
**Actual:** No error message is thrown at all.

---

## BUG-005: Banner Image upload has no file-size limit

| Module | Severity | Priority |
| --- | --- | --- |
| Header Content Page | Major | High |

**Steps**
1. Upload an oversized image into Banner Image.
**Expected:** Oversized file rejected with a size-limit message.
**Actual:** No maximum size rule exists; oversized files are accepted.

---

## BUG-006: Save confirmation alert shows static placeholder text

| Module | Severity | Priority |
| --- | --- | --- |
| Header Content Page | Minor | Low |

**Steps**
1. Change a section and save. 2. Read the confirmation alert.
**Expected:** Real, dynamic confirmation of the change.
**Actual:** Static placeholder text is displayed instead.

---

## BUG-007: No hint text for allowed banner image formats

| Module | Severity | Priority |
| --- | --- | --- |
| Header Content Page | Minor | Low |

**Steps**
1. Open the banner upload area.
**Expected:** Hint text lists allowed file extensions.
**Actual:** No hint text is shown.

---

## BUG-008: Cannot re-upload a banner image after deleting it

| Module | Severity | Priority |
| --- | --- | --- |
| Header Content Page | Major | High |

**Steps**
1. Upload a banner image. 2. Delete it using the "X" button. 3. Try to upload the same image file again.
**Expected:** The same file can be re-uploaded.
**Actual:** Re-uploading the same image is blocked.

---

## BUG-009: Title field does not reset after section update

| Module | Severity | Priority |
| --- | --- | --- |
| Header Content Page | Minor | Low |

**Steps**
1. Fill the title text field. 2. Update the section successfully.
**Expected:** Field resets to its default placeholder state.
**Actual:** Field retains the stale value instead of clearing.

---

## BUG-010: Same imagery/text can be duplicated across page tabs

| Module | Severity | Priority |
| --- | --- | --- |
| Header Content Page | Minor | Medium |

**Steps**
1. Open Home, About, Investors tabs. 2. Save identical imagery and duplicate text across them.
**Expected:** Duplication is prevented or flagged.
**Actual:** Multiple tabs allow identical content to be saved across all pages.

---

## BUG-011: "Why REYA" dropdown is open by default

| Module | Severity | Priority |
| --- | --- | --- |
| Homepage Management | Minor | Low |

**Steps**
1. Load the homepage.
**Expected:** The card is collapsed like the others.
**Actual:** "Why REYA" dropdown card stays wide open on load.

---

## BUG-012: Deleted social impact card remains on the live site

| Module | Severity | Priority |
| --- | --- | --- |
| Loyalty (Social Impact) | **Critical** | High |

**Steps**
1. As admin, delete a saved social impact card. 2. Check the live site.
**Expected:** The card is removed from the live site.
**Actual:** The item remains stuck on the live site.

---

## BUG-013: "Loyalty Content" menu highlights the page header

| Module | Severity | Priority |
| --- | --- | --- |
| Loyalty (Navigations) | Minor | Low |

**Steps**
1. Click the "Loyalty Content" menu item.
**Expected:** Only the loyalty menu reflects the selection.
**Actual:** The main page header highlights itself unexpectedly.

---

## BUG-014: Custom graph axis labels not displayed on public chart

| Module | Severity | Priority |
| --- | --- | --- |
| Investor (ROI Graph) | Major | High |

**Steps**
1. Set custom X-Axis / Y-Axis labels. 2. View the public website chart.
**Expected:** Labels appear on the chart.
**Actual:** Custom labels are never rendered.

---

## BUG-015: Long card text overlaps and breaks adjacent UI

| Module | Severity | Priority |
| --- | --- | --- |
| Investor Journey | Major | High |

**Steps**
1. Type text up to the character limit on the card.
**Expected:** Layout wraps cleanly.
**Actual:** Text overlaps and breaks adjacent UI blocks.

---

## BUG-016: About safety-icon text overflows its borders

| Module | Severity | Priority |
| --- | --- | --- |
| About (Promise Section) | Minor | Medium |

**Steps**
1. View the descriptive strings under the safety icons.
**Expected:** Text fits within design borders.
**Actual:** Text overflows outside the borders and clips unreadably.

---

## BUG-017: GIF rejected with misleading IMG/SVG error

| Module | Severity | Priority |
| --- | --- | --- |
| Founder Section | Minor | Medium |

**Steps**
1. In the file uploader, upload a GIF.
**Expected:** GIF either accepted or rejected with the correct reason.
**Actual:** GIF accepted, but an error claims only IMG and SVG are allowed.

---

## BUG-018: No item limit for security line items

| Module | Severity | Priority |
| --- | --- | --- |
| Investor (Disclaimers) | Minor | Medium |

**Steps**
1. Add security line items to the layout.
**Expected:** An item limit or counter exists.
**Actual:** Infinite items can be added with no counter.

---

## BUG-019: "Join the Waitlist" button dead / random behavior

| Module | Severity | Priority |
| --- | --- | --- |
| Home | **Critical** | High |

**Steps**
1. On homepage, click "Join the Waitlist" in the Hero section (repeat several times).
**Expected:** Waitlist action works consistently.
**Actual:** Button is completely dead or works only randomly.

---

## BUG-020: Registration crashes with "investor creation failed"

| Module | Severity | Priority |
| --- | --- | --- |
| Home | **Critical** | High |

**Steps**
1. Attempt to register on click.
**Expected:** Registration succeeds.
**Actual:** System crashes and throws an "investor creation failed" console exception.

---

## BUG-021: Onboarding data not recorded to the backend

| Module | Severity | Priority |
| --- | --- | --- |
| Home | **Critical** | High |

**Steps**
1. Submit onboarding forms on Investor, Loyalty, or Messages tabs.
**Expected:** Data is stored in the database.
**Actual:** Nothing is recorded into the database sheet on the backend.

---

## BUG-022: Completed rider signup redirects to login modal

| Module | Severity | Priority |
| --- | --- | --- |
| Investors | Major | High |

**Steps**
1. Complete rider signup. 2. Click "Got It".
**Expected:** Redirect to a successful dashboard state.
**Actual:** Redirects back home to a login modal.

---

## BUG-023: "Invest in Reya" button routes to wrong URL

| Module | Severity | Priority |
| --- | --- | --- |
| Investors | Major | High |

**Steps**
1. On the welcome banner, click "Invest in Reya".
**Expected:** Correct investment page.
**Actual:** Routes to a completely wrong page URL.

---

## BUG-024: Profile photo accepts PDFs and videos

| Module | Severity | Priority |
| --- | --- | --- |
| Investors | Major | High |

**Steps**
1. Try uploading a PDF or video to the profile photo zone.
**Expected:** Only images accepted.
**Actual:** Documents/videos are accepted.

---

## BUG-025: Password and phone boxes accept spaces only

| Module | Severity | Priority |
| --- | --- | --- |
| Investors | Minor | Medium |

**Steps**
1. Enter standalone spaces into Password and Phone fields.
**Expected:** Whitespace-only entries blocked.
**Actual:** They are accepted as valid entries.

---

## BUG-026: Onboarding forms lack format validation

| Module | Severity | Priority |
| --- | --- | --- |
| Investors | Major | High |

**Steps**
1. Fill Rider/Driver onboarding forms with invalid Name/Phone/Email formats.
**Expected:** Format validation errors shown.
**Actual:** No validation whatsoever on these fields.

---

## BUG-027: Mandatory Investment Amount can be left empty

| Module | Severity | Priority |
| --- | --- | --- |
| Investors | **Critical** | High |

**Steps**
1. Submit the form while leaving Investment Amount empty.
**Expected:** Mandatory-field error blocks submission.
**Actual:** Empty investment amount is accepted.

---

## BUG-028: Red validation errors remain after valid selection

| Module | Severity | Priority |
| --- | --- | --- |
| Investors | Minor | Medium |

**Steps**
1. Trigger validation error on Investment Tier. 2. Successfully select a tier.
**Expected:** Errors clear.
**Actual:** Red errors stay stuck on screen.

---

## BUG-029: Page slide-in transition animations broken

| Module | Severity | Priority |
| --- | --- | --- |
| Loyalty | Minor | Low |

**Steps**
1. Navigate across Loyalty layout tiles.
**Expected:** Smooth slide-in transitions.
**Actual:** Animations broken or missing across several tiles.

---

## BUG-030: Overlapping reveal eye icons on password fields

| Module | Severity | Priority |
| --- | --- | --- |
| Loyalty | Minor | Low |

**Steps**
1. Open Create/Confirm Password fields.
**Expected:** One reveal icon per field.
**Actual:** Two overlapping eye icons render.

---

## BUG-031: Driver Name field ignores its 30-char limit notice

| Module | Severity | Priority |
| --- | --- | --- |
| Loyalty | Major | High |

**Steps**
1. Type more than 30 characters into Driver Name (label claims max 30).
**Expected:** Input truncated/rejected.
**Actual:** Long text is accepted past the stated limit.

---

## BUG-032: PDF document upload shows no thumbnail preview

| Module | Severity | Priority |
| --- | --- | --- |
| Loyalty | Minor | Medium |

**Steps**
1. Upload identification as a PDF file.
**Expected:** A visual preview/thumbnail is generated.
**Actual:** Thumbnail container is blank.

---

## BUG-033: Tapping Terms text checks the wrong checkbox

| Module | Severity | Priority |
| --- | --- | --- |
| Loyalty | Major | High |

**Steps**
1. In Driver registration, tap the "Terms of Service" label.
**Expected:** The matching Terms checkbox is checked.
**Actual:** The checkbox for the prompt **above** it gets checked instead.

---

## BUG-034: Generic toast instead of inline error under the input

| Module | Severity | Priority |
| --- | --- | --- |
| Loyalty | Minor | Medium |

**Steps**
1. Submit Rider form with no Full Name.
**Expected:** Inline red error directly under the input.
**Actual:** Generic "Full Name required" toast only.

---

## BUG-035: Driver registration has no error validation alerts

| Module | Severity | Priority |
| --- | --- | --- |
| Loyalty | Major | High |

**Steps**
1. Submit the Driver form with empty/invalid inputs.
**Expected:** Validation alerts on every field.
**Actual:** No validation errors are shown.

---

## BUG-036: "I confirm..." text checks the wrong checkbox

| Module | Severity | Priority |
| --- | --- | --- |
| Loyalty | Major | High |

**Steps**
1. Click the "I confirm I have read terms..." text.
**Expected:** The corresponding agreement box is checked.
**Actual:** The wrong agreement checkbox (above it) is checked.

---

## BUG-037: Inquiry selection doesn't clear the "Field Required" error

| Module | Severity | Priority |
| --- | --- | --- |
| Connect Section | Minor | Medium |

**Steps**
1. Trigger "Field Required" error. 2. Select an item from "Select Your Inquiry".
**Expected:** Error clears.
**Actual:** Error label stays active.

---

## BUG-038: Forms fail to push data to the backend storage

| Module | Severity | Priority |
| --- | --- | --- |
| Multiple Modules | **Critical** | High |

**Steps**
1. Submit valid forms on Investor, Loyalty, or Contact portals.
**Expected:** Data rows written to the backend storage sheet.
**Actual:** No data reaches the backend at all.

---

## BUG-039: Profile photo upload has no validation enforcement

| Module | Severity | Priority |
| --- | --- | --- |
| Investors | Minor | Medium |

**Steps**
1. Click the Profile Photo upload button without a file / with any file.
**Expected:** Type checks / validation enforced.
**Actual:** Users can click past it with no validation or file-type check.

---

## BUG-040: Investment Amount field can be bypassed

| Module | Severity | Priority |
| --- | --- | --- |
| Investors | **Critical** | High |

**Steps**
1. Submit the form while skipping the Investment Amount field.
**Expected:** Locked as required.
**Actual:** Field is bypassed and form proceeds.

---

## BUG-041: Registration attempts fail globally

| Module | Severity | Priority |
| --- | --- | --- |
| Investors | **Critical** | High |

**Steps**
1. Attempt any user registration.
**Expected:** Registration succeeds.
**Actual:** All attempts fail, flashing an "investor creation failed" red toast.

---

## BUG-042: Empty phone validation fires instantly on Rider form

| Module | Severity | Priority |
| --- | --- | --- |
| Investors | Minor | Low |

**Steps**
1. Navigate to the Rider form.
**Expected:** Validation triggers only after user input/submission.
**Actual:** Empty-phone alert fires immediately, before typing.

---

## BUG-043: Auto-navigation dashboard helper missing

| Module | Severity | Priority |
| --- | --- | --- |
| Home Screen | Minor | Low |

**Steps**
1. View the live home screen.
**Expected:** Quick auto-navigation dashboard helper visible.
**Actual:** Helper is completely missing.

---

## BUG-044: Ride dispatch ETA frozen at "0 min pickup"

| Module | Severity | Priority |
| --- | --- | --- |
| Ride Requests | Major | High |

**Steps**
1. Dispatch a ride request to an available driver.
**Expected:** ETA counter updates in real time.
**Actual:** ETA stays frozen at "0 min pickup".

---

## BUG-045: Dark Mode hides complaint category text

| Module | Severity | Priority |
| --- | --- | --- |
| Report An Issue | Major | High |

**Steps**
1. Open the support complaint screen in Dark Mode.
**Expected:** Text remains visible.
**Actual:** Category selection text is invisible against the dark background.

---

## BUG-046: Unneeded "Pay Now" button rendered

| Module | Severity | Priority |
| --- | --- | --- |
| Payment Screen | Minor | Low |

**Steps**
1. Open the payment screen with no active balances/fees.
**Expected:** No checkout button when nothing is owed.
**Actual:** A "Pay Now" button renders unnecessarily.

---

## BUG-047: Incoming message toast doesn't open the chat

| Module | Severity | Priority |
| --- | --- | --- |
| Driver App | Major | High |

**Steps**
1. Receive a message while another screen is open. 2. Tap the toast notification.
**Expected:** Opens the conversation / chat screen.
**Actual:** Nothing happens.

---

## BUG-048: "Driver arrived" notification lacks spacing

| Module | Severity | Priority |
| --- | --- | --- |
| Driver Arrival | Minor | Low |

**Steps**
1. Trigger the "Driver arrived to your location" notification.
**Expected:** Text has padding within the view.
**Actual:** Text crashes against the edges with zero padding.

---

## BUG-049: Nav links show spinner only on first click

| Module | Severity | Priority |
| --- | --- | --- |
| Homepage | Minor | Low |

**Steps**
1. Click a navigation link the first time. 2. Click again.
**Expected:** Consistent loading feedback each time.
**Actual:** Spinner fires on first click; second click does nothing.

---

## BUG-050: Invest/Waitlist spinners only on first use

| Module | Severity | Priority |
| --- | --- | --- |
| Homepage | Minor | Low |

**Steps**
1. Click "Invest in Réya"/"Waitlist" once. 2. Click again.
**Expected:** Consistent loading behavior.
**Actual:** Spinners show on first use only; repeat clicks skip loading animations.

---

## BUG-051: Footer "Sign Up" hyperlink is dead

| Module | Severity | Priority |
| --- | --- | --- |
| Homepage | Major | High |

**Steps**
1. Click the footer "Sign Up" hyperlink.
**Expected:** Opens signup target page.
**Actual:** Link points to no destination; nothing opens.

---

## BUG-052: Footer "Feedback" link doesn't scroll

| Module | Severity | Priority |
| --- | --- | --- |
| Homepage | Minor | Medium |

**Steps**
1. Click the footer "Feedback" link.
**Expected:** Smooth scroll to the feedback component.
**Actual:** No scroll action occurs.

---

## BUG-053: Footer "Support" link doesn't anchor-scroll

| Module | Severity | Priority |
| --- | --- | --- |
| Homepage | Minor | Medium |

**Steps**
1. Click footer "Support".
**Expected:** Scrolls to Help Desk channel cards.
**Actual:** No anchor scroll to the help channel blocks.

---

## BUG-054: Footer support email is dead

| Module | Severity | Priority |
| --- | --- | --- |
| Homepage | Minor | Medium |

**Steps**
1. Click `support@reyaapp.com` in the footer.
**Expected:** Opens mail client.
**Actual:** Link is dead and unclickable.

---

## BUG-055: Investment Tier not reset after account creation

| Module | Severity | Priority |
| --- | --- | --- |
| Investors | Minor | Low |

**Steps**
1. Submit the account creation form with a tier selected.
**Expected:** Tier selection resets / clears.
**Actual:** Selection persists instead of resetting.

---

## Summary (Part 1)

| Bug ID | Module | Severity | Status |
| --- | --- | --- | --- |
| BUG-001 to BUG-055 | See individual sections above | — | Open |

*Continue to [Part 2](bug-reports-part2.md) for BUG-056 to BUG-109.*