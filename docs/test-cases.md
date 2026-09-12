# Test Case Report — REYA

> Product: REYA (women-only ride booking platform) • Tested By: Abhishek Kanwar
> Cycle: Functional, E2E & Regression — Cycle 1
> Environments: Web (Chrome 120 / Win 11), Android 14, iOS 17

## Summary

| Metric | Value |
| --- | --- |
| Total Test Cases | 124 |
| Passed | 11 |
| Failed | 109 (each linked to a defect) |
| Blocked | 2 |
| Not Executed | 2 |
| Pass Rate | 9% |

## Execution Report

| TC ID | Test Case | Environment | Expected Result | Actual Result | Status | Linked Bug |
| --- | --- | --- | --- | --- | --- | --- |
| RE_TC_01 | Heading/Subheading character limit | Web | Limit enforced | Unlimited text accepted | **Failed** | BUG-001 |
| RE_TC_02 | Reject whitespace-only headings | Web | Whitespace rejected | Accepted | **Failed** | BUG-002 |
| RE_TC_03 | Banner upload format restriction | Web | Only images accepted | Invalid formats accepted | **Failed** | BUG-003 |
| RE_TC_04 | Update with empty headings shows error | Web | Validation error shown | No error thrown | **Failed** | BUG-004 |
| RE_TC_05 | Banner size limit enforced | Web | Oversized rejected | No limit exists | **Failed** | BUG-005 |
| RE_TC_06 | Save confirmation content | Web | Real confirmation | Placeholder text | **Failed** | BUG-006 |
| RE_TC_07 | Upload format hints shown | Web | Hint text visible | No hint | **Failed** | BUG-007 |
| RE_TC_08 | Re-upload banner after delete | Web | Same file uploadable | Blocked | **Failed** | BUG-008 |
| RE_TC_09 | Title resets after update | Web | Resets to placeholder | Stale value remains | **Failed** | BUG-009 |
| RE_TC_10 | Prevent duplicate tab content | Web | Duplication prevented | Duplication allowed | **Failed** | BUG-010 |
| RE_TC_11 | Why REYA dropdown collapsed on load | Web | Collapsed | Open by default | **Failed** | BUG-011 |
| RE_TC_12 | Deleted card removed from live site | Web | Removed | Remains on live site | **Failed** | BUG-012 |
| RE_TC_13 | Loyalty menu selection state | Web | Only loyalty highlights | Header highlights too | **Failed** | BUG-013 |
| RE_TC_14 | Custom axis labels on chart | Web | Labels shown | Not displayed | **Failed** | BUG-014 |
| RE_TC_15 | Long text layout integrity | Web | Wraps cleanly | Overlaps adjacent UI | **Failed** | BUG-015 |
| RE_TC_16 | About text within borders | Web | Fits borders | Overflows, clips | **Failed** | BUG-016 |
| RE_TC_17 | GIF upload handling | Web | Consistent error | Misleading IMG/SVG error | **Failed** | BUG-017 |
| RE_TC_18 | Security line-item limit | Web | Limit/counter enforced | Infinite items | **Failed** | BUG-018 |
| RE_TC_19 | Join the Waitlist reliability | Web | Always works | Dead/random | **Failed** | BUG-019 |
| RE_TC_20 | Registration submit | Web | Succeeds | Crash "investor creation failed" | **Failed** | BUG-020 |
| RE_TC_21 | Onboarding DB write | Web | Data recorded | Not recorded | **Failed** | BUG-021 |
| RE_TC_22 | Rider signup success redirect | Web | Dashboard state | Login modal | **Failed** | BUG-022 |
| RE_TC_23 | Invest button target URL | Web | Correct page | Wrong URL | **Failed** | BUG-023 |
| RE_TC_24 | Profile photo type restriction | Web | Images only | PDFs/videos accepted | **Failed** | BUG-024 |
| RE_TC_25 | Block whitespace passwords | Web | Blocked | Accepted | **Failed** | BUG-025 |
| RE_TC_26 | Onboarding format validation | Web | Errors shown | None | **Failed** | BUG-026 |
| RE_TC_27 | Investment amount required | Web | Blocks empty submit | Empty accepted | **Failed** | BUG-027 |
| RE_TC_28 | Validation clears after tier select | Web | Clears | Stuck errors | **Failed** | BUG-028 |
| RE_TC_29 | Loyalty transition animations | Web | Animations play | Broken/missing | **Failed** | BUG-029 |
| RE_TC_30 | Password reveal icons | Web | Single icon | Overlapping icons | **Failed** | BUG-030 |
| RE_TC_31 | Driver Name 30-char limit | Web | Enforced | Ignored | **Failed** | BUG-031 |
| RE_TC_32 | PDF upload preview | Web | Thumbnail shown | Blank container | **Failed** | BUG-032 |
| RE_TC_33 | ToS label checkbox mapping | Web | Correct box checked | Wrong box checked | **Failed** | BUG-033 |
| RE_TC_34 | Full Name inline error | Web | Inline error | Generic toast only | **Failed** | BUG-034 |
| RE_TC_35 | Driver form validation alerts | Web | Alerts on each field | None | **Failed** | BUG-035 |
| RE_TC_36 | I-confirm checkbox mapping | Web | Correct box checked | Wrong box checked | **Failed** | BUG-036 |
| RE_TC_37 | Inquiry error clears on select | Web | Clears | Persists | **Failed** | BUG-037 |
| RE_TC_38 | Form data reaches backend | Web | Data stored | Fails to push | **Failed** | BUG-038 |
| RE_TC_39 | Profile photo validation | Web | Enforced | None | **Failed** | BUG-039 |
| RE_TC_40 | Investment amount bypass | Web | Locked required | Bypassable | **Failed** | BUG-040 |
| RE_TC_41 | Global registration | Web | Succeeds | Fails globally | **Failed** | BUG-041 |
| RE_TC_42 | Phone validation timing | Web | After input | Fires immediately | **Failed** | BUG-042 |
| RE_TC_43 | Dashboard auto-nav helper | Web | Present | Missing | **Failed** | BUG-043 |
| RE_TC_44 | Ride ETA counter updates | Android | Counts down | Frozen at 0 min | **Failed** | BUG-044 |
| RE_TC_45 | Dark mode complaint text visibility | Android | Visible text | Invisible text | **Failed** | BUG-045 |
| RE_TC_46 | Pay Now shows only when due | Android | Hidden when none | Shown unnecessarily | **Failed** | BUG-046 |
| RE_TC_47 | Tap message toast opens chat | Android | Chat opens | Nothing happens | **Failed** | BUG-047 |
| RE_TC_48 | Driver-arrived notification padding | Android | Proper spacing | No padding, edge-crash | **Failed** | BUG-048 |
| RE_TC_49 | Nav link loading feedback | Web | Consistent | First-click only | **Failed** | BUG-049 |
| RE_TC_50 | Invest/Waitlist loading state | Web | Consistent | First-use only | **Failed** | BUG-050 |
| RE_TC_51 | Footer Sign Up link | Web | Opens signup | Dead | **Failed** | BUG-051 |
| RE_TC_52 | Footer Feedback scroll | Web | Scrolls | No scroll | **Failed** | BUG-052 |
| RE_TC_53 | Footer Support anchor scroll | Web | Scrolls to channels | No anchor scroll | **Failed** | BUG-053 |
| RE_TC_54 | Support email link | Web | Opens mail | Dead | **Failed** | BUG-054 |
| RE_TC_55 | Tier reset after account creation | Web | Resets | Persists | **Failed** | BUG-055 |
| RE_TC_56 | Valid JPG upload in Rider form | Web | Accepted | Rejected with wrong error | **Failed** | BUG-056 |
| RE_TC_57 | Contact channel links | Web | All work | All dead | **Failed** | BUG-057 |
| RE_TC_58 | Country code selection state | Web | Error clears | Error persists | **Failed** | BUG-058 |
| RE_TC_59 | Email normalization | Web | Lowercased | Case-sensitive failures | **Failed** | BUG-059 |
| RE_TC_60 | Vehicle Info wizard blank state | Web | Blank wizard | Random data preloaded | **Failed** | BUG-060 |
| RE_TC_61 | OTP sent confirmation | Web | Message shown | Missing | **Failed** | BUG-061 |
| RE_TC_62 | Resend OTP rate limit | Web | Cooldown enforced | Infinite spam | **Failed** | BUG-062 |
| RE_TC_63 | New password view layout | Android | Usable | Keyboard blocks view | **Failed** | BUG-063 |
| RE_TC_64 | Admin profile picture render | Web | Photo shown | "DP" initials | **Failed** | BUG-064 |
| RE_TC_65 | Web→Mobile photo sync | Web+Android | Photo synced | Not synced | **Failed** | BUG-065 |
| RE_TC_66 | Vehicle Number symbol input | Web | Validation error | Crash "Something went wrong" | **Failed** | BUG-066 |
| RE_TC_67 | Web subscription on mobile | Web+Android | Active on mobile | Not activated | **Failed** | BUG-067 |
| RE_TC_68 | Email update OTP rerouting | Web | OTP to new email | Stays with old email | **Failed** | BUG-068 |
| RE_TC_69 | Auto-fill login submit | Web | Login proceeds | False "Account not found" | **Failed** | BUG-069 |
| RE_TC_70 | Required photo indicator | Web | Asterisk shown | Missing | **Failed** | BUG-070 |
| RE_TC_71 | Email dot-dot validation | Web | Rejected | Accepted | **Failed** | BUG-071 |
| RE_TC_72 | Logout confirmation | Web | Feedback shown | None | **Failed** | BUG-072 |
| RE_TC_73 | Country-code blank search | Web | Graceful | Results wiped | **Failed** | BUG-073 |
| RE_TC_74 | Login password eye icon | Web | Single icon | Overlapping icons | **Failed** | BUG-074 |
| RE_TC_75 | Empty phone display | Web | Shows "N/A" | Blank | **Failed** | BUG-075 |
| RE_TC_76 | Unsubscribed Complete Payment | Web | No prompt / valid | "planId is required" | **Failed** | BUG-076 |
| RE_TC_77 | Spanish translation | Android | Translated | Not applied | **Failed** | BUG-077 |
| RE_TC_78 | OTP phone change modal | Web | One banner, modal closes | Duplicate banners, stays open | **Failed** | BUG-078 |
| RE_TC_79 | Update Membership scroll position | Web | Stays | Jumps to bottom | **Failed** | BUG-079 |
| RE_TC_80 | Plan upgrade checkout | Web | Proceeds | Falsely blocked | **Failed** | BUG-080 |
| RE_TC_81 | Upgrade state consistency | Web | No change w/o payment | Plan changed w/o payment | **Failed** | BUG-081 |
| RE_TC_82 | License/Plate special chars | Web | Rejected | Accepted | **Failed** | BUG-082 |
| RE_TC_83 | Inline error clearing | Web | Clears | Stays | **Failed** | BUG-083 |
| RE_TC_84 | Reset OTP field presence | Web | OTP field shown | Missing | **Failed** | BUG-084 |
| RE_TC_85 | Payment status badge accuracy | Web | No active badge | Active badge shown | **Failed** | BUG-085 |
| RE_TC_86 | Valid OTP acceptance | Web | Accepted | Rejected | **Failed** | BUG-086 |
| RE_TC_87 | Driver ID warning clearing | Web | Clears | Persists | **Failed** | BUG-087 |
| RE_TC_88 | Real-time char constraints | Web | Real-time | Submit-time only | **Failed** | BUG-088 |
| RE_TC_89 | Safety countdown timer | Android | Updates | Frozen | **Failed** | BUG-089 |
| RE_TC_90 | Home link active state | Web | Preserved | Deselects on reload | **Failed** | BUG-090 |
| RE_TC_91 | Invest button consistency | Web | Same target | Different target | **Failed** | BUG-091 |
| RE_TC_92 | Footer SignUp navigation | Web | Opens register | Goes top of homepage | **Failed** | BUG-092 |
| RE_TC_93 | Newsletter validation UX | Web | Friendly warning | Raw JSON error | **Failed** | BUG-093 |
| RE_TC_94 | Cookie Settings panel | Web | Opens panel | Silently refreshes | **Failed** | BUG-094 |
| RE_TC_95 | Support email single-click | Web | Opens first click | Multi-click needed | **Failed** | BUG-095 |
| RE_TC_96 | LinkedIn icon | Web | Opens LinkedIn | Fails to load | **Failed** | BUG-096 |
| RE_TC_97 | About thumbnail crop | Web | Clean crop | Clipped border | **Failed** | BUG-097 |
| RE_TC_98 | Express Interest submit (valid) | Web | Success | Raw JSON error | **Failed** | BUG-098 |
| RE_TC_99 | Purchase Plan checkout | Web | Checkout starts | Nothing loads | **Failed** | BUG-099 |
| RE_TC_100 | Rider form field layout | Web | Defined fields only | Extra empty input bar | **Failed** | BUG-100 |
| RE_TC_101 | Rider Subscription submit (valid) | Web | Saves | Raw JSON error | **Failed** | BUG-101 |
| RE_TC_102 | Rider photo requirement | Web | Blocks submit | Bypassed | **Failed** | BUG-102 |
| RE_TC_103 | Driver Subscription submit (valid) | Web | Next step | Raw JSON error | **Failed** | BUG-103 |
| RE_TC_104 | Driver mandatory fields | Web | Blocks submit | Bypassed | **Failed** | BUG-104 |
| RE_TC_105 | City/Track default errors | Web | Errors shown | None | **Failed** | BUG-105 |
| RE_TC_106 | Support link responsiveness | Web | Reliable | Slow/multi-tap + dead | **Failed** | BUG-106 |
| RE_TC_107 | Contact form submit (valid) | Web | Sent | Raw JSON error | **Failed** | BUG-107 |
| RE_TC_108 | Forgot password submit (valid) | Web | Reset flow | Raw JSON error | **Failed** | BUG-108 |
| RE_TC_109 | Nav menu at 250% zoom | Web | Scrollable | Scroll locked | **Failed** | BUG-109 |
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

---
*Prepared by Abhishek Kanwar — for portfolio demonstration purposes.*