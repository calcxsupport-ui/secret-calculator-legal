# App Store Connect checklist

## URLs to paste

| Field | Value |
|-------|--------|
| Privacy Policy URL | `https://calcxsupport-ui.github.io/secret-calculator-legal/privacy.html` |
| Terms of Use (optional / custom EULA) | `https://calcxsupport-ui.github.io/secret-calculator-legal/terms.html` |
| Support URL (optional) | `https://calcxsupport-ui.github.io/secret-calculator-legal/` |
| Support / Marketing email | `calcxsupport@gmail.com` |

Path in Connect:

1. **App Information** → Privacy Policy URL → paste privacy URL.
2. License Agreement → Apple’s Standard EULA **or** custom EULA URL pointing at terms.html.
3. **App Privacy** → answer the questionnaire.

## App Privacy (nutrition labels) — current local-only build

Until you add RevenueCat, analytics, crash reporters, or any SDK that sends data off-device:

1. Open **App Privacy** for Secret Calculator.
2. Choose that you do **not** collect data (or equivalent: **Data Not Collected**), if accurate for this build.
3. Do **not** list vault photos, PIN, or Face ID as “collected” if they never leave the device / Apple’s on-device biometric APIs and are not transmitted to you or a third party.

Permissions still shown to the user at runtime (Camera, Face ID, Photos) are separate from “data collection” in the nutrition labels. Document them honestly in the Privacy Policy (already done).

## After GitHub Pages is live

1. Open privacy.html and terms.html in Safari — confirm HTTPS loads (no 404).
2. In the iOS app: Settings → Privacy Policy / Terms of Use / Contact Support.
3. Submit or update the App Store listing with the Privacy Policy URL above.

## When you add RevenueCat / IAP later

1. Update `privacy.html` with a Purchases / third-party section.
2. Revisit **App Privacy** and declare identifiers / purchase history as required by RevenueCat’s guidance.
3. Bump “Last updated” on the policy page and redeploy Pages.
