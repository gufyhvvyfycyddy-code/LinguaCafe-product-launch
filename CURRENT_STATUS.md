# Current Status — 2026-09-07

## Source baseline

- Frozen application-code review baseline: `6989ed27c933716f9069bb9b14fba92624081fc4`
- Source PR #26 merged the reproducible Web build and native `fsrs-rs-php` production-image fix.
- Post-baseline current-source fixes include PR #30 (reproducible Python tokenizer image), PR #31 (registration password-confirmation validation), PR #32 (targeted browser runtime dependencies), PR #33 (compatible PHP security refresh), PR #34/#35 (publication synchronization), PR #36/#37 (tokenizer/IIS CodeQL remediation), PR #39 (unused Vue3 experiment removal), and PR #40 (BrowserSync 3 development-tool update).
- Current product-review status is synchronized through source merge commit `2abc82df754525c19733382200aaf72a930d436a`.
- Architecture dependency P0 Issue #23 and security Issues #25/#26/#28/#29 are resolved.

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

Current default-branch Dependabot snapshot after source PR #40:
- 28 open alerts;
- Critical: 0;
- High: 6;
- Medium: 18;
- Low: 4.

Manifest split:
- root `package-lock.json`: 24;
- `composer.lock`: 2;
- `docker/python/requirements.lock.txt`: 1;
- `mobile/package-lock.json`: 1;
- the unused experimental Vue3 manifest was removed by source PR #39.

Source PR #33 reduced compatible PHP advisories while preserving current behavior (Unit 745/745; Feature 2882/2882). Source PR #40 removed the old BrowserSync/localtunnel axios chain. Current CodeQL has 0 open alerts.

Architecture Issue #23 is closed because all six remaining High alerts now have an explicit current non-reachability, accepted development-tool risk, or future upgrade gate in the architecture review's `DEPENDENCY_HIGH_RISK_DISPOSITION_2026-09-07.md`. Medium/Low debt and planned Laravel 12 / Vue3-Vuetify3 modernization remain visible follow-up work.

### Browser / platform evidence

- Web/PC current-baseline live browser evidence exists for the core Reader → WordSense → sense Review chain and adjacent Home/Library/Vocabulary/Settings routes. This does not prove every admin/destructive path or a public production deployment.
- Python tokenizer clean-build reproducibility is resolved post-baseline by source PR #30; see closed architecture Issue #25.
- Registration password-confirmation validation synchronization is resolved post-baseline by source PR #31; see closed architecture Issue #26.
- Current default-branch CodeQL has 0 open alerts after source PR #36/#37 and subsequent default-branch analysis.
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
