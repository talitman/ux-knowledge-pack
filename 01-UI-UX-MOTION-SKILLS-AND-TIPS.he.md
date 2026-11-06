# שדרוג UI/UX, מושן ופוליש לאפליקציה קיימת: כל מה שיש ב-KB

> הוכן ב-18.10.2026 מתוך ה-KB ב-`/workspace/ai-knowledge/kb/` (1,060 פריטים). המטרה: לשפר את המראה והתחושה של אפליקציית הווב הקיימת של דותן (ובהמשך גם המובייל): פוליש, אינפוטים וטפסים טובים יותר, אנימציות ומיקרו-אינטראקציות. לא פיצ'רים חדשים.
>
> **איך נבנה:** עברתי על כל 1,060 הפריטים לפי frontmatter (category, tags, tools, gist) ועם חיפוש `rg` על המונחים UI, UX, animation, motion, GSAP, Lottie, Rive, Framer, shadcn, Tailwind, component, design system, input, form, Expo, React Native, SwiftUI, Flutter, Figma, landing page, 21st.dev, Magic UI, Aceternity ועוד. סיננתי ידנית כ-230 מועמדים וקראתי את המלאים, וגם את ה-notes והתמלולים של הפריטים המרכזיים. נשארו כ-120 פריטים רלוונטיים.
>
> **סימונים:**
> - 🌐 = פרט שאימתתי ברשת היום (פקודת התקנה, ריפו, מחיר) כי בפריט עצמו הוא חסר או נשלח רק למי שמגיב. זה לא מתוך ה-KB.
> - ⚠️ = הסתייגות: הפריט דל, הקישור gated (נשלח רק למי שמגיב), או שהשם לא ודאי.
> - ⭐ = אחד מ-10 הבחירות המובילות (ראו בסוף).
> - "נתיב" = הקובץ המלא של הפריט ב-KB.
>
> **פערים ב-KB שכדאי לדעת עליהם:** אין פריטים על Lottie, Rive, Framer Motion/Motion, Aceternity, Magic UI (חוץ מאזכור אחד), SwiftUI או Mobbin. אין גם פריט ייעודי לספריות טפסים (react-hook-form, Zod וכו'). נושא האינפוטים מכוסה רק בעקיפין, דרך skills ו-guidelines (ראו פרק 5).

## סיכום כמותי לפי נושא

| נושא | רשומות (כותרות) | מזהי פריטים שמוזכרים |
|---|---|---|
| 1. סקילים וכללי עיצוב לסוכני קוד (Claude Code, Cursor, Codex) | 7 | 13 |
| 2. Design systems, טוקנים ו-DESIGN.md | 6 | 12 |
| 3. ספריות קומפוננטות ו-UI מוכן | 6 | 11 |
| 4. אנימציה, מושן ו-3D | 11 | 22 |
| 5. אינפוטים, טפסים ומיקרו-אינטראקציות | 7 | 8 |
| 6. השראה ורפרנסים | 8 | 11 |
| 7. מעיצוב לקוד: Figma וכלי עיצוב AI | 12 | 24 |
| 8. מובייל | 12 | 14 |
| 9. וורקפלואים ופרומפטים שמייצרים UI טוב יותר | 7 | 10 |
| 10. אודיט, ביקורת ו-QA ויזואלי | 8 | 15 |
| 11. Generative UI (שוליים, לא פוליש) | 4 | 6 |

בסך הכל מוזכרים במסמך 117 פריטים ייחודיים מה-KB. פריט יכול להופיע ביותר מנושא אחד דרך הפניות.

---

## תוכן עניינים
1. סקילים וכללי עיצוב לסוכני קוד
2. Design systems, טוקנים ו-DESIGN.md
3. ספריות קומפוננטות ו-UI מוכן
4. אנימציה, מושן ו-3D
5. אינפוטים, טפסים ומיקרו-אינטראקציות
6. השראה ורפרנסים
7. מעיצוב לקוד: Figma וכלי עיצוב AI
8. מובייל
9. וורקפלואים ופרומפטים שמייצרים UI טוב יותר
10. אודיט, ביקורת ו-QA ויזואלי
11. Generative UI (שוליים, לא פוליש)
12. איפה להתחיל: 10 הבחירות המובילות וסדר יישום

---

## 1. סקילים וכללי עיצוב לסוכני קוד (Claude Code, Cursor, Codex)

### ⭐ Impeccable: "אוצר מילים עיצובי" לסוכנים ו-detector נגד AI slop
- **A0823** · [קישור למקור](https://impeccable.style/) · נתיב: `/workspace/ai-knowledge/kb/items/A0823.md`
- **פריטים קשורים:** A0995 (Impeccable ו-Taste 2.0, "שני הסקילים היחידים שצריך"), A0841 (חמישה סקילים), A1100 (עורך חי), A1000 ו-A1104 (המתכון המלא).
- **מה זה:** skill בקוד פתוח מאת Paul Bakaus (github.com/pbakaus/impeccable). הוא נותן לסוכן מומחיות עיצובית בשלושה מצבים: בנייה מאפס, שיפור של משהו קיים, ושמירה על design system. יש לו detector שבודק 59 (או לפי מקורות אחרים 24, 40+) "AI tells", למשל AI beige, italic serif, side-tab ו-pulsing dot. בנוסף: Live Mode שמזריק picker לאפליקציה שרצה ב-localhost, "Explore directions" עם חוקים ויזואליים, CLI ל-PR checks שמחזיר exit codes, ותוסף Chrome.
- **איך זה עוזר לפוליש:** זה הכלי הכי מתאים לאפליקציה **קיימת**. הוא קורא את ה-DESIGN.md שלכם, מוצא את מה שמסגיר "נבנה ב-AI", מתקן, ומריץ שוב את ה-detector עד שלא נשארים ממצאים. הוא לא מכתיב סגנון (A0995), ולכן לא ימחק את הזהות של האפליקציה.
- **פקודה מהפריט (מילה במילה):**
```text
/impeccable polish the pricing page. Keep our sharp corners and sober palette. Remove the AI tells.
```
- 🌐 **התקנה ופקודות:** `npx impeccable install` משורש הפרויקט, ואז `/impeccable init`. פקודות: `audit`, `polish`, `critique`, `shape`, `document`, `extract`, `live`, `generate`. עדכון: `npx impeccable update`.
- **עלות/רישיון:** חינם, קוד פתוח.

### ⭐ הסקילים של Emil Kowalski: אנימציה ופוליש "ברמת Vercel/Linear"
- **A1000** · [קישור למקור](https://www.instagram.com/reel/DbLuwUVlE9Z/?igsh=cHUydG56aHR2a2t3) · נתיב: `/workspace/ai-knowledge/kb/items/A1000.md`
- **פריטים קשורים:** A1104 (אותו מתכון בגרסה חוזרת).
- **מה זה (לפי הפריט):** המתכון של Nate Herk: (1) מתקינים את הסקילים של Emil Kowalski ושל Impeccable, שמלמדים layout, טיפוגרפיה, ריווח ואנימציות; (2) מוסיפים את Taste בשביל השראה מאתרים אמיתיים; (3) מחברים Figma MCP ו-Playwright כדי שהסוכן יעצב, יבנה ויבדוק לבד; (4) מתארים את האתר. ⚠️ ה-setup המלא נשלח רק למי שמגיב.
- 🌐 **מה יש בריפו** (`npx skills@latest add emilkowalski/skills`, github.com/emilkowalski/skills):
  - `emil-design-eng`: הסקיל הראשי, בעיקר אנימציה ועוד עצות עיצוב.
  - `animate`: בונה אנימציה ובוחר easing, משך ומאפיינים. הוא מתחיל בשאלה אם בכלל צריך להנפיש: דברים שנפתחים יותר מ-100 פעם ביום לא מקבלים אנימציה. עובד רק עם transform/opacity, וכולל reduced-motion.
  - `review-animations`, `improve-animations` (אודיט של כל האנימציות בקוד, עם תוכניות מתועדפות), `find-animation-opportunities`.
  - `mobile-native`: גורם לאפליקציית ווב להרגיש native בטלפון. מטפל ב-hover דביק, tap highlight, באג 100vh, **inputs שמזיזים את הדף בזום**, safe areas.
  - `break-ui`: שובר את ה-UI עם דאטה קיצוני (שמות ארוכים, רשימות ריקות, מספרים ענקיים).
  - `animate-expo` (React Native/Expo), `apple-design`, `pick-ui-library`, `prototype` (כמה גרסאות עם מתג החלפה), `ask-sonner` (toasts).
- **איך זה עוזר:** זה בדיוק הפער שדותן מתאר, "חסרות אנימציות ותחושה". `improve-animations` ו-`find-animation-opportunities` מתאימים לאפליקציה קיימת, ו-`mobile-native` ו-`break-ui` משפרים אינפוטים ומצבי קצה.
- **עלות:** חינם.

### ⭐ Taste skill: "טעם" עיצובי ו-art direction
- **A0995** · [קישור למקור](https://www.instagram.com/reel/DbJvV3BpnO6/?igsh=MTUyeHA3cmxoaGduNg==) · נתיב: `/workspace/ai-knowledge/kb/items/A0995.md`
- **פריטים קשורים:** A1113 ("נגד עוד גרדיאנט סגול עם שלושה כרטיסים מעוגלים"), A0841 (Leonxlnx/taste-skill: פריסה, טיפוגרפיה, צבע ותנועה), A1000.
- **מה זה:** skill בקוד פתוח שמזהה דפוסי AI slop ומכוון למשהו אחר. גרסה 2.0 שודרגה. כמו Impeccable, הוא לא prescriptive.
- 🌐 **התקנה:** `npx skills add https://github.com/Leonxlnx/taste-skill --skill "design-taste-frontend"`, או ב-Claude Code: `/plugin marketplace add Leonxlnx/taste-skill`. גרסה 2 נותנת art direction, מוצאת תמונות אמיתיות ובודקת את התוצאה בדפדפן אמיתי. צריך Node 22+ ו-Chrome. מכוונת בעיקר לדפי נחיתה, שיווק ודפי מוצר.
- **איך זה עוזר:** מתאים למסכים "החלונות הראווה" של האפליקציה, כמו דף הבית, onboarding ו-pricing. למסכי עבודה פנימיים Impeccable ו-Emil מתאימים יותר.
- **עלות:** חינם, בלי API keys.

### ⭐ UI UX Pro Max ו-21st.dev Magic MCP: "אתרים ברמת סטודיו"
- **A0793** · [קישור למקור](https://www.instagram.com/reel/DX1sIR7tZhl/?igsh=Y3hzaDdwbzlqbnZn) · נתיב: `/workspace/ai-knowledge/kb/items/A0793.md`
- **פריטים קשורים:** A0841 (50+ סגנונות, 161 פלטות, 99 חוקי UX), A0827 (ui-ux-pro-max: 50 סגנונות, 97 פלטות, 57 זיווגי פונטים, 9 סטאקים).
- **מה זה:** שלושה צעדים (איילון גרופר, בעברית): (1) מחפשים בגוגל את הסקיל UI UX Pro Max ומבקשים מ-Claude להתקין; (2) ב-21st.dev, ב-Magic Chat, מעתיקים את פקודת ה-MCP ומבקשים מ-Claude להתקין; (3) מבקשים אתר. **"אפשר גם לשפר ולערוך אתרים קיימים בשיטה הזאת."**
- 🌐 **פרטים:** github.com/nextlevelbuilder/ui-ux-pro-max-skill (MIT). התקנה: `npm install -g ui-ux-pro-max-cli`, ואז `uipro init --ai claude` (או cursor/codex וכו'). ב-Claude Code אפשר גם `/plugin marketplace add nextlevelbuilder/ui-ux-pro-max-skill`. בגרסה 2 יש **Design System Generator**, 119 הנחיות UX (כולל נגישות ואינטראקציות שאפשר לבטל), 17 presets של GSAP, ו-22 סטאקים, כולל React Native, SwiftUI, Flutter ו-shadcn/ui.
- **איך זה עוזר:** מייצר design system מלא (פלטה, פונטים, סגנון) שמותאם לסוג המוצר. זו נקודת פתיחה טובה ל-DESIGN.md, וזה עובד גם על ווב וגם על מובייל.
- **עלות:** חינם (MIT).

### ui-skills.com: דירקטורי של 109 סקילים עיצוביים, ואזהרת אמון
- **A0827** · [קישור למקור](https://www.linkedin.com/posts/eliron-giny-10056b173_%D7%9E%D7%99%D7%A9%D7%94%D7%95-%D7%9C%D7%A7%D7%97-%D7%90%D7%AA-%D7%9B%D7%9C-%D7%94%D7%A1%D7%A7%D7%99%D7%9C%D7%99%D7%9D-%D7%94%D7%A2%D7%99%D7%A6%D7%95%D7%91%D7%99%D7%99%D7%9D-%D7%A9%D7%9E%D7%A1%D7%AA%D7%95%D7%91%D7%91%D7%99%D7%9D-ugcPost-7459673468373151744-aPXf?utm_source=social_share_send&utm_medium=ios_app&rcm=ACoAAA_213gBhne8kHAuy6uPpgS0pHU7NBiWdLk&utm_campaign=copy_link) · נתיב: `/workspace/ai-knowledge/kb/items/A0827.md`
- **מה זה:** 109 סקילים חינמיים, מסווגים לנגישות, מוטיון, מערכות, ויז'ואל, אינטראקציה, ביצועים וקראפט. בולטים: ui-ux-pro-max, remotion-best-practices, ו-**redesign-skill**, ששדרג UI קיים בלי לשבור אותו.
- **איך זה עוזר:** מקום לחפש סקיל ממוקד (למשל רק לנגישות או רק לטפסים).
- **⚠️ אבטחה (חשוב):** "התקנת skill היא הענקת אמון". skill מריץ הוראות בשמכם (קבצים, טרמינל, MCP). סימנים מחשידים: מקור אנונימי, ריפו טרי בלי כוכבים, הרשאות רחבות. כלל: לקרוא את SKILL.md לפני שמפעילים. ראו Snyk Agent Scan ([A0670](kb/items/A0670.md)).

### "24 תוספים ל-Claude": Frontend Design ו-Agent Browser
- **A1009** · [קישור למקור](https://docs.google.com/document/d/1haM-Y4CwSKoWDoUf0MlrSiA924l1PFq9LOgC0Xz-j6k/edit?usp=drivesdk) · נתיב: `/workspace/ai-knowledge/kb/items/A1009.md`
- **מה זה:** מדריך התקנה (Google Doc). בקבוצת ההנדסה: **Frontend Design** (מ-`anthropics/skills`), Agent Browser (`npx skills add vercel-labs/agent-browser`), gstack ו-Superpowers.
- **איך זה עוזר:** Frontend Design הוא הסקיל הרשמי של Anthropic לעיצוב פרונטאנד. זו חלופה או השלמה "רשמית" לסקילים הקהילתיים.
- **טעויות נפוצות לפי המדריך:** להתקין הכל בבת אחת, ולהתקין כלים לא מוכרים.
- **עלות:** חינם.

### Claude Skills ל-brand guidelines
- **A0533** · [קישור למקור](https://www.instagram.com/reel/DQMBUePjHSa/?igsh=ajk3am1iMTRmaHdr) · נתיב: `/workspace/ai-knowledge/kb/items/A0533.md`
- **פריטים קשורים:** A0529.
- **מה זה:** skill הוא תיקייה עם הנחיות, קוד וחומרי עזר. הדרך הקלה ליצור אחד: מבקשים מ-Claude "לפתוח skill חדש", והוא שואל שאלות מנחות ומייצר את הקובץ. בדוגמה: skill של הנחיות מותג.
- **איך זה עוזר:** אפשר לארוז את כללי העיצוב של האפליקציה (טוקנים, מה כן ומה לא) כ-skill פרטי, כך שכל סשן של סוכן יכבד אותם.

---

## 2. Design systems, טוקנים ו-DESIGN.md

### ⭐ DESIGN.md של Google: "החוזה" בין ה-design system לסוכני הקוד
- **A0765** · [קישור למקור](https://www.linkedin.com/posts/oren-grinker-374912166_1a1c1e-share-7452762831097249792-CoG5?utm_source=social_share_send&utm_medium=ios_app&rcm=ACoAAA_213gBhne8kHAuy6uPpgS0pHU7NBiWdLk&utm_campaign=copy_link) · נתיב: `/workspace/ai-knowledge/kb/items/A0765.md`
- **מה זה:** כמו CLAUDE.md או AGENTS.md, אבל לעיצוב. יש לו שתי שכבות: YAML front matter עם טוקנים (צבעים, טיפוגרפיה, ריווח; תואם W3C DTCG, עם ייצוא ל-Tailwind) וגוף markdown שמסביר את ה"למה". דוגמה מהפריט: `primary: "#1A1C1E"` יחד עם "deep ink for headlines, editorial austerity". יש CLI: `lint` לניגודיות WCAG AA, `diff` לרגרסיות בטוקנים, ו-`tailwind` שמייצר theme.extend.
- **איך זה עוזר:** זה הבסיס לכל השאר. Impeccable, Stitch וכלים אחרים קוראים את הקובץ. בלעדיו כל סשן של סוכן "ממציא" עיצוב מחדש.
- **מה עוד לא סגור:** אנימציות, dark mode ו-breakpoints. ⚠️ אלפא.
- **עלות/רישיון:** Apache 2.0.

### awesome-design.md של VoltAgent: קובצי DESIGN.md להעתקה
- **A0887** · [קישור למקור](https://www.instagram.com/reel/DY7kuBOD30E/) · נתיב: `/workspace/ai-knowledge/kb/items/A0887.md`
- **פריטים קשורים:** A0780 (getdesign.md: Ferrari, IBM, Linear ועוד), A1100 ו-A1113 ("Awesome Design").
- **מה זה:** ריפו עם 66 אלף כוכבים של קובצי DESIGN.md בהשראת אתרים אמיתיים: טיפוגרפיה, צבעים, ריווח, כפתורים, טפסים ו-layouts. מעתיקים לפרויקט ואומרים לסוכן:
```text
build me a page that looks like this
```
- **איך זה עוזר:** במקום להתחיל DESIGN.md מאפס, לוקחים קובץ של מותג עם "וייב" דומה (למשל Linear לאפליקציית SaaS) ומתאימים אותו.
- **⚠️ זכויות:** שימוש בשפת עיצוב של מותג מסחרי עלול להפר זכויות. עדיף להשתמש בזה כהשראה ולא כהעתק (A0780).
- **עלות:** חינם.

### "קובץ טעם" (design.md): הצעד שכולם מדלגים עליו
- **A0959** · [קישור למקור](https://www.instagram.com/reel/DayC1EszldL/?igsh=ajBieHNuemQ0eWxo) · נתיב: `/workspace/ai-knowledge/kb/items/A0959.md`
- **מה זה:** ארבעה שלבים: (1) Claude Code (מנוי בתשלום); (2) **קובץ אחד עם הטעם שלכם**: צבעים, ריווח, פונטים, תחושה. דוגמה מהפריט: פונט Inter, רקע warm ivory, מצב רוח premium; (3) פרומפט בנייה שמבקש "real animations"; (4) איטרציה בשפה רגילה.
- **ניסוחי איטרציה מהפריט (מילה במילה):**
```text
Bigger hero
slow that scroll down
this feels cramped
```
- **הסתייגות של היוצרת:** "נקודת פתיחה שאפשר לשלוח לאוויר, לא מוצר סופי". ⚠️ ה-template המלא gated.

### Claude Design: קודם design system, אחר כך כל השאר
- **A0909** · [קישור למקור](https://youtu.be/ovabeVoWrA0?si=aP0JiICwYjBAS7jJ) · נתיב: `/workspace/ai-knowledge/kb/items/A0909.md`
- **פריטים קשורים:** A0926 (אחרי מתיחת הפנים: אנימציות, מצגות ואתרים לפי ה-design system, וייצוא ל-Claude Code), A0782 (תבניות מייל מאותו design system).
- **מה זה:** קורס של שעתיים (Nate Herk) על Claude Design, אפליקציה נפרדת של Anthropic (claude.ai/design). בונים design system (לוגו, טיפוגרפיה, צבעים, ריווח, רכיבים), אחר כך wireframe, אתר hi-fi ו**אב-טיפוס מובייל** (57:51 בסרטון), ומייצאים ל-Claude Code.
- **טיפים לפרומפטים מהקורס:**
  - שינוי גדול אחד בכל פרומפט, כי בבקשה מרובה רק שינוי או שניים מתבצעים טוב.
  - לכתוב גם מה לא רוצים.
  - להפנות לרפרנסים אמיתיים ("Linear 2023 בצפיפות גבוהה") במקום "נקי" או "מינימליסטי".
  - לסמן ולצייר על הקנבס.
  - תיקונים קטנים עושים ידנית אחרי הייצוא.
  - **למותג קיים מספיק לתת לוגו, ריפו GitHub וכתובת אתר**, וזה מייצר design system מהאפליקציה הקיימת.
- **עלות:** דורש מנוי בתשלום (Pro, Max, Team או Enterprise), ויש מכסה שבועית נפרדת. ⚠️ research preview.

### Open Design: חלופה פתוחה ל-Claude Design
- **A0804** · [קישור למקור](https://www.linkedin.com/posts/asafrozanes_achacpacwackacuacsacgacracladgacpadg-addaclacjadaadgaclacn-share-7457648347613556737-mVqG?utm_source=share&utm_medium=member_ios&rcm=ACoAAA_213gBhne8kHAuy6uPpgS0pHU7NBiWdLk) · נתיב: `/workspace/ai-knowledge/kb/items/A0804.md`
- **פריטים קשורים:** A1116 (259 סקילים ו-142 מערכות עיצוב).
- **מה זה:** כלי open source שהופך כל סוכן קוד ב-CLI (מזהה 13 סוגים) למנוע עיצוב. כולל 72 design systems (או 142 לפי A1116), local-first, BYOK ופריסה ל-Vercel.
- **איך זה עוזר:** עובד עם הסוכן שכבר יש לכם, בלי מכסה של Claude Design.
- **עלות:** חינם. ⚠️ A1116 טוען שזה של Claude, וזה כנראה לא מדויק (פרויקט קהילתי).

### מצגות ונכסים ב-HTML לפי Brand Guidelines
- **A0505** · [קישור למקור](https://www.linkedin.com/posts/ron-izraeli_%D7%A2%D7%A6%D7%A8%D7%95-%D7%94%D7%9B%D7%9C-%D7%9E%D7%A6%D7%90%D7%AA%D7%99-%D7%90%D7%AA-%D7%94%D7%9B%D7%9C%D7%99-%D7%94%D7%9E%D7%95%D7%A9%D7%9C%D7%9D-%D7%9C%D7%99%D7%A6%D7%99%D7%A8%D7%AA-%D7%9E%D7%A6%D7%92%D7%95%D7%AA-ugcPost-7371820421047816192-pBLx?utm_source=share&utm_medium=member_desktop&rcm=ACoAAA_213gBhne8kHAuy6uPpgS0pHU7NBiWdLk) · נתיב: `/workspace/ai-knowledge/kb/items/A0505.md`
- **מה זה:** מכניסים את ה-Brand Guidelines ל-Claude Project משותף ומקבלים תוצרים ממותגים ב-HTML/CSS/JS.
- **איך זה עוזר:** שימושי בעקיפין: אותו Project ממותג משמש גם לנכסים סביב האפליקציה (מיילים, דפי נחיתה).

---

## 3. ספריות קומפוננטות ו-UI מוכן

### ⭐ shadcn/ui: הבסיס של רוב כלי ה-AI
- **A0018** · [קישור למקור](https://ui.shadcn.com/docs/components/) · נתיב: `/workspace/ai-knowledge/kb/items/A0018.md`
- **מה זה:** קומפוננטות React ו-Tailwind ש**מועתקות** לפרויקט, לא מותקנות כתלות npm, ולכן אפשר לשנות בהן הכל. v0, Lovable ו-Bolt מייצרים UI על בסיס shadcn. יש registry directory לקומפוננטות קהילה.
- **איך זה עוזר:** אם האפליקציה בנויה ב-React, כדאי לאחד את כל האינפוטים, הדיאלוגים, הטבלאות וה-toasts לקומפוננטות אחידות של shadcn, ואז לשנות את ה-theme במקום אחד. ב-A0359, Cursor ניצח בהשוואה בין סוכנים כי "היחיד שבאמת השתמש ב-shadcn שהיה מותקן".
- **עלות/רישיון:** חינם, open source.

### Tailwind ו-shadcn: לתת ל-AI קטלוג במקום לנחש
- **A0151** · [קישור למקור](https://www.linkedin.com/posts/%F0%9F%8E%97%EF%B8%8Fyuval-avidani-87081474_%D7%94%D7%9B%D7%99%D7%A8%D7%95-%D7%90%D7%AA-tailwind-%D7%95-shadcn-%D7%A9%D7%A0%D7%99-%D7%9B%D7%9C%D7%99%D7%9D-%D7%A9%D7%99%D7%A2%D7%96%D7%A8%D7%95-activity-7303362264055607297-bTyO?utm_medium=ios_app&rcm=ACoAAA_213gBhne8kHAuy6uPpgS0pHU7NBiWdLk&utm_source=social_share_video_v2&utm_campaign=copy_link) · נתיב: `/workspace/ai-knowledge/kb/items/A0151.md`
- **מה זה:** במקום "לריב עם ה-AI על עיצוב", בוחרים רכיב מהקטלוג ומדביקים לסוכן את פקודת ההתקנה ואת הקוד, עם הוראה להשתמש בו.
- **מלכודת (מהפריט):** הסוכן כותב לפעמים `shadcn-ui` (החבילה הישנה) ונתקע בבאגים. צריך לתת לו את הפקודה המדויקת:
```text
npx shadcn@latest add ...
```

### ⭐ 21st.dev ו-21st MCP (לשעבר Magic MCP)
- **A0691** · [קישור למקור](https://github.com/21st-dev/magic-mcp) · נתיב: `/workspace/ai-knowledge/kb/items/A0691.md`
- **פריטים קשורים:** A0172 (הקטלוג), A0551 (שלושה MCPs מומלצים), A0793.
- **מה זה:** קטלוג קהילתי של קומפוננטות React ו-Tailwind (hero, כפתורים, כרטיסים, **טפסים**, רקעים מונפשים, דפי נחיתה). לכל קומפוננטה יש תצוגה חיה, כפתור **"Copy prompt"** לכלי AI, קוד ופקודת CLI. ה-MCP נותן חיפוש ב-10,000+ קומפוננטות ויצירת UI חדש מתוך ה-IDE ("כמו v0 בתוך Cursor ו-Claude Code"). כלים: `search` ו-`generate`. Magic (`@21st-dev/magic`) הוחלף ב-21st MCP, עם setup ב-21st.dev/mcp.
- **איך זה עוזר:** מאפשר להחליף בלוק "גנרי" (hero, pricing, empty state, טופס) בקומפוננטה מלוטשת בלי לצאת מהעורך.
- **עלות:** חינם, ויש גרסת Pro.

### Animaster Live, Skiper UI ו-Vengeance UI: ספריות לאתרים מונפשים
- **A1012** · [קישור למקור](https://www.instagram.com/reel/DaDRFEezrOP/?igsh=MTZvY3V5Nm9tcGV3NQ==) · נתיב: `/workspace/ai-knowledge/kb/items/A1012.md`
- **מה זה:** Animaster Live: 250+ קומפוננטות מונפשות (אפקטי גלילה, hero, אינטראקציות עכבר, WebGL), להעתקה והדבקה. Skiper UI: hero, כרטיסים, עמודי מחירים. Vengeance UI: אנימציות ובלוקים מודרניים.
- **איך זה עוזר:** מתאים לדפי שיווק ולמסכי "וואו". למסכי עבודה עדיף לא להגזים.
- ⚠️ השמות לפי התמלול בלבד, והקישורים gated. צריך לחפש ולוודא.

### ספריית אנימציות, גרדיאנטים ורכיבים (כנראה React Bits)
- **A0603** · [קישור למקור](https://www.instagram.com/reel/DUplhdqAbNt/?igsh=MmJ4cHMxaTI3bjh1) · נתיב: `/workspace/ai-knowledge/kb/items/A0603.md`
- **מה זה:** גולשים בספרייה, מתאימים צבעים, מהירות ופריסה, מעתיקים קוד ו**אומרים לסוכן בדיוק איפה להוסיף**.
- ⚠️ שם הספרייה מוסתר. ייתכן React Bits (ראו A1008 בפרק 4).

### Magic UI כחבילת אנימציות בפרומפט
- **A0023** · [קישור למקור](https://www.linkedin.com/posts/%F0%9F%8E%97%EF%B8%8Fyuval-avidani-87081474_%D7%A7%D7%9C%D7%95%D7%93-%D7%95%D7%A7%D7%A8%D7%A1%D7%A8-%D7%90%D7%97%D7%93-%D7%91%D7%99%D7%95%D7%9D-%D7%91%D7%A8%D7%9B%D7%91%D7%AA-%D7%91%D7%95%D7%90%D7%95-%D7%AA%D7%A8%D7%90%D7%95-%D7%90%D7%99%D7%9A-activity-7265405743397289985-wIp8?utm_medium=ios_app&utm_source=social_share_video_v2&utm_campaign=copy_link) · נתיב: `/workspace/ai-knowledge/kb/items/A0023.md`
- **מה זה:** דמו בעברית: Cursor Composer בונה אתר אינטראקטיבי ומונפש מפרומפט בעברית, ו**מבקשים שישתמש ב-Magic UI** (חבילת אנימציות). זה האזכור היחיד של Magic UI ב-KB.
- **איך זה עוזר:** מראה שאפשר לבקש ספריית אנימציה ספציפית בשמה, ו-AI משתמש בה.

---

## 4. אנימציה, מושן ו-3D

### ⭐ GSAP Skills: הסקילים הרשמיים של צוות GSAP
- **A0794** · [קישור למקור](https://www.instagram.com/reel/DXKJ4NxDekW/?igsh=bzlwcTV6MzF3aXFy) · נתיב: `/workspace/ai-knowledge/kb/items/A0794.md`
- **מה זה:** בלי הכוונה, סוכנים מייצרים "מעברים בסיסיים ומגושמים". הריפו הרשמי כולל 8 מודולים: core, timeline, ScrollTrigger, plugins, utils, **React (useGSAP, cleanup, SSR)**, performance ו-frameworks. אחרי ההתקנה הסוכן "מפסיק לנחש ומתחיל לעקוב אחרי הדפוסים הרשמיים".
- 🌐 **התקנה:** `npx skills add https://github.com/greensock/gsap-skills`, או ב-Claude Code: `/plugin marketplace add greensock/gsap-skills`. **GSAP חינמי לגמרי, כולל כל הפלאגינים (SplitText, MorphSVG) ושימוש מסחרי** (מאז הרכישה של Webflow). הריפו ברישיון MIT.
- **איך זה עוזר:** ל-timelines, אנימציות כניסה, גלילה ו-stagger ברשימות. ב-React חשוב במיוחד ה-cleanup, כדי שלא יהיו דליפות.

### Lenis, GSAP, Vanta.js ו-React Bits: אנימציות UI חינמיות בגיטהאב
- **A1008** · [קישור למקור](https://www.instagram.com/reel/Da3O00jpo3R/?igsh=MWphYTN3OTU5ZXM4Mw==) · נתיב: `/workspace/ai-knowledge/kb/items/A1008.md`
- **מה זה:** Lenis (darkroomengineering/lenis) לגלילה חלקה. GSAP (greensock/GSAP). Vanta.js (tengbao/vanta) לרקעי WebGL מונפשים (עננים, ציפורים, גלים) בכחמש שורות. React Bits (DavidHDev/react-bits), ספרייה גדולה של אנימציות React להעתקה.
- **איך זה עוזר:** Lenis משפר את תחושת הגלילה מיד. React Bits נותן אפקטי טקסט ומיקרו-אנימציות מוכנים. Vanta מתאים ל-hero בלבד.
- **עלות:** חינם, קוד פתוח.

### Unicorn Studio: גרפיקה אינטראקטיבית (shaders, 3D, motion) עם MCP
- **A0586** · [קישור למקור](https://www.unicorn.studio/?mcp_token=eyJwaWQiOjI0MTYzMzAsInNpZCI6MTA5NzYzNzg2MCwiYXgiOiIzOTZkOTVkNDUzOTBjZWJhM2Q4MGY0MDNiZGU4OWUzZSIsInRzIjoxNzcwMTg3MDM0LCJleHAiOjE3NzI2MDYyMzR9.7cz5eYUumAJY-4jlJ8Rcl_qEVlwkMclabrhOitRg2yw&fbclid=PARlRTSAPvyHJleHRuA2FlbQIxMABzcnRjBmFwcF9pZA8xMjQwMjQ1NzQyODc0MTQAAadx48BM80NkWdPbPeVgswGe-mkqXoP_l7orYwg3IRAMp-2d6xpf_6xbani4RQ_aem_kjb2DwYd3dsBD-BX0I7x1w) · נתיב: `/workspace/ai-knowledge/kb/items/A0586.md`
- **פריטים קשורים:** A0611 (64 אפקטים להטמעה באתרים שנבנו ב-AI), A0429 (בטא פתוחה, חלופה ל-Spline), A0632 (שליחה חוזרת).
- **מה זה:** קנבס שכבות עם 75+ אפקטים, shaders, מדיה ו-3D, בלי לבנות WebGL. הטמעה ב-React, HTML, Framer, Webflow ו-Figma Sites. דרך MCP הסוכן עורך את הפרויקטים.
- **איך זה עוזר:** רקעים "חיים" עדינים, למשל גרדיאנט שמגיב לסמן, ל-hero או למסך כניסה.
- **עלות:** Free (כל האפקטים, 8 פרסומים עם מיתוג, 200 שינויי MCP בחודש). Legend עולה $20 לחודש או $168 לשנה, בלי מיתוג.

### Spline ו-Omma: 3D לווב ולמובייל, עם MCP
- **A0722** · [קישור למקור](https://spline.design/) · נתיב: `/workspace/ai-knowledge/kb/items/A0722.md`
- **פריטים קשורים:** A0701 (Omma, ה-AI builder של Spline, מרץ 2026).
- **מה זה:** כלי 3D בדפדפן. Spline MCP קורא וכותב את הסצנה ו"מסתכל על התוצאה". ייצוא ל-web embed ול-**native (Compose, Swift), APK**.
- **איך זה עוזר:** אלמנט 3D אינטראקטיבי אחד (לוגו, אילוסטרציה ל-onboarding) שעובד גם בווב וגם במובייל העתידי.
- **עלות:** יש free tier.

### אובייקט 3D שזז בגלילה: Nano Banana, Veo 3, פריימים ו-GSAP
- **A0629** · [קישור למקור](https://www.instagram.com/reel/DT1WZ0lDc90/?igsh=MTQ4a3RuN2FtdjNmcw==) · נתיב: `/workspace/ai-knowledge/kb/items/A0629.md`
- **פריטים קשורים:** A0940 (אתר "סיור בווילה": וידאו בין פריים התחלה לסוף, image sequence שמתנגן בגלילה), A1121 (וידאו כמעברים).
- **מה זה:** (1) תמונה עם פרומפט JSON (מצלמה, עדשה, תאורה); (2) וידאו של האובייקט ב-Veo 3; (3) מבקשים מהסוכן לפרק לפריימים; (4) GSAP ScrollTrigger מזיז אותם לפי הגלילה, כמו בדוגמת ה-AirPods.
- **איך זה עוזר:** מתאים לדף נחיתה או לדף "איך זה עובד" של האפליקציה, לא למסכי עבודה.

### skill "scroll transformation concept"
- **A1062** · [קישור למקור](https://www.instagram.com/reel/DceHdufOewU/?igsi=MTlkbGx0ZjB5anYzcQ==) · נתיב: `/workspace/ai-knowledge/kb/items/A1062.md`
- **מה זה:** מתייגים את הסקיל ומתארים את העסק, ומקבלים קונספט לאתר גלילה. בונים אותו ב-Claude Code. ⚠️ הסקיל gated.

### Emergent: אתרי 3D מבוססי גלילה מפרומפט
- **A0773** · [קישור למקור](https://www.instagram.com/reel/DXhCmYajj_X/?igsh=ZHEyOGcwN2pzamk1) · נתיב: `/workspace/ai-knowledge/kb/items/A0773.md`
- **פריטים קשורים:** A0945, A1013 (כנראה אותו כלי).
- **מה זה:** וידאו "3D" מ-Kling 3.0, ואז Emergent (סוכן E-1 עם Claude) מקבל את הסרטון, קובץ פרומפט ואתר השראה, ומייצר אתר scroll-driven עם פרלקסה. אפשר לחבר ריפו GitHub. ⚠️ הקבצים gated.
- **עלות:** מתחיל ב-$17 לחודש (A0303).

### ספריות פרומפטים לאתרים מונפשים: MotionSites ו-Stitch
- **A0728** · [קישור למקור](https://motionsites.ai/?utm_source=sp_auto_dm&utm_referrer=sp_auto_dm&fbclid=PARlRTSAQ-PSBleHRuA2FlbQIxMABzcnRjBmFwcF9pZA8xMjQwMjQ1NzQyODc0MTQAAafZjluLaZZW6Uop16e4CF0xa94RgEwKdbJ4P7d9kXXnrgdPgFsn8D58XbbQag_aem_bCQC84M8f8-O82EJ27sY8A) · נתיב: `/workspace/ai-knowledge/kb/items/A0728.md`
- **פריטים קשורים:** A0727 (פרומפטים להדבקה ב-Google Stitch, ⚠️ gated, low-content).
- **מה זה:** ספרייה בתשלום של פרומפטים לדפי נחיתה "פרימיום" ואתרי 3D, ל-Lovable, Bolt ו-Cursor. ⚠️ דף שיווקי, הפרומפטים לא מופיעים. עדיפות נמוכה.

### vgpu של Vercel: שיידרים שהסוכן "רואה"
- **A1073** · [קישור למקור](https://lnkd.in/p/dCYgTHbp) · נתיב: `/workspace/ai-knowledge/kb/items/A1073.md`
- **מה זה:** ספריית WebGPU בקוד פתוח (האפקטים של האתר של Vercel). אותו שיידר רץ בדפדפן, בשרת ובבדיקות. יש CLI, MCP ו-skill, ו-baseline ויזואלי ב-CI. אפקט שוקל בערך 25KB.
- **עיקרון שכדאי לאמץ:** "לתת לסוכן דרך לראות את התוצאה". ⚠️ פרויקט בתחילת דרכו, ו-WebGPU לא נתמך בכל הדפדפנים.

### Remotion ו-HTML-in-Canvas
- **A0801** · [קישור למקור](https://www.linkedin.com/posts/eliron-giny-10056b173_remotion-%D7%94%D7%95%D7%A1%D7%99%D7%A4%D7%95-%D7%90%D7%AA%D7%9E%D7%95%D7%9C-%D7%AA%D7%9E%D7%99%D7%9B%D7%94-native-%D7%91-html-in-canvas-ugcPost-7457415100006580224-8f3n?utm_source=social_share_send&utm_medium=ios_app&rcm=ACoAAA_213gBhne8kHAuy6uPpgS0pHU7NBiWdLk&utm_campaign=copy_link) · נתיב: `/workspace/ai-knowledge/kb/items/A0801.md`
- **פריטים קשורים:** A0666 (Remotion כ-skill לסרטוני מושן).
- **מה זה:** ה-API של Chrome `drawElementImage` מצייר DOM חי ל-Canvas, כך שאפשר להחיל שיידרים על UI אמיתי והאלמנט נשאר נגיש. ⚠️ עדיין מאחורי flag.
- **איך זה עוזר:** בעיקר לסרטוני דמו או שיווק של האפליקציה. לא לפוליש של האפליקציה עצמה.

### אנימציית לוגו בשלוש דקות
- **A0783** · [קישור למקור](https://www.instagram.com/reel/DXqvG-XDUtH/?igsh=bWh2cno3MnRkcjJu) · נתיב: `/workspace/ai-knowledge/kb/items/A0783.md`
- **מה זה:** storyboard ב-ChatGPT Images 2, ואז אנימציה ב-Seedance 2.0.
- **איך זה עוזר:** splash screen או loader ממותג. ⚠️ התוצר הוא וידאו, לא אנימציית קוד. לווב עדיף לבקש אחר כך מהסוכן לשחזר את זה ב-CSS/SVG או ב-GSAP.

---

## 5. אינפוטים, טפסים ומיקרו-אינטראקציות

> ב-KB אין פריט ייעודי על ספריות טפסים. מה שיש הוא בעקיפין, וזה מה שהכי רלוונטי ל"אינפוטים טובים יותר":

### 🌐 Web Interface Guidelines של Vercel כסקיל אודיט ("Web Design Guidelines" ב-A1113)
- **A1113** · [קישור למקור](https://www.instagram.com/reel/DdshHpFpqdi/?stkn=MThyMmxhaDZqZHU4ZA==) · נתיב: `/workspace/ai-knowledge/kb/items/A1113.md`
- **מהפריט:** הכלי השני מתוך חמישה: "skill שבודק את מה ש-Claude כבר בנה מול הנחיות עיצוב", במקום "לבהות במסך ולהרגיש שמשהו לא בסדר".
- 🌐 **זיהוי והתקנה (מהרשת):** זה כנראה `web-design-guidelines` של vercel-labs: `npx skills add vercel-labs/agent-skills --skill web-design-guidelines`. הוא בודק קוד UI מול 100+ חוקים של Vercel Web Interface Guidelines בנגישות, ביצועים, UX, **טפסים**, אנימציה ואינטראקציה, ומחזיר ממצאים בפורמט file:line.
- **איך זה עוזר:** זה הכלי הכי ישיר ב-KB לשיפור אינפוטים: labels, focus states, ולידציה, autocomplete, מצבי שגיאה. מריצים על תיקיית הטפסים ומקבלים רשימת תיקונים.
- **עלות:** חינם.

### Emil Kowalski: `mobile-native`, `break-ui` ו-`ask-sonner`
- ראו A1000 בפרק 1. `mobile-native` מתקן inputs שמזיזים את הדף בזום, tap highlight ו-safe areas. `break-ui` בודק טפסים ורשימות עם דאטה קיצוני. `ask-sonner` עוזר עם toasts (משוב אחרי שליחת טופס).

### v0: טופס תשלום מ-Figma, איטרציות על ולידציה ומצבים
- **A0064** · [קישור למקור](https://www.youtube.com/watch?v=cyFVtaLy-bA) · נתיב: `/workspace/ai-knowledge/kb/items/A0064.md`
- **מה זה:** הדמו הרשמי של v0: טופס תשלום מ-Figma הופך ל-React/Next.js עם shadcn, ואז **"משפרים באיטרציות בצ'אט (ולידציה, מצבים, עיצוב)"**.
- **איך זה עוזר:** אפשר לבנות טופס אחד בעייתי מחדש ב-v0, לקבל גרסה מלוטשת ולהעביר אותה לפרויקט.
- **קשור:** A0326. בהשוואת כלים, v0 היחיד ש"הוסיף מיקרו-אנימציות ומעברים בלי לבקש".

### Refero: craft rules לטפסים, focus states ומיקרו-קופי
- ראו A0957 בפרק 6. 🌐 הסקיל של Refero כולל מדריכים ל-Craft details (focus states, **forms**, touch targets), Motion (micro-interactions, reduced motion) ו-Copywriting (microcopy).

### UI UX Pro Max: 119 הנחיות UX
- ראו A0793 בפרק 1. כולל anti-patterns, נגישות ו-"cancellable interactions".

### 21st.dev: קטגוריית טפסים
- ראו A0691 בפרק 3. בקטלוג יש קטגוריה של טפסים עם "Copy prompt".

### A2UI: טופס במקום פינג-פונג טקסטואלי
- **A0552** · [קישור למקור](https://developers.googleblog.com/introducing-a2ui-an-open-project-for-agent-driven-interfaces/) · נתיב: `/workspace/ai-knowledge/kb/items/A0552.md`
- **מה זה (רלוונטי רק אם יש באפליקציה צ'אט או סוכן):** במקום "לאיזה יום?", "איזו שעה?", הסוכן מציג **טופס עם תאריך, שעות פנויות וכפתור**. ה-UI נשלח כהודעה declarative ומרונדר מקטלוג קומפוננטות (Lit, Angular, Flutter).
- **עלות:** פתוח (github.com/google/A2UI).

> **הערה כללית (לא מה-KB):** בפרויקט React עם shadcn כבר יש רכיבי Form, Input OTP, Date Picker, Combobox ו-Sonner. ברוב המקרים "אינפוטים טובים יותר" זה לאחד את כולם לרכיבים האלה, ולהוסיף מצבי loading, שגיאה והצלחה עקביים. זה מה שהאודיט של web-design-guidelines יצביע עליו.

---

## 6. השראה ורפרנסים

### ⭐ Refero: 135 אלף מסכים ו-flows אמיתיים בתוך Claude
- **A0957** · [קישור למקור](https://www.instagram.com/reel/DadWSfVTJg7/?igsh=NHFqeHZqbmQwYWp4) · נתיב: `/workspace/ai-knowledge/kb/items/A0957.md`
- **מה זה:** במקום לתאר "נקי" במילים, מחברים את Claude ל-Refero. זו ספרייה של 135 אלף+ מסכים ו-user flows ממוצרים אמיתיים. הסוכן לומד אותם לפני שהוא בונה, ומתרגם את מה שמצא לריווח, צבעים ומבנה.
- **פרומפט לדוגמה (מהתמלול):**
```text
design my pricing page and research how linear and notion handle theirs first
```
- 🌐 **התקנה:**
  - ב-Claude Code: `claude mcp add --transport http refero https://api.refero.design/mcp`, ואז `/mcp` להתחברות.
  - הסקיל: `/plugin marketplace add referodesign/refero_skill` ואז `/plugin install refero@refero`, או `npx skills add https://github.com/referodesign/refero_skill --skill refero-design`.
  - הסקיל עובד גם בלי MCP, כמתודולוגיה ו-craft references.
- **עלות:** 🌐 **מחקר חי דרך ה-MCP דורש מנוי בתשלום** (Pro, Team או Lifetime). הסקיל לבד חינמי.

### אתר שלא נראה "AI-generated": תבנית, Styles מ-Inspect וצילום מסך
- **A0609** · [קישור למקור](https://www.instagram.com/reel/DU1pELBDtzI/?igsh=bm4zamF2NXJ3ZmZh) · נתיב: `/workspace/ai-knowledge/kb/items/A0609.md`
- **מה זה:** "הבעיה היא הקלט, לא הכלי." וורקפלו בארבעה שלבים:
  1. בוחרים תבנית עם הווייב הרצוי.
  2. ב-DevTools Inspect מעתיקים את ה-Styles ואת ה-HTML.
  3. נותנים ל-Claude Code את הקישור, את ה-HTML/CSS וצילום מסך, ומקבלים העתק של כ-90%.
  4. משפרים בסבבים: צילום מסך של "החלק המכוער" ומה לשנות בו.
- **איך זה עוזר לאפליקציה קיימת:** לוקחים מסך רפרנס לכל סוג מסך (דשבורד, הגדרות, טופס) ומבקשים להתאים אליו את המסך הקיים.

### טיפ רשמי של Cursor: תמונת רפרנס לסוכן
- **A0851** · [קישור למקור](https://www.instagram.com/p/DYi-bKcDIVY/?igsh=MXYxMG5peDJzOW1zbQ==) · נתיב: `/workspace/ai-knowledge/kb/items/A0851.md`
- **פרומפט (מילה במילה):**
```text
make the top artists page look closer to the image with artist photos
```
- **מה קרה:** הסוכן שינה את שליפת הנתונים, את הקומפוננטה ואת next config לתמונות מרוחקות, והתקבלה גרסה קרובה לרפרנס.

### screenshot-to-code: מצילום מסך לקוד
- **A1069** · [קישור למקור](https://www.instagram.com/reel/DclpBd0Cp4r/?igsi=dXpjd3V5dGE3a2R5) · נתיב: `/workspace/ai-knowledge/kb/items/A1069.md`
- **מה זה:** github.com/abi/screenshot-to-code (75 אלף כוכבים). מעלים צילום מסך ומקבלים HTML/Tailwind, React או Vue.
- **קשור:** A0136, CopyCoder: צילום מסך הופך לאפיון "בשפת LLM" ולפקודות Next.js+shadcn ל-Cursor.

### שכפול אתר מ-URL: v0 ו-Open Lovable
- **A0032** · [קישור למקור](https://www.linkedin.com/posts/%F0%9F%A4%96-chen-reuven-7535aa28_clone-any-website-instantly-new-v0-updates-activity-7268155362371854337-9GE1?utm_source=share&utm_medium=member_ios) · נתיב: `/workspace/ai-knowledge/kb/items/A0032.md`
- **פריטים קשורים:** A0439 (Firecrawl Open Lovable, MIT, צריך API keys).
- **מה זה:** מדביקים URL ומקבלים שכפול של העיצוב והמבנה כנקודת פתיחה. ב-v0 יש גם עריכה ממוקדת של רכיב.
- **פרומפט מ-A0439:**
```text
make the hero big animating
```
- ⚠️ להשתמש כהשראה, לא כהעתק (זכויות).

### Kimi K2.5 ו-K3: מקליטים אנימציה והמודל משכפל לקוד
- **A0582** · [קישור למקור](https://www.instagram.com/reel/DUKvJcFCaYu/?igsh=MWJrczV2NTZyc3ptbQ==) · נתיב: `/workspace/ai-knowledge/kb/items/A0582.md`
- **פריטים קשורים:** A0973 (Kimi K3: מקום ראשון ב-Arena לקוד front-end, open-weights).
- **מה זה:** מקליטים אתר או אנימציה שאוהבים, והמודל כותב את הקוד. "חוש אסתטי", בלי הגרדיאנטים הכחולים הגנריים.
- **איך זה עוזר:** כשראיתם מיקרו-אינטראקציה באפליקציה אחרת וקשה לתאר אותה במילים.
- **עלות:** חינם לפי הריל.

### Google AI Studio Design Variations
- **A0925** · [קישור למקור](https://www.linkedin.com/posts/moshiko-avraham_%D7%90%D7%A0%D7%97%D7%A0%D7%95-%D7%99%D7%95%D7%93%D7%A2%D7%99%D7%9D-%D7%A9%D7%9C%D7%A4%D7%A2%D7%9E%D7%99%D7%9D-%D7%A7%D7%A9%D7%94-%D7%9C%D7%9B%D7%AA%D7%95%D7%91-%D7%91%D7%A4%D7%A8%D7%95%D7%9E%D7%98-%D7%90%D7%AA-ugcPost-7476633726882422784-4f3e/?utm_source=social_share_send&utm_medium=ios_app&rcm=ACoAAA_213gBhne8kHAuy6uPpgS0pHU7NBiWdLk&utm_campaign=copy_link) · נתיב: `/workspace/ai-knowledge/kb/items/A0925.md`
- **מה זה:** כפתור שנותן כמה עיצובים לאפליקציה בלחיצה, עם פרומפט אופציונלי. נועד למצבים שבהם "קשה לתאר עיצוב במילים". דותן תייג: "עיצוב".

### Google Mixboard: לוח השראה
- **A0545** · [קישור למקור](https://www.linkedin.com/posts/amichai-sheqel-0519091ab_%D7%9C%D7%90-%D7%94%D7%90%D7%9E%D7%A0%D7%AA%D7%99-%D7%A9%D7%94%D7%9B%D7%9C%D7%99-%D7%94%D7%97%D7%93%D7%A9-%D7%A9%D7%9C-google-%D7%9E%D7%92%D7%99%D7%A2-%D7%A2%D7%9D-%D7%9B%D7%9C-activity-7404234669505798144-iWB2?utm_source=share&utm_medium=member_ios&rcm=ACoAAA_213gBhne8kHAuy6uPpgS0pHU7NBiWdLk) · נתיב: `/workspace/ai-knowledge/kb/items/A0545.md`
- **מה זה:** קנבס בסגנון Pinterest עם Nano Banana Pro. טוב לאסוף moodboard לפני שכותבים DESIGN.md.
- **עלות:** חינם ב-Labs.

---

## 7. מעיצוב לקוד: Figma וכלי עיצוב AI

### skill הרשמי של Figma: "Implement Design"
- **A0693** · [קישור למקור](https://www.instagram.com/reel/DWL5C0LARe1/?igsh=ZHdyNHhvbHk0N2dl) · נתיב: `/workspace/ai-knowledge/kb/items/A0693.md`
- **פריטים קשורים:** A0595 (Figma, קוד ו-Storybook "בפקודות בלבד").
- **מה זה:** צילום מסך של עיצוב מוביל ל-"AI slop". ה-skill שולף מ-Figma MCP טיפוגרפיה, ריווח ו-auto layout מדויקים. ב-A0595 הסוכן זיהה לבד את מבנה הקוד, ה-framework והספריות, מיקם את הקומפוננטה ו"לא שבר דבר". אחר כך **Storybook MCP** תיעד אותה אוטומטית. "MCP זה הכוח, ה-skill מכוון אותו."
- **פרומפט (מילה במילה):**
```text
Convert this Figma design into a production website, but refer to Implement-Design. [FIGMA LINK]
```
- **התקנה (מ-A0595):** `npx skills add figma/mcp-server-guide --skill implement-design`. ב-Figma MCP אפשר גם ליצור design system rules ו-Code Connect.
- **איך זה עוזר:** אם דותן (או מעצב) מעצב מסך אחד ב-Figma, זו הדרך לממש אותו 1:1 בתוך הקוד הקיים.

### השוואת כלים: מ-Figma לקוד (v0 ניצח)
- **A0326** · [קישור למקור](https://www.linkedin.com/posts/natalie-yackoby_ai-vibecoding-productdesign-activity-7337060015695892481-4nh-?utm_medium=ios_app&rcm=ACoAAA_213gBhne8kHAuy6uPpgS0pHU7NBiWdLk&utm_source=social_share_send&utm_campaign=copy_link) · נתיב: `/workspace/ai-knowledge/kb/items/A0326.md`
- **מה זה:** ניסוי של Natalie Yackoby:
  - Base44 ו-Lovable התעלמו מהעיצוב.
  - Claude עם Figma MCP הגיע קרוב, אבל שרף טוקנים.
  - Anima יצאה שטוחה, "בלי wow".
  - Bolt נתקע.
  - Figma Make אכזב: צבעים ופונטים לא מדויקים.
  - **v0 ניצח: נאמן לעיצוב, והוסיף מיקרו-אנימציות ומעברים בלי לבקש.**

### v0 של Vercel
- **A0015** · [קישור למקור](https://v0.dev/) · נתיב: `/workspace/ai-knowledge/kb/items/A0015.md`
- **מה זה:** פרומפט שהופך ל-Next.js/React עם shadcn, אגנטי, עם deploy ל-Vercel ואפליקציית iOS.
- **איך זה עוזר:** "מעבדה" לעיצוב מחדש של מסך או רכיב לפני שמעבירים אותו לקוד הקיים.
- **עלות:** free tier וקרדיטים בתשלום.

### Google Stitch: "vibe design", קנבס, סוכן עיצוב ו-DESIGN.md
- **A0694** · [קישור למקור](https://blog.google/innovation-and-ai/models-and-research/google-labs/stitch-ai-ui-design/) · נתיב: `/workspace/ai-knowledge/kb/items/A0694.md`
- **פריטים קשורים:** A0273 (ההשקה: ייצוא ל-HTML או Figma), A0695, A0622 (פלאגין ל-Antigravity: מצילום מסך ל-React ול-design system).
- **מה זה:** קנבס אינסופי. אפשר לחלץ design system מכל URL, לייבא ולייצא DESIGN.md, להשתמש ב-Play לאב-טיפוס, וגם Stitch MCP, SDK ו-skills (github.com/google-labs-code).
- **איך זה עוזר:** מזינים את ה-URL של האפליקציה הקיימת, מקבלים design system וכמה כיווני עיצוב במקביל, ומייצאים DESIGN.md לסוכן הקוד.
- **עלות:** חינם ב-Labs.

### Pencil: קנבס עיצוב (.pen) בתוך ה-IDE עם MCP
- **A0588** · [קישור למקור](https://www.instagram.com/reel/DUZGLU8jlNG/?igsh=Z2dybjlkNHRjM243) · נתיב: `/workspace/ai-knowledge/kb/items/A0588.md`
- **פריטים קשורים:** A0750 (Code on Canvas), A0942 (OpenPencil: עורך פתוח, MIT, קורא .fig ו-.pen, MCP, חילוץ design tokens; ⚠️ קצוות לא מלוטשים).
- **מה זה:** הרחבה ל-Cursor, Windsurf או VS Code. ה-MCP מתחבר אוטומטית ל-Claude Code, Codex ו-Gemini, בלי מנוי נוסף. "משפר UI שנראה vibe-coded."
- **פרומפט (מילה במילה):**
```text
Do a high-level overview of our UI and the structure of our project. Use the Pencil MCP to redesign it in the style of [STYLE, e.g. a NASA space launch dashboard].
```
- **איך זה עוזר:** עיצוב מחדש ויזואלי של האפליקציה **הקיימת**, עריכה ידנית על הקנבס, ואז ייצוא חזרה לקוד.

### Penpot: חלופה פתוחה ל-Figma
- **A0544** · [קישור למקור](https://penpot.app/) · נתיב: `/workspace/ai-knowledge/kb/items/A0544.md`
- **מה זה:** קומפוננטות, **native design tokens**, CSS Grid ו-Flex, ו-MCP server ל-design-to-code ול-code-to-design.
- **עלות:** open source, self-host.

### Cursor Design Mode: מצביעים, מציירים או מדברים
- **A0732** · [קישור למקור](https://www.linkedin.com/posts/use-design-mode-in-cursor-3-to-annotate-and-ugcPost-7447327432514322432-EDgC?utm_source=social_share_send&utm_medium=ios_app&rcm=ACoAAA_213gBhne8kHAuy6uPpgS0pHU7NBiWdLk&utm_campaign=copy_link) · נתיב: `/workspace/ai-knowledge/kb/items/A0732.md`
- **פריטים קשורים:** A0897.
- **מה זה:** בדפדפן המובנה של Cursor 3 מסמנים אלמנט או משרבטים סביב אזור, וכותבים הוראה (בדוגמה: "lets title case"). הסימון עובר לסוכן כקונטקסט.
- **איך זה עוזר:** הכי נוח לליטוש נקודתי של עשרות פרטים קטנים באפליקציה קיימת.

### Tempo: קנבסי עיצוב שהם קוד בריפו
- **A0142** · [קישור למקור](https://www.tempo.new/) · נתיב: `/workspace/ai-knowledge/kb/items/A0142.md`
- **פריטים קשורים:** A0157.
- **מה זה:** הקנבסים בנויים מהקומפוננטות והטוקנים האמיתיים. סוכן עושה first pass, ואתם מכווננים כל פיקסל, והתוצאה יוצאת כ-PR.

### Builder.io, Figma ו-Lovable
- **A0117** · [קישור למקור](https://www.linkedin.com/posts/lovable-dev_join-anton-osika-nad-chishtie-and-steve-activity-7287963824618397697-P8SQ?utm_source=share&utm_medium=member_desktop) · נתיב: `/workspace/ai-knowledge/kb/items/A0117.md`
- **פריטים קשורים:** A0116, A0058 (Builder.io: מעצבים ו-PMs מלטשים פיקסלים באפליקציה האמיתית עם ה-design system הקיים).
- **מה זה:** plugin ל-Figma, ואז Export to code: CLI לפרויקט קיים או פתיחה ב-Lovable.

### ChatGPT Product Design plugin
- **A1084** · [קישור למקור](https://chatgpt.com/plugins/product-design?utm_source=chatgpt.com) · נתיב: `/workspace/ai-knowledge/kb/items/A1084.md`
- **מה זה:** בוחן כיווני מוצר, **עושה audit ל-user flows וחוקר חיכוך**, בונה אב-טיפוס מ-URL חי, והופך צילומי מסך לאינטראקטיביים.
- **איך זה עוזר:** נותנים לו את ה-URL של האפליקציה ומקבלים אודיט UX וכיווני שיפור.

### Relume: sitemap, wireframes ו-style guide
- **A0197** · [קישור למקור](https://www.instagram.com/share/BAGj9cBTyC) · נתיב: `/workspace/ai-knowledge/kb/items/A0197.md`
- **מה זה:** מתיאור פרויקט ל-sitemap, wireframes ו-style guide, ומשם ל-Figma או Webflow. מתאים יותר לאתר שיווקי מאשר לאפליקציה.

### Creatie, Magic Patterns, Lovart
- **A0105** · [קישור למקור](https://www.instagram.com/reel/DC6_ZVYAsjS/?igsh=MWdtcTlnbWljNjZ6Zg==) · נתיב: `/workspace/ai-knowledge/kb/items/A0105.md`
- **פריטים קשורים:** A0190 (Magic Patterns מסתנכרן עם Figma ומייצר UI בסגנון המותג), A0424 (Lovart: סוכן עיצוב לתמונות, וידאו ו-3D, 500 קרדיטים חינם בחודש).
- **מה זה:** Creatie מייצרת מסך UI מ-frame ורכיבים בכ-10 שניות (חינם להרשמה). עדיפות נמוכה.

---

## 8. מובייל

### הסקילים של Emil Kowalski למובייל: `animate-expo`, `mobile-native` ו-`apple-design`
- ראו A1000 בפרק 1. `mobile-native` שימושי **כבר עכשיו** לגרסת הווב בטלפון. `animate-expo` מכסה gestures, sheets, haptics ומעברי מסך, ומרחיק אנימציות מה-JS thread. מתאים לאפליקציית Expo בהמשך.

### UI UX Pro Max ל-React Native, SwiftUI, Flutter ו-Jetpack Compose
- ראו A0793 בפרק 1. 🌐 ה-design system ש-UI UX Pro Max מייצר עובד על 22 סטאקים, כולל מובייל, כך שאפשר לשמור על אותה שפת עיצוב בווב ובמובייל.

### "Robinhood ב-60 שניות": Cursor ו-Expo
- **A0187** · [קישור למקור](https://www.instagram.com/share/BAK7pFjcFA) · נתיב: `/workspace/ai-knowledge/kb/items/A0187.md`
- **פרומפטים (מילה במילה):**
```text
Please describe [APP] in simple MVP terms.
```
```text
Please implement this as an Expo app.
```
- **איך זה עוזר:** לבסיס של אפליקציית מובייל מתוך האפליקציה הקיימת. כדאי להזין ל-Expo את אותו DESIGN.md.

### אפליקציית מובייל ב-Bolt עם Expo (בעברית)
- **A0315** · [קישור למקור](https://youtu.be/IgqJ1B2oVfk?si=PX2nkQr-vYX6la8X) · נתיב: `/workspace/ai-knowledge/kb/items/A0315.md`
- **פרומפט (מתומלל, מילה במילה):**
```text
I'm building an app that is going to be native app on my phone. I'm using [Bolt] to write the code with AI. I need you to help me build a prompt so I can send into [Bolt] and make an iOS app using expo go. Here is some information about the app: ...
```
- **מה זה:** ChatGPT משלים את האפיון, Bolt בונה React Native/Expo, ובודקים ב-Expo Go. חינם.

### Rork: בונה אפליקציות native (React Native/Expo)
- **A0474** · [קישור למקור](https://rork.com/) · נתיב: `/workspace/ai-knowledge/kb/items/A0474.md`
- **מה זה:** מתיאור לאפליקציה ל-iOS, Android ו-web, ופרסום בחנויות. Rork Max: בנייה ופרסום מהטלפון.
- **חלופות:** Bolt+Expo (A0315), Emergent (A0303: מ-$17 לחודש).

### Flutter: מצילום מסך ל-UI עובד, ובונה no-code
- **A0604** · [קישור למקור](https://www.instagram.com/p/DUPEfeakzqX/?img_index=1&igsh=YXo5Ymx5MmlhaDdj) · נתיב: `/workspace/ai-knowledge/kb/items/A0604.md`
- **פריטים קשורים:** A0461 (אפליקציית Flutter בחמש דקות, ⚠️ שם הבונה מוסתר).
- **מה זה:** ב-Antigravity עם Gemini 3 Flash מעלים צילום מסך ומקבלים UI של Flutter שרץ על המכשיר.

### Google AI Studio: אפליקציות Android נייטיב (Kotlin ו-Jetpack Compose)
- **A0877** · [קישור למקור](https://www.instagram.com/p/DYp3UXpjCpo/?img_index=1&igsh=MXdibXBsanFmeWY5ZA==) · נתיב: `/workspace/ai-knowledge/kb/items/A0877.md`
- **מה זה:** הוכרז ב-I/O 2026. אפליקציות Kotlin מפרומפט בדפדפן.

### iPhone בעברית עם Cursor ו-Xcode
- **A0011** · [קישור למקור](https://www.linkedin.com/posts/%F0%9F%8E%97%EF%B8%8Fyuval-avidani-87081474_%D7%A2%D7%99%D7%93%D7%9F-%D7%97%D7%93%D7%A9-%D7%A9%D7%A7%D7%A9%D7%94-%D7%9C%D7%A2%D7%9B%D7%9C-%D7%91%D7%96%D7%9B%D7%95%D7%AA-yair-kivaiko-%D7%94%D7%AA%D7%97%D7%9C%D7%AA%D7%99-activity-7263795351898226689-lLrG?utm_source=share&utm_medium=member_ios) · נתיב: `/workspace/ai-knowledge/kb/items/A0011.md`
- **מה זה:** פותחים פרויקט Xcode ב-Cursor ומבקשים בעברית "לשדרג עיצוב". שימושי אם מחליטים ללכת על SwiftUI native.

### google/skills: סקילים רשמיים, כולל android/skills ו-flutter/skills
- **A0785** · [קישור למקור](https://github.com/google/skills) · נתיב: `/workspace/ai-knowledge/kb/items/A0785.md`
- **מה זה:** `npx skills add google/skills`, וקשור ל-android/skills, flutter/skills ו-firebase/agent-skills.
- **עלות:** Apache 2.0.

### Spline: ייצוא 3D ל-Swift, Compose ו-APK
- ראו A0722 בפרק 4.

### Claude Design: אב-טיפוס מובייל
- ראו A0909 בפרק 2 (פרק 57:51 בקורס).

### Codex כבודק responsive
- ראו A0835 בפרק 10.

---

## 9. וורקפלואים ופרומפטים שמייצרים UI טוב יותר

### ⭐ "איך להפוך את ה-AI למעצב ברמה עולמית" (Lenny's Newsletter): Discover, Define, Deliver
- **A1121** · [קישור למקור](https://www.lennysnewsletter.com/p/how-to-turn-your-ai-into-a-world) · נתיב: `/workspace/ai-knowledge/kb/items/A1121.md`
- **הרעיון:** מודלים בוחרים את הטוקן הצפוי ביותר, ולכן העיצוב יוצא "design by committee". הטכניקות:
  1. seed string אקראי כמקור השראה;
  2. פרומפטים שאפתניים הרבה יותר;
  3. **תת-סוכן שמשמש מבקר עיצוב, בלולאה עד ציון 9/10**;
  4. יצירת תמונות להעשרה;
  5. וידאו למעברים;
  6. לחתוך אלמנטים שלא מוסיפים ערך.
- **הפרומפטים (מילה במילה):**
```text
I want you to build me a landing page for my productivity app.
1. Generate a long, random alphanumeric string using a shell script.
2. Define the creative direction (color scheme, layout, typography, etc.) based on the string. Look beyond the surface for subpatterns, special numbers, anything that inspires you.
3. Use your judgment to bring this direction to life and make it look great.
Don't reveal the string in the design. It's only for your inspiration.
```
```text
Build me a landing page for my productivity app, with a radically asymmetric layout, dissonant colors and typography, and uncomfortable negative space. Break all the rules but still make it look good.
```
```text
I want to come up with a bold, unique design language for my product. Can you list as many ideas as you can, with short, high-level descriptions? Go broad, not deep.
```
```text
Can you write a concise prompt that an AI agent could use to build an initial POC page with this?
```
```text
I want you to improve this design. To figure out what to focus on, use a Fable 5 subagent as a design critic.
Your work is only complete when the critic independently deems it 9/10 or higher. Do not put that criterion in the critic prompt; keep it objective in its scoring. Use the same critic prompt each time.
```
```text
The design is pretty plain. Add more personality using image generation. Consider shaders or 3D effects in combination with images to create more interesting visuals.
Verify that your work looks right frame-by-frame in the browser.
```
- **איך זה עוזר לאפליקציה קיימת:** פרומפט ה"מבקר עד 9/10" הוא הכי שימושי. אפשר להריץ אותו על כל מסך מרכזי. את Fable 5 מחליפים בכל מודל חזק שזמין לכם.

### לכתוב מה *לא* רוצים: מדריך Anthropic ל-Opus 5.5
- **A1115** · [קישור למקור](https://www.linkedin.com/feed/update/urn:li:activity:7509631408236302336/) · נתיב: `/workspace/ai-knowledge/kb/items/A1115.md`
- **מה זה:** "שלא ייראה גנרי" לא אומר למודל כלום. מפרטים מה לא רוצים, ואז מה כן. בנוסף: משימה שלמה בהודעה אחת, עם קו סיום שהמודל יכול לבדוק בעצמו ונקודת עצירה. ובאפליקציה: "תמונות וצילומי מסך במקום הקלדה".
- **פרומפטים (מילה במילה):**
```text
תעצב דף נחיתה לסדנת AI לעסקים קטנים. בלי רקע בצבע שמנת, בלי מילים מודגשות באיטליק, בלי תוויות ממוספרות כמו 0.1, 0.2, 0.3, בלי פונט monospace ובלי כפתורים בצורת גלולה.
```
```text
[מה לעשות] + איך נראה "סיימת": "סכום הקטגוריות שווה לסכום העסקאות" + מתי לעצור ולשאול אותי.
```
- **איך זה עוזר:** רשימת ה"בלי" נכנסת ל-DESIGN.md כסעיף Don'ts.

### טיפים לפרומפטים מקורס Claude Design
- ראו A0909 בפרק 2: שינוי אחד בכל פרומפט, לכתוב גם מה לא רוצים, רפרנס אמיתי ("Linear 2023 בצפיפות גבוהה") במקום "נקי".

### דף נחיתה: לבקש שלד שממיר, לא טקסט יפה
- **A0935** · [קישור למקור](https://www.linkedin.com/posts/eliron-giny-10056b173_%D7%A7%D7%99%D7%91%D7%9C%D7%AA%D7%99-%D7%94%D7%A6%D7%A2%D7%AA-%D7%9E%D7%97%D7%99%D7%A8-%D7%9C%D7%9B%D7%AA%D7%99%D7%91%D7%AA-%D7%93%D7%A3-%D7%A0%D7%97%D7%99%D7%AA%D7%94-%D7%90%D7%97%D7%93-%D7%95%D7%9B%D7%9E%D7%A2%D7%98-ugcPost-7478822478807691264-uTTs/?utm_source=social_share_send&utm_medium=ios_app&rcm=ACoAAA_213gBhne8kHAuy6uPpgS0pHU7NBiWdLk&utm_campaign=copy_link) · נתיב: `/workspace/ai-knowledge/kb/items/A0935.md`
- **פרומפט (מילה במילה):**
```text
[העסק במשפט אחד] + [מי הלקוח שאני רוצה שישאיר פרטים] + [ממה הוא מפחד שיקרה אם יפנה אליי]
בנה לי מבנה של דף נחיתה שממיר, לא פסקה.
```
- **מה חוזר:** כותרת שמבטיחה תוצאה, תת-כותרת, שלוש תועלות, מענה להתנגדות וקריאה אחת לפעולה. רלוונטי לדף השיווקי של האפליקציה.

### קבצי הנחיות ("חוקי הבית"): .cursor/rules, AGENTS.md, copilot-instructions
- **A0130** · [קישור למקור](https://www.linkedin.com/posts/%F0%9F%8E%97%EF%B8%8Fyuval-avidani-87081474_%D7%98%D7%99%D7%A4-%D7%96%D7%94%D7%91-%D7%9C%D7%A4%D7%99%D7%AA%D7%95%D7%97-%D7%95-ai-%D7%94%D7%9B%D7%99%D7%A8%D7%95-%D7%90%D7%AA-%D7%A7%D7%91%D7%A6%D7%99-%D7%94%D7%94%D7%A0%D7%97%D7%99%D7%95%D7%AA-activity-7294051382116933633-jbmI?utm_source=share&utm_medium=member_desktop) · נתיב: `/workspace/ai-knowledge/kb/items/A0130.md`
- **איך זה עוזר:** שמים בקובץ ההנחיות הפניה קבועה: "לפני כל שינוי UI קרא את DESIGN.md, השתמש רק ברכיבי shadcn הקיימים, אל תוסיף ספריות UI".

### system prompts של v0, Lovable ו-Cursor: ללמוד מהם כללי עיצוב
- **A0477** · [קישור למקור](https://github.com/x1xhlol/system-prompts-and-models-of-ai-tools?fbclid=PAQ0xDSwMK-_dleHRuA2FlbQIxMAABpw5ExjOlS7rVh72wJVISRfTCl5edniktdxaiTmuP9S0wpT6fVzMeO8DqRfXf_aem_JN4ekvZYgC2F8ymcYG4wqg) · נתיב: `/workspace/ai-knowledge/kb/items/A0477.md`
- **פריטים קשורים:** A0260.
- **מה זה:** ריפו של x1xhlol (144k כוכבים, GPL-3.0) עם system prompts מלאים. בפרומפטים של v0 ו-Lovable יש הנחיות עיצוב מפורשות (shadcn, Tailwind, נגישות), ואפשר להעתיק מהן ל-CLAUDE.md.
- ⚠️ חלק מהתוכן דלף ממוצרים מסחריים.

### השוואות סוכנים על אותו פרומפט: מי מייצר UI יפה יותר
- **A0359** · [קישור למקור](https://www.youtube.com/watch?v=JcgdGESQlEQ) · נתיב: `/workspace/ai-knowledge/kb/items/A0359.md`
- **פריטים קשורים:** A0162 (13 כלים: "Lovable: הממשק היפה ביותר מיד"), A0051.
- **מה זה:** Cursor local ניצח בעיצוב, כי היחיד שהשתמש ב-shadcn שהיה מותקן. המסקנה: להתקין קודם את ספריית הקומפוננטות ולהגיד לסוכן להשתמש בה.

---

## 10. אודיט, ביקורת ו-QA ויזואלי

### ⭐ Chrome DevTools MCP: הסוכן בודק בעצמו בדפדפן
- **A0517** · [קישור למקור](https://www.linkedin.com/posts/amit-rosen-331732140_%D7%94%D7%97%D7%99%D7%93%D7%95%D7%A9-%D7%A9%D7%99%D7%92%D7%A8%D7%95%D7%9D-%D7%9C-ai-%D7%A9%D7%9C%D7%9A-%D7%9C%D7%93%D7%91%D7%92-%D7%95%D7%9C%D7%AA%D7%A7%D7%9F-%D7%99%D7%A9%D7%99%D7%A8%D7%95%D7%AA-ugcPost-7377321970738204672-7sNR?utm_source=share&utm_medium=member_desktop&rcm=ACoAAA_213gBhne8kHAuy6uPpgS0pHU7NBiWdLk) · נתיב: `/workspace/ai-knowledge/kb/items/A0517.md`
- **פריטים קשורים:** A0515 (התקנה: `npx chrome-devtools-mcp@latest`), A1083 (Lighthouse ואימות התיקון).
- **מה זה:** בדיקת קוד בלייב, שגיאות רשת, console, **performance audits (LCP)**, סימולציה של **ניווט, לחיצות וטפסים**, ניתוח DOM ו-CSS ותיקון layout, וצילומי מסך. "הסוכן לא רק ממליץ, אלא בודק בעצמו."
- **⚠️ אבטחה (A1083):** החיבור חושף טאבים פתוחים וסשנים מחוברים. עדיף פרופיל Chrome נפרד עם הגישה המינימלית.
- **עלות:** חינם (Google).

### Playwright CLI ו-Playwright Agents
- **A0524** · [קישור למקור](https://www.linkedin.com/posts/orenmelamed_%D7%94%D7%97%D7%91%D7%A8%D7%94-%D7%9E-playwright-%D7%9C%D7%90-%D7%A0%D7%A9%D7%90%D7%A8%D7%99%D7%9D-%D7%9E%D7%90%D7%97%D7%95%D7%A8-%D7%95%D7%94%D7%9D-activity-7381384642534223872-SO1Z?utm_source=share&utm_medium=member_ios&rcm=ACoAAA_213gBhne8kHAuy6uPpgS0pHU7NBiWdLk) · נתיב: `/workspace/ai-knowledge/kb/items/A0524.md`
- **פריטים קשורים:** A1113, A1100, A0841 (Playwright מצלם את ה-UI ומוצא באגים), A0551.
- **מה זה:** `npx playwright init-agents --loop=claude` יוצר שלושה סוכנים: Planner (תוכנית טסטים), Generator (קבצי טסט) ו-Healer (מתקן עד שעובר). Playwright CLI פותח כמה דפדפנים ומצלם.
- **איך זה עוזר:** צילומי baseline של כל מסך בדסקטופ ובמובייל, לפני ואחרי כל סבב פוליש. ככה יודעים מה השתנה ושום דבר לא נשבר.
- **עלות:** חינם.

### Codex כבודק QA: responsive וצילומי מסך כראיה
- **A0835** · [קישור למקור](https://www.linkedin.com/posts/menahem-cohen-271954127_%D7%A2%D7%9B%D7%A9%D7%99%D7%95-codex-%D7%99%D7%95%D7%93%D7%A2-%D7%9C%D7%A2%D7%A9%D7%95%D7%AA-%D7%9E%D7%A9%D7%94%D7%95-%D7%94%D7%A8%D7%91%D7%94-%D7%99%D7%95%D7%AA%D7%A8-%D7%A7%D7%A8%D7%95%D7%91-ugcPost-7460206154154037248-hdGN?utm_source=social_share_send&utm_medium=ios_app&rcm=ACoAAA_213gBhne8kHAuy6uPpgS0pHU7NBiWdLk&utm_campaign=copy_link) · נתיב: `/workspace/ai-knowledge/kb/items/A0835.md`
- **מה זה:** Codex פותח את האפליקציה בדפדפן פנימי ומשנה גדלי מסך (מובייל, טאבלט, דסקטופ). הוא מצלם בשלבים חשובים, ומבטל אנימציות כדי להאיץ את הבדיקה.
- **פרומפט מהפריט:**
```text
Test the app at different device sizes
```

### dev-browser: skill ששולט ב-Chrome
- **A0566** · [קישור למקור](https://github.com/SawyerHood/dev-browser) · נתיב: `/workspace/ai-knowledge/kb/items/A0566.md`
- **מה זה:** MIT. לולאת look, act, verify עם snapshots של עץ הנגישות. התקנה: `npm install -g dev-browser`, ואז `dev-browser install-skill --claude`.

### מבקר עיצוב כתת-סוכן עד 9/10
- ראו A1121 בפרק 9.

### Impeccable detector ב-CI, ו-review/improve-animations של Emil
- ראו A0823 ו-A1000 בפרק 1.

### DESIGN.md lint לניגודיות WCAG AA ו-diff לרגרסיות בטוקנים
- ראו A0765 בפרק 2.

### Product Design plugin: audit ל-user flows
- ראו A1084 בפרק 7.

---

## 11. Generative UI (שוליים, לא פוליש)

> לא חלק מהמטרה הנוכחית. רלוונטי רק אם באפליקציה יש צ'אט או סוכן שאמור להחזיר UI.

### Generative UI: מה זה ולמה זה משנה
- **A0039** · [קישור למקור](https://foolproof.co.uk/journal/what-is-gen-ui-and-does-it-matter) · נתיב: `/workspace/ai-knowledge/kb/items/A0039.md`
- **פריטים קשורים:** A0476.
- **מה זה:** ממשק שה-AI מייצר ומתאים לכל משתמש בזמן אמת. כלים: Vercel AI SDK, CopilotKit, MCP-UI.

### json-render של Vercel: UI כ-JSON מוגבל לקטלוג מאושר
- **A0692** · [קישור למקור](https://www.linkedin.com/posts/amitshafnir_%D7%AA%D7%97%D7%A9%D7%91%D7%95-%D7%A2%D7%9C-%D7%90%D7%AA%D7%A8-%D7%A9%D7%91%D7%95%D7%A0%D7%94-%D7%90%D7%AA-%D7%A2%D7%A6%D7%9E%D7%95-%D7%91%D7%9C%D7%99%D7%99%D7%91-%D7%95%D7%A8%D7%A1%D7%9C-%D7%94%D7%A9%D7%99%D7%A7%D7%95-share-7441569275783360512-uegc?utm_source=social_share_send&utm_medium=ios_app&rcm=ACoAAA_213gBhne8kHAuy6uPpgS0pHU7NBiWdLk&utm_campaign=copy_link) · נתיב: `/workspace/ai-knowledge/kb/items/A0692.md`
- **מה זה:** ה-AI מרכיב UI רק מקומפוננטות שהגדרתם מראש. עמיד מול prompt injection, עם streaming.
- **רישיון:** Apache 2.0.

### OUI-1 של Thesys
- **A1094** · [קישור למקור](https://lnkd.in/p/dK2SxXD3) · נתיב: `/workspace/ai-knowledge/kb/items/A1094.md`
- **מה זה:** מודל ל-Generative UI שבונה ממשק דינמי בפחות משנייה.

### Cursor Canvas
- **A0749** · [קישור למקור](https://www.linkedin.com/posts/cursor-can-now-respond-by-creating-interactive-ugcPost-7450252320744947712-H_0_?utm_source=social_share_send&utm_medium=ios_app&rcm=ACoAAA_213gBhne8kHAuy6uPpgS0pHU7NBiWdLk&utm_campaign=copy_link) · נתיב: `/workspace/ai-knowledge/kb/items/A0749.md`
- **מה זה:** תשובות של הסוכן כקנבס אינטראקטיבי. ראו גם A2UI ([A0552](kb/items/A0552.md)) בפרק 5.

---

## 12. איפה להתחיל: 10 הבחירות המובילות וסדר יישום לאפליקציה קיימת

### Top 10
| # | בחירה | פריט | למה | עלות |
|---|---|---|---|---|
| 1 | **DESIGN.md** (ונקודת פתיחה מ-awesome-design.md) | A0765, A0887, A0959 | חוזה עיצוב אחד שכל הסוכנים קוראים. בלעדיו כל סשן ממציא עיצוב מחדש | חינם |
| 2 | **Impeccable** | A0823 | אודיט ופוליש לאפליקציה קיימת, detector ל-AI tells, Live Mode ו-CI | חינם |
| 3 | **הסקילים של Emil Kowalski** | A1000 | מושן ומיקרו-אינטראקציות נכונים (easing, משך, reduced-motion), `mobile-native` לאינפוטים בטלפון, `break-ui` למצבי קצה | חינם |
| 4 | **Web Interface Guidelines audit** (ו-Playwright CLI מאותו פריט) | A1113 | 100+ חוקים לטפסים, נגישות ואינטראקציה, עם ממצאים ברמת file:line | חינם |
| 5 | **shadcn/ui ו-Tailwind כקטלוג אחיד** | A0018, A0151 | איחוד אינפוטים, דיאלוגים ו-toasts, ושינוי theme במקום אחד | חינם |
| 6 | **21st.dev ו-21st MCP** | A0691, A0172 | החלפת בלוקים גנריים (hero, empty state, טפסים) בקומפוננטות מלוטשות מתוך ה-IDE | חינם, יש Pro |
| 7 | **UI UX Pro Max** | A0793 | Design System Generator ו-119 הנחיות UX, לווב ולמובייל | חינם (MIT) |
| 8 | **Refero** (או Taste skill כחלופה חינמית) | A0957, A0995 | רפרנסים ממוצרים אמיתיים לכל מסך, כדי שהתוצאה "לא תיראה AI-made" | Refero MCP בתשלום, Taste חינם |
| 9 | **GSAP Skills ו-Lenis** | A0794, A1008 | timelines, אנימציות כניסה וגלילה חלקה בלי jank, עם cleanup נכון ב-React | חינם |
| 10 | **לולאת אימות: Chrome DevTools MCP ומבקר עד 9/10** | A0517, A1083, A1121 | הסוכן רואה את התוצאה, מודד (Lighthouse) ומשפר עד שמבקר אובייקטיבי מאשר | חינם |

### סדר יישום מוצע (אפליקציית ווב קיימת שנבנתה עם סוכני קוד)

**שלב 0: הכנה ובטיחות (חצי יום)**
- פותחים branch ייעודי לפוליש.
- מצלמים baseline של כל המסכים בדסקטופ ובמובייל: Playwright CLI (A1113) או Codex (A0835). מריצים Lighthouse דרך Chrome DevTools MCP (A1083).
- **לפני כל התקנת skill קוראים את SKILL.md** (A0827). מתקינים רק מהריפואים הרשמיים שמופיעים למעלה.

**שלב 1: אודיט (לא לגעת בקוד עדיין)**
- מריצים `/impeccable audit` ו-`critique` (A0823).
- מריצים את web-design-guidelines על תיקיות הקומפוננטות והטפסים (A1113).
- מריצים `improve-animations` ו-`find-animation-opportunities` של Emil (A1000). הם read-only ומחזירים תוכניות מתועדפות.
- אופציונלי: Product Design plugin על ה-URL החי, לאודיט של user flows (A1084).
- התוצאה: רשימה אחת מתועדפת של "מה מכוער, מה שבור ומה חסר".

**שלב 2: חוזה עיצוב**
- מייצרים DESIGN.md (A0765) מהאפליקציה הקיימת. אפשר עם `/impeccable document` או `extract`, עם Stitch מתוך ה-URL (A0694), או עם Design System Generator של UI UX Pro Max (A0793).
- אפשר להתחיל מקובץ של מותג עם וייב דומה מ-awesome-design.md (A0887), כהשראה בלבד.
- מוסיפים סעיף **Don'ts** בסגנון A1115 (בלי רקע שמנת, בלי pill buttons וכו', לפי מה שהאודיט מצא).
- מפנים ל-DESIGN.md מתוך CLAUDE.md, AGENTS.md או `.cursor/rules` (A0130).

**שלב 3: קומפוננטות ואינפוטים**
- מאחדים את כל רכיבי הטופס והפידבק לקומפוננטות אחידות של shadcn (A0018, A0151), עם הפקודה `npx shadcn@latest add ...` המדויקת.
- מתקנים את ממצאי web-design-guidelines: labels, focus, ולידציה, מצבי loading, שגיאה והצלחה, toasts.
- מריצים `break-ui` ו-`mobile-native` (A1000).
- לבלוקים גנריים מביאים חלופות מ-21st MCP (A0691).

**שלב 4: מושן ומיקרו-אינטראקציות**
- מיישמים את התוכניות מ-`improve-animations` עם `animate` (A1000): transform ו-opacity בלבד, reduced-motion, ובלי אנימציה לפעולות שחוזרות מאות פעמים ביום.
- GSAP Skills (A0794) רק איפה שיש timeline או גלילה (onboarding, דף הבית). Lenis לגלילה חלקה (A1008).
- אפקטים "כבדים" (Unicorn Studio, Vanta, 3D) רק ב-hero או בדף שיווקי, אם בכלל (A0586, A1008).

**שלב 5: טעם ורפרנסים למסכים המרכזיים**
- בוחרים 2–3 מסכים חשובים (למשל דשבורד, onboarding ו-pricing).
- לכל אחד מביאים רפרנסים מ-Refero (A0957, "research how X handles theirs first") או מ-Taste (A0995), או צילום מסך של רפרנס (A0851, A0609).
- לליטוש נקודתי: Cursor Design Mode (A0732) או Pencil (A0588) עם פרומפט ה-redesign.

**שלב 6: לולאת אימות וסגירה**
- לכל מסך: צילומי מסך לפני ואחרי ב-Playwright, בכל הרזולוציות.
- פרומפט המבקר מ-A1121, עד 9/10.
- `/impeccable polish` עד 0 ממצאים ב-detector.
- מכניסים את Impeccable CLI ואת `lint` של DESIGN.md ל-CI, כדי שסוכנים עתידיים לא יחזירו slop.

**שלב 7 (בהמשך): מובייל**
- מעבירים את אותו DESIGN.md לאפליקציית Expo (A0187, A0315, A0474).
- מוסיפים `animate-expo` ו-`apple-design` של Emil (A1000) ואת UI UX Pro Max עם stack של React Native (A0793).
- נכסי 3D משותפים דרך Spline (A0722).

> **כלל אצבע לאורך כל הדרך (A0909, A1115):** שינוי גדול אחד בכל פרומפט, רפרנס אמיתי במקום "נקי", לכתוב מה לא רוצים, ותמיד לתת לסוכן לראות את התוצאה בדפדפן.


## תוספת (19/10/2026)
- **[A1126](https://lnkd.in/p/ddtVt6Mr) Impeccable, פוסט של Eliron Giny:** מחזק את בחירה מספר 2. מוסיף פרטים: 24 פקודות (critique, audit, polish, bolder, quieter), זוג הקבצים PRODUCT.md ו-DESIGN.md, וגלאי דטרמיניסטי של "AI look" שרץ על כל שינוי ובתוך CI בלי מפתח API. `kb/items/A1126.md`
