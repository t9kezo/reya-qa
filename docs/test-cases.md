# Test Case Report — REYA

> Product: REYA (women-only ride booking platform) • Tested By: Abhishek Kanwar
> Cycle: Functional, E2E & Regression — Cycle 1
> Environments: Web (Chrome 120 / Win 11), Android 14, iOS 17

## Summary

| Metric | Value |
| --- | --- |
| Total Test Cases (Executed) | 126 |
| Passed | 11 |
| On Hold (open defect) | 111 (each linked to a defect) |
| Blocked | 2 |
| Not Executed | 2 |
| Executed Pass Rate | 9% |
| Proposed Coverage (not yet executed) | 36 |

## Execution Report

| TC ID | Test Case | Environment | Expected Result | Actual Result | Status | Linked Bug |
| --- | --- | --- | --- | --- | --- | --- |
| RE_TC_01 | Heading/Subheading character limit | Web | Limit enforced | Unlimited text accepted | **On Hold** | BUG-001 |
| RE_TC_02 | Reject whitespace-only headings | Web | Whitespace rejected | Accepted | **On Hold** | BUG-002 |
| RE_TC_03 | Banner upload format restriction | Web | Only images accepted | Invalid formats accepted | **On Hold** | BUG-003 |
| RE_TC_04 | Update with empty headings shows error | Web | Validation error shown | No error thrown | **On Hold** | BUG-004 |
| RE_TC_05 | Banner size limit enforced | Web | Oversized rejected | No limit exists | **On Hold** | BUG-005 |
| RE_TC_06 | Save confirmation content | Web | Real confirmation | Placeholder text | **On Hold** | BUG-006 |
| RE_TC_07 | Upload format hints shown | Web | Hint text visible | No hint | **On Hold** | BUG-007 |
| RE_TC_08 | Re-upload banner after delete | Web | Same file uploadable | Blocked | **On Hold** | BUG-008 |
| RE_TC_09 | Title resets after update | Web | Resets to placeholder | Stale value remains | **On Hold** | BUG-009 |
| RE_TC_10 | Prevent duplicate tab content | Web | Duplication prevented | Duplication allowed | **On Hold** | BUG-010 |
| RE_TC_11 | Why REYA dropdown collapsed on load | Web | Collapsed | Open by default | **On Hold** | BUG-011 |
| RE_TC_12 | Deleted card removed from live site | Web | Removed | Remains on live site | **On Hold** | BUG-012 |
| RE_TC_13 | Loyalty menu selection state | Web | Only loyalty highlights | Header highlights too | **On Hold** | BUG-013 |
| RE_TC_14 | Custom axis labels on chart | Web | Labels shown | Not displayed | **On Hold** | BUG-014 |
| RE_TC_15 | Long text layout integrity | Web | Wraps cleanly | Overlaps adjacent UI | **On Hold** | BUG-015 |
| RE_TC_16 | About text within borders | Web | Fits borders | Overflows, clips | **On Hold** | BUG-016 |
| RE_TC_17 | GIF upload handling | Web | Consistent error | Misleading IMG/SVG error | **On Hold** | BUG-017 |
| RE_TC_18 | Security line-item limit | Web | Limit/counter enforced | Infinite items | **On Hold** | BUG-018 |
| RE_TC_19 | Join the Waitlist reliability | Web | Always works | Dead/random | **On Hold** | BUG-019 |
| RE_TC_20 | Registration submit | Web | Succeeds | Crash "investor creation failed" | **On Hold** | BUG-020 |
| RE_TC_21 | Onboarding DB write | Web | Data recorded | Not recorded | **On Hold** | BUG-021 |
| RE_TC_22 | Rider signup success redirect | Web | Dashboard state | Login modal | **On Hold** | BUG-022 |
| RE_TC_23 | Invest button target URL | Web | Correct page | Wrong URL | **On Hold** | BUG-023 |
| RE_TC_24 | Profile photo type restriction | Web | Images only | PDFs/videos accepted | **On Hold** | BUG-024 |
| RE_TC_25 | Block whitespace passwords | Web | Blocked | Accepted | **On Hold** | BUG-025 |
| RE_TC_26 | Onboarding format validation | Web | Errors shown | None | **On Hold** | BUG-026 |
| RE_TC_27 | Investment amount required | Web | Blocks empty submit | Empty accepted | **On Hold** | BUG-027 |
| RE_TC_28 | Validation clears after tier select | Web | Clears | Stuck errors | **On Hold** | BUG-028 |
| RE_TC_29 | Loyalty transition animations | Web | Animations play | Broken/missing | **On Hold** | BUG-029 |
| RE_TC_30 | Password reveal icons | Web | Single icon | Overlapping icons | **On Hold** | BUG-030 |
| RE_TC_31 | Driver Name 30-char limit | Web | Enforced | Ignored | **On Hold** | BUG-031 |
| RE_TC_32 | PDF upload preview | Web | Thumbnail shown | Blank container | **On Hold** | BUG-032 |
| RE_TC_33 | ToS label checkbox mapping | Web | Correct box checked | Wrong box checked | **On Hold** | BUG-033 |
| RE_TC_34 | Full Name inline error | Web | Inline error | Generic toast only | **On Hold** | BUG-034 |
| RE_TC_35 | Driver form validation alerts | Web | Alerts on each field | None | **On Hold** | BUG-035 |
| RE_TC_36 | I-confirm checkbox mapping | Web | Correct box checked | Wrong box checked | **On Hold** | BUG-036 |
| RE_TC_37 | Inquiry error clears on select | Web | Clears | Persists | **On Hold** | BUG-037 |
| RE_TC_38 | Form data reaches backend | Web | Data stored | Fails to push | **On Hold** | BUG-038 |
| RE_TC_39 | Profile photo validation | Web | Enforced | None | **On Hold** | BUG-039 |
| RE_TC_40 | Investment amount bypass | Web | Locked required | Bypassable | **On Hold** | BUG-040 |
| RE_TC_41 | Global registration | Web | Succeeds | Fails globally | **On Hold** | BUG-041 |
| RE_TC_42 | Phone validation timing | Web | After input | Fires immediately | **On Hold** | BUG-042 |
| RE_TC_43 | Dashboard auto-nav helper | Web | Present | Missing | **On Hold** | BUG-043 |
| RE_TC_44 | Ride ETA counter updates | Android | Counts down | Frozen at 0 min | **On Hold** | BUG-044 |
| RE_TC_45 | Dark mode complaint text visibility | Android | Visible text | Invisible text | **On Hold** | BUG-045 |
| RE_TC_46 | Pay Now shows only when due | Android | Hidden when none | Shown unnecessarily | **On Hold** | BUG-046 |
| RE_TC_47 | Tap message toast opens chat | Android | Chat opens | Nothing happens | **On Hold** | BUG-047 |
| RE_TC_48 | Driver-arrived notification padding | Android | Proper spacing | No padding, edge-crash | **On Hold** | BUG-048 |
| RE_TC_49 | Nav link loading feedback | Web | Consistent | First-click only | **On Hold** | BUG-049 |
| RE_TC_50 | Invest/Waitlist loading state | Web | Consistent | First-use only | **On Hold** | BUG-050 |
| RE_TC_51 | Footer Sign Up link | Web | Opens signup | Dead | **On Hold** | BUG-051 |
| RE_TC_52 | Footer Feedback scroll | Web | Scrolls | No scroll | **On Hold** | BUG-052 |
| RE_TC_53 | Footer Support anchor scroll | Web | Scrolls to channels | No anchor scroll | **On Hold** | BUG-053 |
| RE_TC_54 | Support email link | Web | Opens mail | Dead | **On Hold** | BUG-054 |
| RE_TC_55 | Tier reset after account creation | Web | Resets | Persists | **On Hold** | BUG-055 |
| RE_TC_56 | Valid JPG upload in Rider form | Web | Accepted | Rejected with wrong error | **On Hold** | BUG-056 |
| RE_TC_57 | Contact channel links | Web | All work | All dead | **On Hold** | BUG-057 |
| RE_TC_58 | Country code selection state | Web | Error clears | Error persists | **On Hold** | BUG-058 |
| RE_TC_59 | Email normalization | Web | Lowercased | Case-sensitive failures | **On Hold** | BUG-059 |
| RE_TC_60 | Vehicle Info wizard blank state | Web | Blank wizard | Random data preloaded | **On Hold** | BUG-060 |
| RE_TC_61 | OTP sent confirmation | Web | Message shown | Missing | **On Hold** | BUG-061 |
| RE_TC_62 | Resend OTP rate limit | Web | Cooldown enforced | Infinite spam | **On Hold** | BUG-062 |
| RE_TC_63 | New password view layout | Android | Usable | Keyboard blocks view | **On Hold** | BUG-063 |
| RE_TC_64 | Admin profile picture render | Web | Photo shown | "DP" initials | **On Hold** | BUG-064 |
| RE_TC_65 | Web→Mobile photo sync | Web+Android | Photo synced | Not synced | **On Hold** | BUG-065 |
| RE_TC_66 | Vehicle Number symbol input | Web | Validation error | Crash "Something went wrong" | **On Hold** | BUG-066 |
| RE_TC_67 | Web subscription on mobile | Web+Android | Active on mobile | Not activated | **On Hold** | BUG-067 |
| RE_TC_68 | Email update OTP rerouting | Web | OTP to new email | Stays with old email | **On Hold** | BUG-068 |
| RE_TC_69 | Auto-fill login submit | Web | Login proceeds | False "Account not found" | **On Hold** | BUG-069 |
| RE_TC_70 | Required photo indicator | Web | Asterisk shown | Missing | **On Hold** | BUG-070 |
| RE_TC_71 | Email dot-dot validation | Web | Rejected | Accepted | **On Hold** | BUG-071 |
| RE_TC_72 | Logout confirmation | Web | Feedback shown | None | **On Hold** | BUG-072 |
| RE_TC_73 | Country-code blank search | Web | Graceful | Results wiped | **On Hold** | BUG-073 |
| RE_TC_74 | Login password eye icon | Web | Single icon | Overlapping icons | **On Hold** | BUG-074 |
| RE_TC_75 | Empty phone display | Web | Shows "N/A" | Blank | **On Hold** | BUG-075 |
| RE_TC_76 | Unsubscribed Complete Payment | Web | No prompt / valid | "planId is required" | **On Hold** | BUG-076 |
| RE_TC_77 | Spanish translation | Android | Translated | Not applied | **On Hold** | BUG-077 |
| RE_TC_78 | OTP phone change modal | Web | One banner, modal closes | Duplicate banners, stays open | **On Hold** | BUG-078 |
| RE_TC_79 | Update Membership scroll position | Web | Stays | Jumps to bottom | **On Hold** | BUG-079 |
| RE_TC_80 | Plan upgrade checkout | Web | Proceeds | Falsely blocked | **On Hold** | BUG-080 |
| RE_TC_81 | Upgrade state consistency | Web | No change w/o payment | Plan changed w/o payment | **On Hold** | BUG-081 |
| RE_TC_82 | License/Plate special chars | Web | Rejected | Accepted | **On Hold** | BUG-082 |
| RE_TC_83 | Inline error clearing | Web | Clears | Stays | **On Hold** | BUG-083 |
| RE_TC_84 | Reset OTP field presence | Web | OTP field shown | Missing | **On Hold** | BUG-084 |
| RE_TC_85 | Payment status badge accuracy | Web | No active badge | Active badge shown | **On Hold** | BUG-085 |
| RE_TC_86 | Valid OTP acceptance | Web | Accepted | Rejected | **On Hold** | BUG-086 |
| RE_TC_87 | Driver ID warning clearing | Web | Clears | Persists | **On Hold** | BUG-087 |
| RE_TC_88 | Real-time char constraints | Web | Real-time | Submit-time only | **On Hold** | BUG-088 |
| RE_TC_89 | Safety countdown timer | Android | Updates | Frozen | **On Hold** | BUG-089 |
| RE_TC_90 | Home link active state | Web | Preserved | Deselects on reload | **On Hold** | BUG-090 |
| RE_TC_91 | Invest button consistency | Web | Same target | Different target | **On Hold** | BUG-091 |
| RE_TC_92 | Footer SignUp navigation | Web | Opens register | Goes top of homepage | **On Hold** | BUG-092 |
| RE_TC_93 | Newsletter validation UX | Web | Friendly warning | Raw JSON error | **On Hold** | BUG-093 |
| RE_TC_94 | Cookie Settings panel | Web | Opens panel | Silently refreshes | **On Hold** | BUG-094 |
| RE_TC_95 | Support email single-click | Web | Opens first click | Multi-click needed | **On Hold** | BUG-095 |
| RE_TC_96 | LinkedIn icon | Web | Opens LinkedIn | Fails to load | **On Hold** | BUG-096 |
| RE_TC_97 | About thumbnail crop | Web | Clean crop | Clipped border | **On Hold** | BUG-097 |
| RE_TC_98 | Express Interest submit (valid) | Web | Success | Raw JSON error | **On Hold** | BUG-098 |
| RE_TC_99 | Purchase Plan checkout | Web | Checkout starts | Nothing loads | **On Hold** | BUG-099 |
| RE_TC_100 | Rider form field layout | Web | Defined fields only | Extra empty input bar | **On Hold** | BUG-100 |
| RE_TC_101 | Rider Subscription submit (valid) | Web | Saves | Raw JSON error | **On Hold** | BUG-101 |
| RE_TC_102 | Rider photo requirement | Web | Blocks submit | Bypassed | **On Hold** | BUG-102 |
| RE_TC_103 | Driver Subscription submit (valid) | Web | Next step | Raw JSON error | **On Hold** | BUG-103 |
| RE_TC_104 | Driver mandatory fields | Web | Blocks submit | Bypassed | **On Hold** | BUG-104 |
| RE_TC_105 | City/Track default errors | Web | Errors shown | None | **On Hold** | BUG-105 |
| RE_TC_106 | Support link responsiveness | Web | Reliable | Slow/multi-tap + dead | **On Hold** | BUG-106 |
| RE_TC_107 | Contact form submit (valid) | Web | Sent | Raw JSON error | **On Hold** | BUG-107 |
| RE_TC_108 | Forgot password submit (valid) | Web | Reset flow | Raw JSON error | **On Hold** | BUG-108 |
| RE_TC_109 | Nav menu at 250% zoom | Web | Scrollable | Scroll locked | **On Hold** | BUG-109 |
| RE_TC_110 | Valid rider login | Android | Logs in | Passed as expected | Passed | — |
| RE_TC_111 | Valid driver login | Android | Logs in | Passed as expected | Passed | — |
| RE_TC_112 | Create ride request | Android | Request created | Passed as expected | Passed | — |
| RE_TC_113 | Request matching flow | Android | Match succeeds | Passed as expected | Passed | — |
| RE_TC_114 | Payment with valid method | Android | Succeeds | Passed as expected | Passed | — |
| RE_TC_115 | Trip completion flow | Android | Completes | Passed as expected | Passed | — |
| RE_TC_116 | Profile edit & view | Android | Updates correctly | Passed as expected | Passed | — |
| RE_TC_117 | Notification list rendering | Android | Renders | Passed as expected | Passed | — |
| RE_TC_118 | Ride history display | Android | Shows history | Passed as expected | Passed | — |
| RE_TC_119 | Home hero rendering | Web | Renders correctly | Passed as expected | Passed | — |
| RE_TC_120 | Newsletter valid email submit | Web | Success message | Passed as expected | Passed | — |
| RE_TC_121 | Contact page render | Web | Renders | Blocked by BUG-107 | Blocked | BUG-107 |
| RE_TC_122 | Purchase flow E2E | Web | Complete checkout | Blocked by BUG-099 | Blocked | BUG-099 |
| RE_TC_123 | iOS rider app smoke | iOS | Core flows pass | Not executed this cycle | Not Executed | — |
| RE_TC_124 | Performance (page load timings) | Web | Within threshold | Not executed this cycle | Not Executed | — |

