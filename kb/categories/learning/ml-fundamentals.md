# משאבי למידה (Learning resources) › יסודות ML ו-Deep Learning

[← משאבי למידה (Learning resources)](README.md) · [ראשי](../../README.md) · 18 פריטים

## סינתזה

**יסודות:** 3Blue1Brown [A0044](../../items/A0044.md) [A0286](../../items/A0286.md) [A0020](../../items/A0020.md), Karpathy (מבוא ל-LLMs [A0059](../../items/A0059.md), nanochat [A0527](../../items/A0527.md)), Neural Networks from Scratch [A0004](../../items/A0004.md) [A0024](../../items/A0024.md) [A0043](../../items/A0043.md), רשתות ב-JavaScript [A0081](../../items/A0081.md), ו-TensorFlow Playground [A0050](../../items/A0050.md).
**מושגים שחוזרים בחדשות:** Mixture of Experts [A0984](../../items/A0984.md), fine-tuning [A0437](../../items/A0437.md) [A0564](../../items/A0564.md), RL [A0118](../../items/A0118.md), וההבחנה בין מודל, harness ותזמור [A0875](../../items/A0875.md).
**להרצאה:** חמשת אלגוריתמי ה-ML על אותו גרף [A1067](../../items/A1067.md) הם המחשה טובה לקהל לא טכני.

**כלים בולטים בתת-הקטגוריה:** NNFS book (3), NumPy (2), (none) (1), Mixtral (1), DeepSeek-V3 (1), Llama 4 (1), Claude Code (1), Azure AI Foundry (1), GPT-4o (1), nanochat (1), Cohere (1), GPT-3 (1)

## פריטים

