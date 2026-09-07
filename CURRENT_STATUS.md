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

- Web/PC: most complete implementation; fresh current-baseline browser acceptance is still required until a live run is recorded.
- Android: native implementation exists; current signed release/AAB/Play Console evidence is incomplete.
- iOS: native implementation exists; macOS/Xcode/signing/device/TestFlight/App Store evidence is incomplete.
- Server: candidate first-user topology is documented, but no completed public production deployment is claimed.

## Current product/launch evidence

Documents cover:
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

## Cross-repository security / launch blockers

### Public source environment hygiene

Tracked environment-configuration paths remain in the public source tree.

Current project rules do not authorize reading or modifying .env files. Secret values are not copied into public review documents.

See architecture Issue #1.

### Production dependency security

Source default-branch Dependabot snapshot after merged source PR #25:
- 113 open alerts;
- Critical: 0;
- High: 44;
- Moderate: 59;
- Low: 10.

The former Critical Laravel Reverb advisory was removed by source PR #25:
https://github.com/gufyhvvyfycyddy-code/LinguaCafe-local/pull/25

The remaining dependency debt is still a launch-readiness problem. It must be triaged by shipped-path reachability and compatibility rather than bulk-upgraded.

See architecture Issue #23.

### Browser / platform evidence

- Web/PC needs a current live browser regression on the frozen source baseline.
- Android still needs current release artifact/signing/device/Play evidence.
- iOS still needs reproducible fresh-checkout preparation plus macOS/Xcode/signing/device/TestFlight/App Store evidence.

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

The next product milestone should be real-user evidence, not a large new feature surface.
