# 🎲 Israeli Lottery Data Archive

**ארכיון מלא של תוצאות הגרלות ישראליות ממקורות רשמיים בלבד**

## 📋 סקירה

מאגר נתונים היסטורי מקיף של כל ההגרלות שנערכו בישראל, כולל:
- **מפעל הפיס**: לוטו, צ'אנס, 777, 123
- **ספורטוטו**: ווינר, טוטו

### ✅ עקרונות המערכת
1. **מקורות רשמיים בלבד** - כל נתון מגיע ממקור רשמי מאומת
2. **שקיפות מלאה** - כל הגרלה כוללת קישור למקור
3. **אימות אינטגריטי** - checksum לכל רשומה
4. **עדכון אוטומטי** - GitHub Actions מעדכן יומית

## 📂 מבנה הנתונים

```
datasets/
├── _meta/
│   ├── coverage.json      # כיסוי נתונים - תאריכים, חוסרים
│   └── sources.json       # מקורות רשמיים לכל משחק
├── pais/
│   ├── lotto/            # לוטו - מפעל הפיס
│   ├── chance/           # צ'אנס - מפעל הפיס
│   ├── 777/              # 777 - מפעל הפיס
│   └── 123/              # 123 - מפעל הפיס
└── sportoto/
    ├── winner/           # ווינר
    └── toto/             # טוטו
```

## 📊 פורמט הנתונים

כל הגרלה נשמרת בפורמט NDJSON (JSON per line):

```json
{"draw_id":"4567","date":"2026-02-17","numbers":[7,14,21,28,35,42],"bonus":[3],"source":"https://www.pais.co.il/lotto/archive.aspx","checksum":"a3f5d2c1"}
```

## 🔄 עדכניות

המערכת מתעדכנת אוטומטית באמצעות GitHub Actions.
לצפייה בסטטוס העדכניות: [`datasets/_meta/coverage.json`](datasets/_meta/coverage.json)

## 🔗 קישורים

- [Backend API](https://github.com/ubriga/lottery-platform-backend)
- [Frontend Dashboard](https://github.com/ubriga/lottery-platform-frontend)
- [מקורות רשמיים](datasets/_meta/sources.json)

## 📜 רישיון

נתונים ממקורות ציבוריים רשמיים. השימוש במאגר זה הוא למטרות מחקר ואנליזה בלבד.

---

**⚠️ הערה חשובה**: הגרלות הן אקראיות לחלוטין. נתונים היסטוריים אינם מאפשרים ניבוי תוצאות עתידיות.
