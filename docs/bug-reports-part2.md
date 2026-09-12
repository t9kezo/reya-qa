# Bug Reports — REYA (Part 2: BUG-056 to BUG-109)

> Product: REYA (women-only ride booking platform) • Tested by: Abhishek Kanwar
> Environment (unless noted): Web — Chrome 120, Windows 11; Android 14; iOS 17 • Status legend: Open

---

## BUG-056: Valid JPG rejected with "valid image or PDF" error

| Module | Severity | Priority |
| --- | --- | --- |
| Loyalty | Major | High |

**Steps**
1. In Rider registration, upload a valid JPG file.
**Expected:** File accepted.
**Actual:** JPG breaks with "Please upload a valid image or PDF" even though it is valid.

---

## BUG-057: All support channel links are dead

| Module | Severity | Priority |
| --- | --- | --- |
| Contact | Major | High |

**Steps**
1. Open the contact/support section. 2. Tap each communication channel link.
**Expected:** Each opens the relevant channel.
**Actual:** All links are dead and do not respond on tap.

---

## BUG-058: "Please select a country code" shown despite selection

| Module | Severity | Priority |
| --- | --- | --- |
| Admin / Website | Major | High |

**Steps**
1. Select a valid country code.
**Expected:** Error indicator clears.
**Actual:** "Please select a country code" text still shows.

---

## BUG-059: Emails not lowercased — capitalization causes login errors

| Module | Severity | Priority |
| --- | --- | --- |
| Admin / Multi-platform | Major | High |

**Steps**
1. Register with a capitalized email (e.g. John@...). 2. Attempt login.
**Expected:** Emails normalized to lowercase; login works.
**Actual:** Emails store as entered; login fails on case mismatch.

---

## BUG-060: Vehicle Info panel preloads random data

| Module | Severity | Priority |
| --- | --- | --- |
| Admin / Website | Minor | Medium |

**Steps**
1. Open the Vehicle Info setup panel.
**Expected:** Clean/blank input wizard.
**Actual:** Random default data rows pre-load.

---

## BUG-061: No "OTP sent successfully" confirmation

| Module | Severity | Priority |
| --- | --- | --- |
| Admin / Website | Minor | Low |

**Steps**
1. Dispatch a mobile OTP code.
**Expected:** Visual confirmation message.
**Actual:** No "OTP sent successfully" message appears.

---

## BUG-062: "Resend OTP" has no rate limit

| Module | Severity | Priority |
| --- | --- | --- |
| Admin / Multi-platform | Major | High |

**Steps**
1. On Forgot Password, spam "Resend OTP".
**Expected:** Cooldown/rate limit enforced.
**Actual:** Button can be triggered infinitely with no cooldown.

---

## BUG-063: Phone keyboard auto-opens and blocks the view

| Module | Severity | Priority |
| --- | --- | --- |
| Admin / Multi-platform | Minor | Medium |

**Steps**
1. Open the Set New Password view.
**Expected:** Layout remains usable.
**Actual:** Phone keyboard forcibly opens, blocking layout views.

---

## BUG-064: Admin-generated profiles show "DP" initials instead of photos

| Module | Severity | Priority |
| --- | --- | --- |
| Admin / Multi-platform | Major | High |

**Steps**
1. Generate a profile manually in the admin panel.
**Expected:** Profile picture shown on the profile.
**Actual:** Default "DP" initials text renders instead.

---

## BUG-065: Web profile photos not synced to mobile app

| Module | Severity | Priority |
| --- | --- | --- |
| Admin / Website | Major | High |

**Steps**
1. Upload a profile picture via a web account. 2. Open the mobile app avatar zone.
**Expected:** Photo synced to mobile avatar.
**Actual:** Photo never passes over to the app.

---

## BUG-066: Single symbol in Vehicle Number crashes the view

| Module | Severity | Priority |
| --- | --- | --- |
| Admin / Multi-platform | **Critical** | High |

**Steps**
1. Enter a single symbol (e.g. `#`) into the Vehicle Number field.
**Expected:** A validation error message.
**Actual:** View crashes with a "Something went wrong" block.

---

## BUG-067: Web subscriptions not activated on the mobile app

