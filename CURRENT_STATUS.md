# Current Status — 2026-09-07

## Source baseline

- Frozen application-code review baseline: `6989ed27c933716f9069bb9b14fba92624081fc4`
- Source PR #26 merged the reproducible Web build and native `fsrs-rs-php` production-image fix.
- Post-baseline current-source fixes include PR #30 (reproducible Python tokenizer image), PR #31 (registration password-confirmation validation synchronization), PR #32 (targeted axios + moment runtime dependency updates), and PR #34 (publication-state documentation). Current source publication sync is represented by merge commit `abba49dd9723170d861839b478dad9224505ea8c`.
- Architecture Issues #25 and #26 are resolved by source PR #30 and PR #31 respectively.

## Product

Current direction:
- English reading-first learning;
- concrete WordSense as learning content;
- sense-level ReviewCard + FSRS as formal scheduling;
- source occurrence retained as learning evidence;
- AI for explanation/translation/candidate/disambiguation;
- daily experience moving toward a simpler MaiMemo-like information hierarchy without copying its vocabulary or business model.

## Release

- Web/PC: most complete implementation; current-baseline real Chrome acceptance is recorded for login, Home, Library/import, Reader, dictionary lookup, WordSense creation, Vocabulary, sense Review and Settings. The final production Web image loaded native `fsrs-rs-php`; interval preview and rating returned HTTP 200 with exactly one ReviewLog for the final smoke card.
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

Source default-branch Dependabot snapshot after merged source PR #26:
- 137 open alerts;
- Critical: 0;
- High: 48;
- Medium: 73;
- Low: 16.

Manifest split:
- root package-lock.json: 46;
- composer.lock: 49;
- experimental resources/vue3/package-lock.json: 41;
- mobile/package-lock.json: 1.

The increase from 113 to 137 follows the addition of the root package lock, which exposes the previously unlocked root frontend dependency graph to Dependabot. It is increased visibility, not proof that PR #26 introduced 24 new exploitable runtime vulnerabilities.

The former Critical Laravel Reverb advisory was removed by source PR #25:
https://github.com/gufyhvvyfycyddy-code/LinguaCafe-local/pull/25

The remaining dependency debt is still a launch-readiness problem. It must be triaged by shipped-path reachability and compatibility rather than bulk-upgraded.

See architecture Issue #23.

### Browser / platform evidence

- Web/PC current-baseline live browser evidence exists for the core Reader → WordSense → sense Review chain and adjacent Home/Library/Vocabulary/Settings routes. This does not prove every admin/destructive path or a public production deployment.
- Python tokenizer clean-build reproducibility is resolved post-baseline by source PR #30; see closed architecture Issue #25.
- Registration password-confirmation validation synchronization is resolved post-baseline by source PR #31; see closed architecture Issue #26.
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