## Additional Suggested Test Cases (Proposed Coverage — next cycle)

Suggested scenarios the app should be checked against. Not yet executed.

| TC ID | Test Case | Environment | Test Steps | Expected Result | Status |
| --- | --- | --- | --- | --- | --- |
| RE_TC_125 | Rider signup happy path (valid data) | Web | 1. Complete rider signup with valid data. | Account created, lands on dashboard | Proposed |
| RE_TC_126 | Driver signup happy path (valid data) | Web | 1. Complete driver signup with valid documents. | Account created, verification flow starts | Proposed |
| RE_TC_127 | Login with valid credentials | Web | 1. Enter valid credentials. 2. Submit. | Login succeeds | Proposed |
| RE_TC_128 | Login with invalid credentials | Web | 1. Enter wrong password. | Friendly error, no data leak | Proposed |
| RE_TC_129 | Logout clears session fully | Web | 1. Logout. 2. Access protected page. | Session cleared; protected pages require login | Proposed |
| RE_TC_130 | Profile photo upload (valid image) | Web | 1. Upload valid JPG/PNG. | Upload succeeds with preview | Proposed |
| RE_TC_131 | Edit personal details and save | Web | 1. Edit name/phone. 2. Save. | Changes persist | Proposed |
| RE_TC_132 | Change password flow | Web | 1. Change password with valid inputs. | Old password stops working, new works | Proposed |
| RE_TC_133 | OTP resend cooldown | Web | 1. Request OTP twice quickly. | Rate limit / cooldown enforced | Proposed |
| RE_TC_134 | Email format boundaries | Web | 1. Test `user@`, `@x.com`, no TLD, etc. | Invalid formats rejected | Proposed |
| RE_TC_135 | Phone format validation per country code | Web | 1. Enter valid/invalid digits per selected code. | Correct validation applied | Proposed |
| RE_TC_136 | Add valid payment card | Web | 1. Enter valid card details. | Card saved securely | Proposed |
| RE_TC_137 | Remove payment method | Web | 1. Delete saved card. | Card removed from list | Proposed |
| RE_TC_138 | Subscription plan pricing display | Web | 1. Open plans. | Prices and features render correctly | Proposed |
| RE_TC_139 | Cancel subscription flow | Web | 1. Initiate cancellation. 2. Confirm. | Subscription cancelled cleanly | Proposed |
| RE_TC_140 | Ride history detail view | Web | 1. Open a past ride. | Details (route, fare, driver) correct | Proposed |
| RE_TC_141 | Homepage hero rendering | Web | 1. Load homepage. | All hero elements render | Proposed |
| RE_TC_142 | About page content rendering | Web | 1. Load About page. | Content and images render | Proposed |
| RE_TC_143 | Express-interest form resets after submit | Web | 1. Submit then reopen form. | Fields cleared, success message shown | Proposed |
| RE_TC_144 | Newsletter unsubscribe link | Web | 1. Click unsubscribe in email. | Preference updated, no more emails | Proposed |
| RE_TC_145 | Cookie consent accept/reject | Web | 1. Accept cookies; reload. 2. Reject. | Preference saved and honored | Proposed |
| RE_TC_146 | Language switch (Spanish) on web | Web | 1. Set Spanish. 2. Browse pages. | UI translates across pages | Proposed |
| RE_TC_147 | Responsive breakpoints (tablet, mobile web) | Web | 1. Load at tablet and mobile widths. | Layout adapts, no overflow | Proposed |
| RE_TC_148 | Rider books a ride (happy path) | Android | 1. Set pickup → confirm payment → wait. | Booking confirmed, driver assigned | Proposed |
| RE_TC_149 | Driver accepts a request | Android | 1. Receive request. 2. Accept. | Request confirmed and routed | Proposed |
| RE_TC_150 | Fare estimate before booking | Android | 1. Enter route before confirming. | Estimate shown before commitment | Proposed |
| RE_TC_151 | Live location tracking during trip | Android | 1. Start trip; watch map. | Position updates on the map | Proposed |
| RE_TC_152 | Cancel ride with reason | Android | 1. Cancel after booking. | Cancellation recorded with reason | Proposed |
| RE_TC_153 | Rider rates driver after trip | Android | 1. Trip ends. 2. Submit rating. | Rating saved and reflected | Proposed |
| RE_TC_154 | Driver rates rider after trip | Android | 1. Trip ends. 2. Submit rating. | Rating saved and reflected | Proposed |
| RE_TC_155 | Push notification for new ride request | Android | 1. Driver online, request created. | Push received promptly | Proposed |
| RE_TC_156 | Driver online/offline toggle | Android | 1. Toggle availability. | Status reflects in dispatch | Proposed |
| RE_TC_157 | Safety countdown timer display | Android | 1. Open safety timer. | Countdown updates in real time | Proposed |
| RE_TC_158 | Emergency/help button behavior | Android | 1. Tap emergency button. | Help/SOS flow initialises | Proposed |
| RE_TC_159 | Payment failure during trip | Android | 1. Simulate declined payment. | Clear error + retry option, no trip block | Proposed |
| RE_TC_160 | Ride history sync web ↔ mobile | Web + Android | 1. Take a ride, check both platforms. | History consistent across platforms | Proposed |

## Executed — Ride App Passenger Module (Cycle 2)

| TC ID | Test Case | Environment | Expected Result | Actual Result | Status | Linked Bug |
| --- | --- | --- | --- | --- | --- | --- |
| RE_TC_161 | Passenger Name character limit | Android | Limit enforced with validation | No limit; unlimited text accepted | **On Hold** | BUG-110 |
| RE_TC_162 | Passenger name hidden on Submit button | Android | Generic button label | Name shown on button | **On Hold** | BUG-111 |

---
*Prepared by Abhishek Kanwar — for portfolio demonstration purposes.*