| Module | Severity | Priority |
| --- | --- | --- |
| Admin / Multi-platform | **Critical** | High |

**Steps**
1. Purchase a subscription via the web. 2. Log into the mobile app dashboard.
**Expected:** Subscription active and displayed.
**Actual:** Purchase does not activate or appear on mobile.

---

## BUG-068: Updating user email breaks login OTP delivery

| Module | Severity | Priority |
| --- | --- | --- |
| Admin / Website | **Critical** | High |

**Steps**
1. Update a user's email in the admin table.
**Expected:** Login OTPs go to the new email.
**Actual:** OTPs keep going to the old email; account loop breaks.

---

## BUG-069: Login auto-fill triggers false "Account not found"

| Module | Severity | Priority |
| --- | --- | --- |
| Website: Login | Major | High |

**Steps**
1. Open the login page (inputs may auto-fill from browser). 2. Click submit.
**Expected:** Login proceeds with the filled credentials.
**Actual:** Auto-filled stale text triggers a false "Account not found" blocker.

---

## BUG-070: Mandatory profile picture lacks required indicator

| Module | Severity | Priority |
| --- | --- | --- |
| Website: Sign up | Minor | Low |

**Steps**
1. View the signup form.
**Expected:** Required field marked with a red asterisk.
**Actual:** Profile picture is required but shows no asterisk.

---

## BUG-071: Email handles with consecutive dots accepted

| Module | Severity | Priority |
| --- | --- | --- |
| Website: Sign up | Minor | Medium |

**Steps**
1. Enter an email like `..user@email.com`.
**Expected:** Rejected as invalid.
**Actual:** Invalid handles starting with consecutive dots are accepted.

---

## BUG-072: Logout gives no visual confirmation

| Module | Severity | Priority |
| --- | --- | --- |
| Website: Logout | Minor | Medium |

**Steps**
1. Tap the logout button.
**Expected:** Confirmation / success feedback.
**Actual:** Session clears but no visual confirmation appears.

---

## BUG-073: Blank space in country-code lookup wipes results

| Module | Severity | Priority |
| --- | --- | --- |
| Website: Sign up | Minor | Low |

**Steps**
1. In the country-code prompt, type a blank space.
**Expected:** Suggestions remain / handle gracefully.
**Actual:** All visible search results are wiped out.

---

## BUG-074: Overlapping password eye icons (Login)

| Module | Severity | Priority |
| --- | --- | --- |
| Website: Login | Minor | Low |

**Steps**
1. Type into the password box on login.
**Expected:** Single eye toggle rendered.
**Actual:** Two visibility icons render stacked on each other.

---

## BUG-075: Missing phone number shows blank instead of "N/A"

| Module | Severity | Priority |
| --- | --- | --- |
| Profile Details | Minor | Low |

**Steps**
1. View a profile with no recorded mobile number.
**Expected:** Field displays "N/A".
**Actual:** The field line stays empty.

---

## BUG-076: Unsubscribed users see a broken "Complete Payment" link

| Module | Severity | Priority |
| --- | --- | --- |
| Profile Details | Major | High |

**Steps**
1. Log in as an unsubscribed user. 2. Click "Complete Payment".
**Expected:** No payment prompt, or valid behavior.
**Actual:** "planId is required" error is thrown on click.

---

## BUG-077: Spanish language setting not applied to app views

| Module | Severity | Priority |
| --- | --- | --- |
| Language Controls | Major | High |

**Steps**
1. Switch the app preference to Spanish.
**Expected:** Text translates across main views.
**Actual:** Spanish is not applied; text stays untranslated.

---

## BUG-078: OTP phone change shows duplicate banners and modal stays open

| Module | Severity | Priority |
| --- | --- | --- |
| Verification Flows | Minor | Medium |

**Steps**
1. Confirm a phone number change via OTP.
**Expected:** Single success banner; modal closes.
**Actual:** Two duplicate success banners; modal stays open.

---

## BUG-079: "Update Membership" scrolls viewport to page bottom

| Module | Severity | Priority |
| --- | --- | --- |
| Subscription Upgrades | Major | High |

