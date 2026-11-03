# PolliGen Studio

**PolliGen Studio** is a multimodal generative AI application designed to fulfill the requirements of the **Pollinations App Directory Catalog** (`operations/app-management/app.json`) and build verifiable user engagement.

[![Made with pollinations.ai](https://raw.githubusercontent.com/pollinations/pollinations/main/packages/ui/src/brand/badge-made-with.svg)](https://pollinations.ai/?ref=badge)

---

## Capabilities & Architecture
1. **Intelligent Prompt Synthesizer**: Connects to Pollinations chat completion models (`gen.pollinations.ai/v1`) to expand base concepts into high-detail artistic prompts (lighting, composition, mood, style tokens).
2. **Dynamic Image Rendering**: Queries the Pollinations Image Generation API (`image.pollinations.ai/prompt/...`) utilizing models such as `flux` and `turbo`.
3. **Resilient Local Mode**: Works with deterministic prompt expansion if the network is disconnected, ensuring robust local testing.
4. **App Catalog Compliant**: Contains verified metadata formatted strictly according to Pollinations `operations/app-management/app.json` and `AGENTS.md`.

---

## Verification & Audit Findings
- **Quest Mapping Audit**: PolliGen Studio is a general creative web tool, **not** associated with the Unity package bounty (`#15580`). Its `quest` field is properly set to `null` to prevent submission rejection.
- **Badge Requirement**: Official badge (`https://pollinations.ai/badges/badge-made-with.svg`) is embedded in both the web interface (`index.html`) and this README.
- **Deployment & Screenshot**: For final catalog submission, deploy the web app to a public host (e.g., GitHub Pages, Cloudflare Pages, or Vercel) and capture a 16:9 WebP/PNG screenshot ($\ge 1280\times 720$).

---

## Local Testing & Execution

### 1. Run Schema Validator
```bash
node src/appValidator.js
```

### 2. Start Local Web Interface
```bash
node src/demo_app/server.js
```
Open `http://localhost:3000` in your browser.

---

## Submission Guide via GitHub Issues
1. Open the [Pollinations App Submission Template](https://github.com/pollinations/pollinations/issues/new?template=app-submission.yml).
2. Title: `[APP-SUBMISSION] PolliGen Studio`.
3. Provide the fields from `app_metadata.json` (leaving Quest blank or null).
4. Attach the 16:9 screenshot.
5. Once approved by maintainers with `APP-APPROVED`, the app is automatically merged into the catalog.
