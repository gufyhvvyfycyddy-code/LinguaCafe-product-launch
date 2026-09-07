# Current Status — 2026-09-07

## Product

Current direction:
- English reading-first learning;
- concrete WordSense as learning content;
- sense-level ReviewCard + FSRS as formal scheduling;
- source occurrence retained as learning evidence;
- AI for explanation/translation/candidate/disambiguation;
- daily experience moving toward a simpler MaiMemo-like information hierarchy without copying its vocabulary or business model.

## Release

- Web/PC: most complete implementation; fresh current-baseline browser acceptance still required.
- Android: native implementation exists; current signed release/AAB/Play Console evidence is incomplete.
- iOS: native implementation exists; macOS/Xcode/signing/device/TestFlight/App Store evidence is incomplete.
- Server: candidate first-user topology is documented, but no completed public production deployment is claimed.

## Current product/launch evidence

Documents now cover:
- target-user hypotheses;
- 10 → 50 → 100 user-validation ladder;
- first-user server options;
- current Apple/Google store gates;
- privacy/account-deletion requirements;
- support/operations gaps;
- growth-channel hypotheses;
- pricing options;
- investor readiness.

No claim is made that real retention or product-market fit has already been proven.

## Cross-repository P0s

### Public source environment hygiene
Tracked environment-configuration paths remain in the public source tree.

See architecture Issue #1.

### Production dependency security
Dependabot currently reports 115 open alerts on the source default branch, including one Critical Laravel Reverb advisory.

A bounded remediation PR is open:
https://github.com/gufyhvvyfycyddy-code/LinguaCafe-local/pull/24

See architecture Issue #23.

## External gates

- Apple Developer membership / macOS / Xcode / signing / TestFlight / App Store.
- Google Play account / signed AAB / required testing / policy declarations / production access.
- Deployment-region decision, including mainland-China filing/compliance implications if that route is chosen.

## User / business gaps

Still unproven:
- first 10 deep-use users;
- first-10-minute onboarding;
- D1/D7 retention;
- retained users by acquisition channel;
- willingness to pay;
- support workload;
- investor-quality traction.

The next product milestone should be real-user evidence, not adding a large new feature surface.