**Steps**
1. Tap "Update Membership".
**Expected:** Stay on the current view.
**Actual:** Viewport jumps instantly to the bottom of the page.

---

## BUG-080: Plan upgrade falsely blocked as "already active"

| Module | Severity | Priority |
| --- | --- | --- |
| Subscription Upgrades | **Critical** | High |

**Steps**
1. As a valid user, attempt to upgrade a plan.
**Expected:** Checkout/upgrade proceeds.
**Actual:** False "User already has an active or pending subscription" alert blocks payment.

---

## BUG-081: Upgrade error shown, yet plan updated without payment

| Module | Severity | Priority |
| --- | --- | --- |
| Subscription Upgrades | **Critical** | High |

**Steps**
1. Attempt an upgrade; observe the "already active subscription" error. 2. Check profile details.
**Expected:** No plan change without payment.
**Actual:** Plan updates without any payment while the error is shown — inconsistent state.

---

## BUG-082: License and Plate fields accept special characters

| Module | Severity | Priority |
| --- | --- | --- |
| Website: Sign up | Major | High |

**Steps**
1. As a driver, fill License/Plate with only special characters (`#@$...`).
**Expected:** Validation rejects them.
**Actual:** Registration is bypassed and accepted.

---

## BUG-083: Inline validation errors never clear

| Module | Severity | Priority |
| --- | --- | --- |
| Website: Sign up | Minor | Medium |

**Steps**
1. Trigger a validation error. 2. Fix the input to valid data.
**Expected:** Errors disappear.
**Actual:** Inline errors stay stuck on screen.

---

## BUG-084: Reset email sent but no OTP field presented

| Module | Severity | Priority |
| --- | --- | --- |
| Forgot Password | **Critical** | High |

**Steps**
1. Submit a password reset. 2. Wait for the reset link email.
**Expected:** An OTP verification field follows the reset link.
**Actual:** No OTP field is ever presented; recovery pipeline is blocked.

---

## BUG-085: "Active" badge shown despite failed payment

| Module | Severity | Priority |
| --- | --- | --- |
| Rider Web | Major | High |

**Steps**
1. Have a checkout payment transaction fail.
**Expected:** Subscription not marked active.
**Actual:** Dashboard shows an "Active" status badge even though payment failed.

---

## BUG-086: Valid OTP codes rejected during registration

| Module | Severity | Priority |
| --- | --- | --- |
| Rider Web | **Critical** | High |

**Steps**
1. During phone registration, receive and enter an authentic OTP.
**Expected:** OTP accepted; registration proceeds.
**Actual:** Valid OTPs are rejected.

---

## BUG-087: Red warnings persist after correcting driver IDs

| Module | Severity | Priority |
| --- | --- | --- |
| Driver Web | Minor | Medium |

**Steps**
1. Correct Driver and Vehicle identification numbers after an error.
**Expected:** Warnings clear.
**Actual:** Red warning text remains on screen.

---

## BUG-088: Character constraints only run at final submit

| Module | Severity | Priority |
| --- | --- | --- |
| Driver Web | Minor | Medium |

**Steps**
1. Type into Driver/License fields.
**Expected:** Constraints validate in real-time.
**Actual:** Checks run only during final form submission.

---

## BUG-089: Safety countdown timer is frozen

| Module | Severity | Priority |
| --- | --- | --- |
| Driver App | Major | High |

**Steps**
1. Open the "drive to get off the app" safety countdown.
**Expected:** Remaining hours update in real time.
**Actual:** Timer stays frozen.

---

## BUG-090: Home link deselects on silent reload

| Module | Severity | Priority |
| --- | --- | --- |
| Homepage | Minor | Low |

**Steps**
1. Click the "App Coming Soon" button. 2. Watch the highlighted home navigation link.
**Expected:** Active link state preserved.
**Actual:** Home link unselects itself during a silent page reload.

---

## BUG-091: Invest button in video section routes to wrong target

| Module | Severity | Priority |
| --- | --- | --- |
| Homepage | Minor | Medium |

**Steps**
1. Click "Invest in Réya" in the header — goes to Express Your Interest form (correct).
2. Click the same button inside the video playback section.
**Expected:** Same destination.
**Actual:** Wrongly redirects to the header section of the investors page.

