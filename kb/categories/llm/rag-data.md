# מודלים וכלי LLM (LLM tools) › RAG, נתונים ו-knowledge bases

[← מודלים וכלי LLM (LLM tools)](README.md) · [ראשי](../../README.md) · 25 פריטים

## סינתזה

**מ-RAG ל"מוח ארגוני":** החומרים המוקדמים עוסקים ב-RAG קלאסי (Pinecone [A0045](../../items/A0045.md), RAGFlow [A0484](../../items/A0484.md), Gemini File Search [A0538](../../items/A0538.md), Text-to-SQL עם Vanna [A0211](../../items/A0211.md)) ובחיפוש לסוכנים (Tavily [A0475](../../items/A0475.md)).
**קליטת מסמכים:** המרת מסמכים ואתרים ל-Markdown נקי (Crawl4AI [A0963](../../items/A0963.md), anydoc [A1039](../../items/A1039.md)) הפכה לשלב קריטי בפני עצמו. גם הדור החדש של OCR פתוח עושה בדיוק את זה: olmOCR [A0929](../../items/A0929.md), Unlimited-OCR [A0981](../../items/A0981.md) ו-Chandra [A0546](../../items/A0546.md). LangExtract מחלץ נתונים מובנים מכמה דוגמאות [A0983](../../items/A0983.md), ויש שליפה ויזואלית מ-PDF בלי OCR [A1063](../../items/A1063.md).
**זיכרון וגרף ידע:** החומרים החדשים טוענים שהבעיה היא **עדכניות** ולא שליפה [A0946](../../items/A0946.md). הם מציעים אנטומיה של מוח (קליטה, זכירה, "חלימה וגיזום" בלילה ושליפה [A1074](../../items/A1074.md)), זיכרון בשכבות לסוכנים (TencentDB [A1031](../../items/A1031.md)), וגרף ידע שבו כל קישור הוא נתיב קובץ מלא [A0975](../../items/A0975.md). זה מתחבר לגרפי הקוד ב-coding/repos ול-Obsidian ב-business/productivity.
**Embeddings מולטימודליים:** [A0662](../../items/A0662.md) [A0669](../../items/A0669.md).

**כלים בולטים בתת-הקטגוריה:** Hugging Face (2), Ollama (2), Obsidian (2), Claude Code (2), MCP (2), Cursor (2), Gemini Embedding 2 (2), RAGFlow (2), Cohere Embed (2), GBrain (1), Zep (1), Graphiti (1)

## פריטים

