# REYA — QA Test Report

## Project Overview

**Product:** REYA — Women-only ride booking platform
**Type:** Web application + Mobile apps (Rider / Driver)
**Platforms Tested:** Web (Chrome, Windows 11), Android, iOS

**Modules Covered:** Homepage, Header/Content pages, Investor, Loyalty, Rider & Driver registration, Admin website, Driver/Rider mobile apps, Payments & subscriptions, Contact, Forgot Password, Profile, Language

**Tested By:** Abhishek Kanwar — QA Engineer (Manual & Functional Testing)

---

## Test Summary

| Metric | Value |
| --- | --- |
| Testing Type | Manual, Functional, End-to-End, Cross-platform, Regression |
| Test Cases Executed | 124 (11 passed, 109 failed, 2 blocked, 2 not executed) |
| **Total Bugs Found** | **109** |
| Open | 109 |
| Severity — Critical | 20 |
| Severity — Major | 33 |
| Severity — Minor | 56 |

## Key Findings

- **Form & data-loss failures across registration/onboarding:** multiple forms (Investor, Loyalty, Rider, Driver) crash with raw `Unexpected token '<', 'DOCTYPE'... is not valid JSON` errors and fail to save data, in several cases even with fully valid input. See BUG-020/021, 038, 098, 101, 103, 107, 108.
- **Validation is widely bypassable:** empty/whitespace-only fields accepted (BUG-025, 027, 040, 104), special characters accepted in License/Plate/Vehicle fields (BUG-066, 082), and invalid file formats/size limits not enforced (BUG-003, 005, 024).
- **Subscription & payment integrity broken:** upgrades falsely blocked by "already active subscription" (BUG-080/081), "Active" badge shown after failed payment (BUG-085), and web purchases not reflected in mobile app (BUG-067).
- **Account/verification flows unreliable:** OTPs rejected or never delivered (BUG-084, 086), email changes break OTP delivery (BUG-068), email casing causes login failures (BUG-059).
- **Widespread navigation/dead-link issues:** footer links, support channels, LinkedIn icon, and multiple buttons dead or misdirected (BUG-051–054, 057, 090–096, 106).
- **Cross-platform gaps:** web-profile photos not synced to mobile (BUG-065), subscriptions not activated on mobile (BUG-067), wrong validation error on valid JPG (BUG-056).

## Top Critical Defects

| Bug ID | Module | Issue |
| --- | --- | --- |
| [BUG-012](docs/bug-reports.md#bug-012-deleted-social-impact-card-remains-on-live-site) | Loyalty | Deleted social impact card stays on live site |
| [BUG-019](docs/bug-reports.md#bug-019-join-the-waitlist-button-dead) | Home | Join the Waitlist dead/unreliable |
| [BUG-020](docs/bug-reports.md#bug-020-registration-crashes-with-investor-creation-failed) | Home | Registration crashes — "investor creation failed" |
| [BUG-021](docs/bug-reports.md#bug-021-onboarding-data-not-recorded) | Home | Onboarding data not saved to DB |
| [BUG-027](docs/bug-reports.md#bug-027-mandatory-investment-amount-can-be-empty) | Investors | Mandatory investment amount can be empty |
| [BUG-038](docs/bug-reports.md#bug-038-forms-fail-to-push-to-backend) | Multiple | Registration/contact forms don't reach backend |
| [BUG-040](docs/bug-reports.md#bug-040-investment-amount-field-bypassable) | Investors | Investment Amount can be bypassed |
| [BUG-041](docs/bug-reports.md#bug-041-registration-fails-globally) | Investors | Global registration failure toast |
| [BUG-066](docs/bug-reports.md#bug-066-single-symbol-crashes-vehicle-number-field) | Admin | Single symbol in Vehicle Number crashes view |
| [BUG-067](docs/bug-reports.md#bug-067-web-subscriptions-not-active-on-mobile) | Admin | Web subscription not shown on mobile |
| [BUG-068](docs/bug-reports.md#bug-068-email-update-breaks-otp-delivery) | Admin | Updated email breaks login OTPs |
| [BUG-080](docs/bug-reports.md#bug-080-plan-upgrade-falsely-blocked) | Subscription | Upgrade blocked by false "active subscription" |
| [BUG-081](docs/bug-reports.md#bug-081-plan-updated-without-payment) | Subscription | Error shown yet plan updated without payment |
| [BUG-084](docs/bug-reports.md#bug-084-reset-linked-but-no-otp-field) | Forgot Password | No OTP field after reset link |
| [BUG-086](docs/bug-reports.md#bug-086-valid-otp-rejected) | Rider Web | Valid OTP rejected |
| [BUG-098](docs/bug-reports.md#bug-098-express-interest-form-json-error) | Investors Page | Valid form shows raw JSON error |
| [BUG-099](docs/bug-reports.md#bug-099-purchase-plan-no-checkout) | Loyalty Page | Purchase Plan triggers no checkout |
| [BUG-101](docs/bug-reports.md#bug-101-rider-subscription-json-error) | Loyalty Page | Rider subscription raw JSON error |
| [BUG-102](docs/bug-reports.md#bug-102-rider-photo-bypassable) | Loyalty Page | Rider photo upload can be bypassed |
| [BUG-103](docs/bug-reports.md#bug-103-driver-subscription-json-error) | Loyalty Page | Driver subscription raw JSON error |
| [BUG-104](docs/bug-reports.md#bug-104-driver-mandatory-fields-bypassed) | Loyalty Page | Driver mandatory fields can be empty |
| [BUG-107](docs/bug-reports.md#bug-107-contact-form-json-error) | Contact Page | Contact form raw JSON error |
| [BUG-108](docs/bug-reports.md#bug-108-forgot-password-json-error) | Forgot Password | Reset submission raw JSON error |

## Documents

- [Bug Reports — Part 1 (BUG-001 to BUG-055)](docs/bug-reports.md)
- [Bug Reports — Part 2 (BUG-056 to BUG-109)](docs/bug-reports-part2.md)
- [Test Cases](docs/test-cases.md) — manual test case report
- [Raw Bug Data](data/bugs.csv) — original defect tracking sheet

## Test Approach

- End-to-end manual testing of homepage, investor/loyalty pages, onboarding, payment and subscription flows.
- Admin website coverage (vehicle info, profiles, subscriptions, email management).
- Cross-platform verification across Web, Android, and iOS (rider/driver apps).
- Validation, boundary, and error-handling testing of every form.
- Dark mode, language, and zoom (accessibility) checks.

---
*Prepared by Abhishek Kanwar — for portfolio demonstration purposes.*