---

## BUG-092: Footer SignUp goes to top of homepage

| Module | Severity | Priority |
| --- | --- | --- |
| Homepage | Minor | Medium |

**Steps**
1. On the homepage footer, click the SignUp link (newsletter category).
**Expected:** Opens a registration screen/modal.
**Actual:** Redirects straight back to the top of the homepage.

---

## BUG-093: Newsletter invalid input throws raw JSON error

| Module | Severity | Priority |
| --- | --- | --- |
| Homepage | Major | High |

**Steps**
1. Submit invalid characters, or leave the newsletter email blank.
**Expected:** Proper validation warning.
**Actual:** Raw error: `Unexpected token '<', 'DOCTYPE'... is not valid JSON`.

---

## BUG-094: Cookie Settings silently refreshes page

| Module | Severity | Priority |
| --- | --- | --- |
| Homepage | Minor | Low |

**Steps**
1. Click "Cookie Settings" in the footer.
**Expected:** Cookie configuration panel opens.
**Actual:** Screen silently refreshes instead.

---

## BUG-095: Support email link needs multiple clicks

| Module | Severity | Priority |
| --- | --- | --- |
| Homepage | Minor | Low |

**Steps**
1. Click the support email link once, then multiple times.
**Expected:** Opens on first click.
**Actual:** Needs several clicks before it redirects to Gmail.

---

## BUG-096: LinkedIn icon fails to load

| Module | Severity | Priority |
| --- | --- | --- |
| Homepage | Minor | Medium |

**Steps**
1. Click the LinkedIn social media icon.
**Expected:** Opens the LinkedIn page.
**Actual:** Target webpage stalls and fails to load.

---

## BUG-097: About title thumbnail cropped incorrectly

| Module | Severity | Priority |
| --- | --- | --- |
| About Us | Minor | Low |

**Steps**
1. View the title thumbnail image on the About page.
**Expected:** Clean crop within container radius.
**Actual:** Image is clipped awkwardly against the border-radius.

---

## BUG-098: Valid Express Interest form throws raw JSON error

| Module | Severity | Priority |
| --- | --- | --- |
| Investors Page | **Critical** | High |

**Steps**
1. Fill the Express Your Interest form with fully valid entries. 2. Submit.
**Expected:** Success state.
**Actual:** Raw error: `Unexpected token '<', 'DOCTYPE'... is not valid JSON`.

---

## BUG-099: Purchase Plan never triggers checkout

| Module | Severity | Priority |
| --- | --- | --- |
| Loyalty Page | **Critical** | High |

**Steps**
1. Open a plan modal. 2. Click "Purchase Plan" for any tier.
**Expected:** Checkout process starts.
**Actual:** Nothing loads or triggers.

---

## BUG-100: Rider Subscription form shows an empty input bar

| Module | Severity | Priority |
| --- | --- | --- |
| Loyalty Page | Minor | Low |

**Steps**
1. Open the Rider Subscription form.
**Expected:** Only defined fields render.
**Actual:** An unnecessary empty input bar appears below the profile photo upload.

---

## BUG-101: Valid Rider Subscription submission throws JSON error

| Module | Severity | Priority |
| --- | --- | --- |
| Loyalty Page | **Critical** | High |

**Steps**
1. Fill the Rider Subscription form with accurate details. 2. Submit.
**Expected:** Data saved.
**Actual:** Raw error: `Unexpected token 'I', 'Internal S'... is not valid JSON`.

---

## BUG-102: Rider profile photo requirement can be bypassed

| Module | Severity | Priority |
| --- | --- | --- |
| Loyalty Page | **Critical** | High |

**Steps**
1. Skip the profile photo upload. 2. Submit the Rider Subscription form.
**Expected:** Required photo blocks submission.
**Actual:** Form submits without any image.

---

## BUG-103: Valid Driver Subscription submission shows raw DB error

| Module | Severity | Priority |
| --- | --- | --- |
| Loyalty Page | **Critical** | High |

**Steps**
1. Complete all mandatory rows in the Driver Subscription form. 2. Submit.
**Expected:** Advances to the next step.
**Actual:** Raw error: `Unexpected token 'I', 'Internal S'... is not valid JSON`; no progression.