| ID | כותרת | מחבר | תאריך | תקציר |
|---|---|---|---|---|
| [A1074](../../items/A1074.md) | תשע גישות ל"מוח ארגוני": קליטה, זכירה, "חלימה וגיזום" בלילה, ושליפה | Roey Zalta | 2026-08-30 | בהרבה ארגונים "המוח" הוא RAG בשם חדש: יודע למצוא, לא זוכר. לכל הגישות יש אותה אנטומיה: קולט סיגנלים (שיחות, מסמכים, מערכות, אירועים); זוכר עובדות,… |
| [A1063](../../items/A1063.md) | EVIE-Preview-4.5B של Tencent: חיפוש ויזואלי מקומי במסמכי PDF, בלי OCR | Amit Yanay | 2026-08-26 | מודל VDR (Visual Document Retrieval) עם משקלים פתוחים שמאנדקס את תמונת העמוד כמו שהיא, בלי OCR ובלי שיטוח ל-Markdown. הווקטורים מייצגים יחד טקסט,… |
| [A1039](../../items/A1039.md) | anydoc של Firecrawl: כל מסמך ל-Markdown בפחות מ-5 מילישניות (Rust, MIT) | Amit Shafnir | 2026-08-06 | ספרייה פתוחה (MIT) שממירה כ-14 פורמטים (Word, PowerPoint, Excel, PDF, EPUB, RTF, CSV ועוד) ל-Markdown אחיד. זמן חציוני מתחת ל-5ms, ו-500 קבצי docx… |
| [A1031](../../items/A1031.md) | TencentDB Agent Memory: זיכרון מקומי וקוד פתוח בארבע שכבות לסוכנים (61% פחות טוקנים, לפי הריל) | 100xEngineers | 2026-08-02 | לפי הכיתוב, ארבע שכבות בהשראת המוח: זיכרון קצר טווח למה שקורה עכשיו, ועד זיכרון שאוגר הרגלים, העדפות ואישיות לאורך זמן. הסוכן לא קורא מחדש את הרקע… |
| [A0981](../../items/A0981.md) | Unlimited-OCR של Baidu: מודל OCR של 3B ברישיון MIT, שקורא PDF שלם במעבר אחד | רני אלבג ויין | 2026-07-20 | 3 מיליארד פרמטרים, רץ מקומית. קורא מסמך ארוך שלם במעבר אחד, בלי לחתוך לעמודים ובלי לאבד הקשר, עם חלון של 32K. רץ עם Transformers, vLLM, SGLang,… |
| [A0983](../../items/A0983.md) | LangExtract של גוגל: חילוץ נתונים מובנים מטקסט חופשי לפי כמה דוגמאות, עם מיפוי לכל שדה במקור | רני אלבג ויין | 2026-07-20 | ספריית Python פתוחה (37 אלף כוכבים). נותנים כמה דוגמאות ומסמך (רפואי, חוזה, דוח), ומקבלים נתונים בסכמה קבועה, בלי regex ובלי אימון. כל שדה ממופה… |
| [A0975](../../items/A0975.md) | גרף ידע לסוכנים: נתיבי קבצים מלאים בקישורים במקום [[שם קובץ]], ו-Open Knowledge Format של גוגל | Eric Bragas | 2026-07-18 | Obsidian הוא רק אפליקציה מעל קובצי Markdown, והקישורים בו הם שם הקובץ בלבד. כשיש אלפי קבצים, הסוכן צריך לרשום את כל התיקיות כדי למצוא את המחט, וזה… |
| [A0963](../../items/A0963.md) | Crawl4AI: סורק ווב פתוח שהופך כל אתר ל-Markdown מוכן ל-LLM (86k כוכבים) | unclecode | 2026-07-16 | Crawl4AI (Apache-2.0, כ-86k כוכבים) הופך כל אתר ל-Markdown נקי לסוכנים ול-RAG. אפשר להריץ לבד (pip, Playwright, Docker, CLI) או לעבוד עם Crawl4AI… |
| [A0946](../../items/A0946.md) | Company Brain לצוות ב-monday: הבעיה היא עדכניות, לא שליפה | Amit Cohen | 2026-07-08 | לקחים מבניית Company Brain בשלושה שבועות: (1) הבעיה היא freshness, לא retrieval; (2) מתחילים ממקורות הידע, לא מה-wiki; (3) הכל אוטומטי: Notetaker בכל… |
| [A0929](../../items/A0929.md) | olmOCR של AllenAI: מ-PDF וסריקות ל-Markdown נקי לשימוש ב-LLM (טבלאות, משוואות, כתב יד) | Marc Kaz | 2026-06-30 | מטפל בטבלאות, משוואות, כתב יד ופריסות של כמה עמודות. שומר על סדר קריאה טבעי. עובד על סריקות ישנות, איורים, כותרות עליונות ותחתונות.… |
| [A0669](../../items/A0669.md) | Gemini Embedding 2: embeddings מולטימודליים (וידאו, תמונה, אודיו, טקסט) ורעיונות לאפליקציות | Sina | 2026-03-13 | מודל embedding מולטימודלי מטבעו: מקבל וידאו, תמונות, אודיו וטקסט ומאפשר לחלץ ולחפש מידע מכולם יחד, למשל וידאו ו-PDF. רעיונות: אפליקציית כושר שצופה… |
| [A0662](../../items/A0662.md) | Gemini Embedding 2: טקסט, תמונה, וידאו, אודיו ו-PDF באותו מרחב וקטורי | Itai Ben Zeev | 2026-03-12 | מודל ה-embedding הראשון של גוגל שממפה טקסט, תמונות, וידאו, אודיו ו-PDF לאותו מרחב. קריאת API אחת במקום מודלים נפרדים ו-glue code. Matryoshka: 768 עד… |
| [A0546](../../items/A0546.md) | Chandra (Datalab): OCR בקוד פתוח לטבלאות, נוסחאות וכתב יד | Amit Rosen | 2025-12-20 | OCR הוא צוואר בקבוק בפרויקטי AI, כי כלים רגילים "עיוורים למבנה". Chandra מזהה layout (כותרת, טקסט, טבלה), ממיר נוסחאות ל-LaTeX (Vision-to-Code),… |
| [A0538](../../items/A0538.md) | Gemini File Search: RAG מנוהל ב-Gemini API | Joseph Michael | 2025-11-07 | File Search ב-Gemini API עושה בשבילך 5 מתוך 6 השלבים של RAG: טעינה, chunking, embeddings, vector DB ו-retrieval. מעלים קבצים, הוא מאנדקס, ומשמש כהקשר… |
| [A0484](../../items/A0484.md) | RAGFlow: צ'אטבוט על המסמכים שלך, בלי חודשים של בנייה | Roey Zalta | 2025-08-20 | RAGFlow (קוד פתוח): עובד עם כל מודל (GPT-5, Claude, Llama), קורא טבלאות ותמונות, מחזיר ציטוטים למקור, מתקין ב-Docker עם API, תומך GraphRAG ויכולות… |
| [A0475](../../items/A0475.md) | Tavily: מנוע חיפוש בזמן אמת לסוכני AI | Tavily | 2025-08-14 | APIs לחיפוש וחילוץ תוכן מהרשת שמחזירים מידע מובנה ו-chunked למודל, ל-grounding בלי הזיות. caching ו-indexing ל-latency צפוי, ושכבות אבטחה נגד דליפת… |
| [A0323](../../items/A0323.md) | 6 כלי no-code ו-open source לבניית LLM, Agents ו-RAG | Avi Chawla | 2025-07-04 | RAGFlow (RAG עם ציטוטים, 59k כוכבים), xpander (backend לסוכנים), Transformer Lab (אימון וצ'אט מקומי), LLaMA-Factory (fine-tuning של 100+ מודלים בלי… |
| [A0310](../../items/A0310.md) | Bright Data: פלטפורמת proxies, scraping ו-datasets לאיסוף מידע מהרשת | Bright Data | 2025-07-02 | פלטפורמה לגישה למידע ציבורי ברשת: יותר מ-400M IPs של proxies, Scraper APIs, ו-Data Feeds מוכנים (יותר מ-5B רשומות), ל"כל מודל, pipeline או workflow".… |
| [A0211](../../items/A0211.md) | Vanna: Text-to-SQL פתוח שבאמת עובד (RAG על הסכמה) | Akshay Pachaar | 2025-04-12 | Vanna (14k+ כוכבים): "מאמנים" RAG על הסכמה, ה-DDL ודוגמאות מהנתונים שלך, ושואלים בשפה טבעית. מקבלים SQL שרץ אוטומטית, טבלה, גרף ושאלות המשך. הנתונים… |
| [A0196](../../items/A0196.md) | אפליקציית RAG על MCP למסמכים מורכבים (GroundX + Cursor) | Akshay Pachaar | 2025-04-04 | MCP server שעוטף את GroundX (חיפוש ושליפה ממסמכים מורכבים עם טבלאות, תרשימים ותמונות) ומתחבר ל-Cursor: חיפוש ו-ingest של מסמכים חדשים מצ'אט ה-Agent. |
| [A0135](../../items/A0135.md) | לראות Embeddings בעיניים (Cohere Playground) | Yuval Avidani | 2025-02-20 | דמו בעברית: מזינים משפטים ל-Embeddings ב-Cohere Playground ורואים אותם כנקודות במרחב. משמעות דומה יוצאת קרובה. בסיס להבנת clustering. |
| [A0127](../../items/A0127.md) | Second Brain: צ'אט שעונה רק מתוך המקורות שנתתם (דוקומנטציה, ספרים, יוטיוב, GitHub) | Tech Wizzdom (Domagoj Lalk Vidovic) | 2025-02-07 | במקום לקרוא דוקומנטציה, מדביקים את הקישור ל-Second Brain ושואלים. הידע מגיע רק מהמסמכים שסופקו, וכשאין תשובה הוא אומר "I don't know" במקום להמציא קוד… |
| [A0045](../../items/A0045.md) | Pinecone: פלטפורמת ידע וחיפוש וקטורי לאייג'נטים | Pinecone | 2024-12-03 | Vector DB מנוהל ל-RAG ולאייג'נטים: search, upsert ו-rerank מאותו אינדקס, plugin ל-Claude Code, ומחיר שלא מתייקר בסקייל. |
| [A0037](../../items/A0037.md) | תובנות על LLMs מלייב עם Cohere: מודלים טובים בשפה, לא בידע | Yuval Avidani | 2024-11-30 | מודלי שפה טובים בחיקוי דיבור, לא בידע. לכן החוכמה היא לצרף הקשר נכון: חיפוש, Re-Ranking ו-Embeddings רב-לשוניים (כולל עברית) של Cohere. |
| [A0010](../../items/A0010.md) | Mixpeek: pipeline נתונים מולטימודלי ל-RAG (פיץ' של מייסד) | The Feedback Loop (Ethan Steininger, Mixpeek) | 2024-11-17 | פיץ' של דקה: Mixpeek מחבר לכל DB, מזרים שינויים דרך מודלי ML ומוציא embeddings ו-metadata ליעד, בשביל אפליקציות RAG. |

⚠️ = תוכן חלקי (וידאו לא תומלל או מקור חסום) · 🔸 = מעט תוכן
