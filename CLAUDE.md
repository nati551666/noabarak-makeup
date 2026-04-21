# נועה ברק — אתר מאפרת מקצועית

## סקירת הפרויקט
אתר דף יחיד (`index.html`) עבור נועה ברק, מאפרת מקצועית. האתר בנוי בעברית RTL עם עיצוב יוקרתי בצבעי ורוד/זהב.

## מבנה הפרויקט
```
נעה אתר/
├── index.html        # כל הקוד — CSS + HTML + JS בקובץ אחד
├── noa1.jpg          # תמונה לסקשן "אודות" (צריך להוסיף)
└── noa2.jpg          # תמונה ל-Hero (צריך להוסיף)
```

## טכנולוגיות
- HTML/CSS/JS ונילה בלבד — ללא פריימוורק
- גופנים: Playfair Display (כותרות), Assistant (גוף)
- RTL מלא (`lang="he" dir="rtl"`)

## עיצוב — Design Tokens
| משתנה | ערך | שימוש |
|--------|-----|--------|
| `--rose` | `#c9738a` | צבע ראשי |
| `--gold` | `#c9a96e` | הדגשות |
| `--cream` | `#fffbfc` | רקע בהיר |
| `--dark` | `#120b0f` | רקע כהה |

## סקשנים
1. **Hero** — תמונה + טקסט + מונים אנימציה
2. **About** — split dark עם ציטוט
3. **Services** — Bento Grid עם מחירים
4. **Courses** — 2 קורסים (אישי 1,200₪ / מקצועי 3,000₪)
5. **AI Chat** — יועצת נועה, קורא ל-Anthropic API ישירות מהדפדפן
6. **Testimonials** — 3 כרטיסיות
7. **CTA** — WhatsApp + Instagram
8. **Footer**

## פרטי קשר (חשוב)
- WhatsApp: `972559569455`
- Instagram: `noa_barak_makeup`

## AI Chat
קורא ל-`https://api.anthropic.com/v1/messages` ישירות מה-JS בצד הלקוח.  
מודל: `claude-sonnet-4-20250514`  
**שים לב:** ה-API key חייב להיות מוגדר — כרגע אין מנגנון לכך בקוד. בפרודקשן צריך backend proxy.

## הערות לפיתוח
- תמונות `noa1.jpg` ו-`noa2.jpg` מוצגות עם fallback אוטומטי אם לא קיימות
- כל האנימציות מבוססות `IntersectionObserver`
- Cursor מותאם אישית — `cursor: none` על כל ה-body