| ID | כותרת | מחבר | תאריך | תקציר |
|---|---|---|---|---|
| [A1067](../../items/A1067.md) | חמישה אלגוריתמי ML על אותו גרף: רגרסיה לינארית, לוגיסטית, עץ החלטה, SVM ו-KNN | RickTheEngineer | 2026-08-28 | רגרסיה לינארית מותחת את הקו הטוב ביותר, למשל זמן משלוח לפי מרחק. לוגיסטית: עקומת S להסתברות. עץ החלטה: חלוקות ל"מדרגות". SVM: גבול עם מרווח מקסימלי… |
| [A0984](../../items/A0984.md) | מה זה Mixture of Experts? Router שבוחר top-k מומחים לכל טוקן: ענק בזיכרון, קטן בפעולה | רני אלבג ויין | 2026-07-20 | **מהשקופיות:** במודל dense, כל טוקן מפעיל את כל הפרמטרים. ב-MoE יש רשתות "מומחים" קטנות, ו-router בכל שכבה נותן ציון לכל מומחה ומפעיל רק את המובילים… |
| [A0875](../../items/A0875.md) | מודל, harness ושכבת orchestration: ההבדל, בהסבר פשוט | James Goldbach | 2026-05-30 | מודל הוא רשת שחוזה את הטוקן הבא. סוכן או harness עוטף את המודל בלולאה ונותן לו כלים: המודל פולט בלוק טקסט של "אני רוצה להשתמש בכלי", וקוד רגיל של… |
| [A0564](../../items/A0564.md) | Fine-tuning ל-GPT-4o בלי קוד ב-Azure AI Foundry: דאטה בפורמט, suffix, deploy ומחיקה | Mariana Antaya | 2026-01-16 | ב-Azure AI Foundry (בגרסה הישנה) בוחרים Fine-tuning ומודל בסיס, GPT-4o. החלק הכי חשוב הוא הדאטה: דוגמאות בפורמט הנדרש לתחום שלכם. מוסיפים suffix כדי… |
| [A0527](../../items/A0527.md) | nanochat של Karpathy: "ה-ChatGPT הכי טוב שאפשר לקנות ב-100$" | גיקטיים | 2025-10-18 | Karpathy (שטבע את "Vibe Coding") שחרר את nanochat, כ-8,000 שורות קוד פתוח שמאמנות צ'אטבוט מאפס עם UI דמוי ChatGPT: כ-4 שעות על 8xH100 (כ-100$). 12… |
| [A0437](../../items/A0437.md) | מה זה Fine-tuning? מדריך (Cohere) | Cohere | 2025-08-03 | מדריך של Cohere: fine-tuning מתאים LLM מאומן למשימות או לדאטה ספציפיים. הטקסט שנשמר הוא בעיקר ניווט, אז הסיכום כולל רקע כללי. |
| [A0286](../../items/A0286.md) | Transformers, הטכנולוגיה שמאחורי LLMs (3Blue1Brown, פרק 5) | 3Blue1Brown (Grant Sanderson) | 2025-06-07 | הסבר ויזואלי מופתי (27 דק'): GPT = Generative Pre-trained Transformer. חיזוי טוקן הבא ודגימה בלולאה, embeddings (וקטורים עם כיוונים סמנטיים),… |
| [A0181](../../items/A0181.md) | פריסת מודל ל-AWS SageMaker בארבעה שלבים, והכי חשוב: לכבות endpoints | Reshad | 2025-03-27 | כדי לבנות אפליקציית AI על מודל משלכם, פורסים אותו לשירות ענן כמו AWS SageMaker. כותבים סקריפט שמוריד את המודל ופורס endpoint. שלב 4, "החשוב ביותר":… |
| [A0118](../../items/A0118.md) | לאמן AI לשחק Flappy Bird עם Reinforcement Learning (Gymnasium) | Yuval Avidani | 2025-01-24 | היכרות עם RL דרך Gymnasium (לשעבר OpenAI Gym): מודל לומד לבד לשחק Flappy Bird ממערכת של תגמולים וקנסות. |
| [A0081](../../items/A0081.md) | רשתות נוירונים ב-JavaScript פשוט (יונתן קרא, JavaScript Israel) | Yonatan Kra (JavaScript Israel Meetup) | 2024-12-29 | הרצאה בעברית (מיטאפ 27.6.2024): בונים רשת נוירונים מאפס ב-JavaScript בלי אלגברה ליניארית כבדה, מבינים "מה גורם לה לעבוד" ואיך משלבים NN באפליקציה. |
| [A0059](../../items/A0059.md) | Andrej Karpathy: הרצאת מבוא של שעה ל-LLMs | Andrej Karpathy | 2024-12-15 | ההרצאה הקלאסית: LLM הוא "שני קבצים", pretraining כדחיסת האינטרנט, fine-tuning לעוזר, scaling laws, כלים, LLM OS ואיומי אבטחה (jailbreak, prompt… |
| [A0050](../../items/A0050.md) | TensorFlow Neural Network Playground | Google (Daniel Smilkov, Shan Carter) | 2024-12-07 | סימולטור אינטראקטיבי בדפדפן: בוחרים dataset, features, שכבות, אקטיבציה ו-learning rate ורואים את הרשת לומדת בזמן אמת. |
| [A0043](../../items/A0043.md) | בניתי רשת נוירונים מאפס (NumPy בלבד) | Green Code | 2024-12-01 | סרטון של 9 דקות: מנוירון יחיד (סכום משוקלל + bias) לשכבות, אקטיבציות ו-backprop, ובדיקה על MNIST ו-Fashion-MNIST. |
| [A0044](../../items/A0044.md) | 3Blue1Brown: מה זה בעצם רשת נוירונים? (Deep learning פרק 1) | 3Blue1Brown | 2024-12-01 | ההסבר הוויזואלי הקלאסי: רשת לזיהוי ספרות 28x28, נוירון = מספר בין 0 ל-1, שכבות, משקלים, biases, sigmoid מול ReLU. |
| [A0024](../../items/A0024.md) | הספר Neural Networks from Scratch in Python | Harrison Kinsley (sentdex) & Daniel Kukieła | 2024-11-22 | הספר שמלווה את סדרת sentdex: בניית רשתות נוירונים בלי ספריות, בפורמט מודפס ו-e-book עם גישה לטיוטה ולתגובות. |
| [A0020](../../items/A0020.md) | Large Language Models explained briefly | 3Blue1Brown (Grant Sanderson) | 2024-11-20 | הסבר ויזואלי של 8 דקות: LLM חוזה את המילה הבאה, pretraining על כמויות טקסט אדירות, RLHF, transformers ו-attention. |
| [A0012](../../items/A0012.md) | מה זה רשתות נוירונים? (שיעור מבוא ל-Deep Learning, בעברית) | Nissan Courses | 2024-11-17 | שיעור בעברית מקורס ML ב-Python: השראה מהמוח, נוירון, שכבות נסתרות, ולמה "Deep" Learning. |
| [A0004](../../items/A0004.md) | Neural Networks from Scratch, חלק 1: מבוא וקוד של נוירון | sentdex (Harrison Kinsley) | 2024-11-15 | סדרת YouTube שבונה רשת נוירונים מאפס ב-Python (בלי ספריות, אחר כך NumPy); פרק 1 מסביר נוירון יחיד ומשקלים/bias. |

⚠️ = תוכן חלקי (וידאו לא תומלל או מקור חסום) · 🔸 = מעט תוכן