---

## BUG-104: Driver mandatory fields can be left empty

| Module | Severity | Priority |
| --- | --- | --- |
| Loyalty Page | **Critical** | High |

**Steps**
1. Leave Driving License, Vehicle Registration, Vehicle Insurance, and Training Certificates empty. 2. Submit.
**Expected:** Mandatory-field errors block submission.
**Actual:** Driver registration bypasses validation and succeeds.

---

## BUG-105: City/Track defaults produce no validation errors

| Module | Severity | Priority |
| --- | --- | --- |
| Loyalty Page | Minor | Low |

**Steps**
1. Leave City and Select Track on default placeholders. 2. Submit driver registration.
**Expected:** Visual error messages shown.
**Actual:** No errors are triggered.

---

## BUG-106: Support links slow/multi-tap and some dead

| Module | Severity | Priority |
| --- | --- | --- |
| Contact Page | Major | High |

**Steps**
1. Click the email support link. 2. Try Call Center and Live Support links.
**Expected:** All respond reliably.
**Actual:** Email link is slow and needs multiple taps; Call Center and Live Support route nowhere.

---

## BUG-107: Valid Contact form submission shows raw JSON error

| Module | Severity | Priority |
| --- | --- | --- |
| Contact Page | **Critical** | High |

**Steps**
1. Fill "Send Us a Message" with valid inputs. 2. Submit.
**Expected:** Message sent.
**Actual:** Raw error: `Unexpected token '<', 'DOCTYPE'... is not valid JSON`.

---

## BUG-108: Forgot Password with valid email shows raw JSON error

| Module | Severity | Priority |
| --- | --- | --- |
| Forgot password Screen | **Critical** | High |

**Steps**
1. Submit a valid email to trigger a reset.
**Expected:** Reset link flow proceeds.
**Actual:** Raw error: `Unexpected token '<', 'DOCTYPE'... is not valid JSON`; pipeline blocked.

---

## BUG-109: 250% zoom breaks nav-menu scrolling

| Module | Severity | Priority |
| --- | --- | --- |
| Homepage | Major | High |

**Steps**
1. Zoom browser to 250%. 2. Open the expanded navigation menu. 3. Try to scroll to hidden links.
**Expected:** Menu remains scrollable.
**Actual:** Scroll is locked; hidden navigation links are unreachable.

---

## BUG-110: Ride App — Passenger Name field has no character limit

| Field | Value |
| --- | --- |
| Bug ID | BUG-110 |
| Module | Ride App — Passenger Details |
| Severity | Minor |
| Priority | Medium |

**Steps to Reproduce**
1. Open the ride app booking flow. 2. Enter an extremely long string in the Passenger Name field.

**Expected Result**
A character limit is enforced with validation on the Passenger Name field.

**Actual Result**
No character limit exists; users can enter unlimited text in the Passenger Name field.

---

## BUG-111: Ride App — Passenger name shown on the Submit button

| Field | Value |
| --- | --- |
| Bug ID | BUG-111 |
| Module | Ride App — Booking (Submit Button) |
| Severity | Minor |
| Priority | Medium |

**Steps to Reproduce**
1. Open the ride app booking flow. 2. Enter a passenger name. 3. Observe the Submit button text.

**Expected Result**
The Submit button shows a generic label (e.g., "Submit") — the passenger's name should not appear on it.

**Actual Result**
The passenger's name is displayed on the Submit button, which is incorrect and potentially confusing to the user.

---

## Summary (Part 2)

| Bug ID | Module | Severity | Status |
| --- | --- | --- | --- |
| BUG-056 to BUG-109 | See individual sections above | — | Open |
| BUG-110 | Ride App — Passenger Details | Minor | Open |
| BUG-111 | Ride App — Booking (Submit Button) | Minor | Open |

---

## Overall Summary (BUG-001 to BUG-111)

| Severity | Count |
| --- | --- |
| Critical | 20 |
| Major | 33 |
| Minor | 58 |
| **Total** | **111** |

All 111 defects remain **Open** pending development fixes and re-testing.