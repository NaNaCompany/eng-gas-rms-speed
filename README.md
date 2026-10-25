# 기체 분자 RMS 속력 계산기

이상기체 분자 병진운동의 RMS 속력 계산

- Plan ID: E060
- App: https://nanalab.kr/eng-gas-rms-speed/
- Repository: https://github.com/NaNaCompany/eng-gas-rms-speed
- Formula: `v_rms = √(3RT/M)`
- Output: 제곱평균제곱근 속력 v_rms

## Model

T,M>0. 열평형 이상기체의 비상대론 병진운동 모델이다. 평균 속력·최빈 속력과 구분한다. 혼합기체 전체에 임의의 몰질량을 넣지 않는다.

Inputs are normalized to SI. Only one scalar is returned. Model conditions, finite numbers, physical boundaries, overflow and underflow are checked. External solver APIs and property databases are not used.

## Verification

Run `node --test tests/*.test.mjs` with Node.js 22 or later. Independent 70-digit Decimal example result: `508.234449836508`. Source and license notices are in [SOURCES.md](SOURCES.md) and [LICENSE](LICENSE).

## Hosting

GitHub Pages uses `main` and `/`, with the NaNaCompany domain inherited. Google GTM, GA4, AdSense, Cloudflare analytics and the gray More Apps link are included. All code, descriptions and graphics are original.

## Static languages

Korean (existing root), English (`en/`), Spanish (`es/`), Simplified Chinese (`zh/`), Japanese (`ja/`) and German (`de/`). Each page has its own canonical URL, reciprocal hreflang, localized metadata, interface, validation messages and preview image. The language links work without JavaScript. Calculation code is shared and no runtime translation API is used.

Edit `localization/*.json` for text, `src/template.html` for the shared page, and run `python scripts/build-locales.py`. Run `python scripts/build-locales.py --check` and `npm test` before publishing. Decimal commas are accepted in Spanish and German; thousands separators are not supported.
