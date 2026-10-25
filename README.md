# دليل الموردين في مصر · Egypt Supplier Directory

**إعداد: م. محمد الرفاعي · هاتف ‎+20 106 736 8265**
**Prepared by Eng. Mohamed Elrefay · Phone +20 106 736 8265**

دليل مفتوح ثنائي اللغة (عربي / إنجليزي) للمصنّعين والموزعين والوكلاء الرسميين ومقدمي الصيانة في مصر، والشركات الأجنبية التي لها شركاء في مصر، مع ما يمكن تصنيعه من كل خامة.

An open, bilingual (Arabic / English) directory of manufacturers, distributors, official agents and maintenance providers in Egypt, the foreign companies that have partners in Egypt, and what can be manufactured from each raw material.

## المحتوى · Contents

| | |
|---|---|
| **القطاعات · Sectors** | البناء والتشييد، الإلكترونيات وتكنولوجيا المعلومات، الخامات، البلاستيك، المطاط، الطرق والسباكة، الزجاج، الأخشاب والألواح، الإكسسوارات والخردوات، الماكينات والمعدات، الصيانة والخدمات |
| **لكل مورد · Per supplier** | الاسم، المنتجات، نوع المورد، المسؤول، الهواتف وحالتها، العنوان، الموقع الرسمي، الفروع، الشركاء، المصدر |
| **الشركات الأجنبية · Foreign companies** | البلد، المنتجات، الموقع الرسمي، شركاؤها في مصر ودورهم (شركة تابعة، وكيل، موزع، شريك صيانة…) |

## الملفات · Files

- `index.html`: التطبيق كاملًا، يعمل في أي متصفح · the full app; opens in any browser
- `snapshot.json`: البيانات التي يقرؤها التطبيق · the data the app reads
- `data/suppliers.json`, `data/suppliers.csv`: الموردون · suppliers (the CSV opens in Excel)
- `data/foreign-companies.json`, `data/foreign-companies.csv`: الشركات الأجنبية وشركاؤها في مصر · foreign companies and their Egyptian partners

## التشغيل · Run it

افتح `index.html` من خلال أي خادم ويب، أو فعّل GitHub Pages لهذا المستودع (Settings → Pages → Deploy from branch → `main` / root).
Serve the folder with any web server, or turn on GitHub Pages for this repository (Settings → Pages → Deploy from branch → `main` / root).

```bash
python3 -m http.server 8000   # then open http://localhost:8000
```

## مصادر البيانات · Data sources

البيانات مجمّعة من مواقع الشركات الرسمية، وقوائم الوكلاء والموزعين، والإفصاحات، والأدلة التجارية العامة (مثل الصفحات الصفراء مصر، Kompass، اتحاد الصلب العربي، جمعية رجال الأعمال المصريين). لا تُسجَّل أرقام هواتف إلا إذا وُجدت في مصدر منشور، ويوضح حقل `phoneStatus` مصدر الرقم:
`official` = من الشركة نفسها، `directory` = من دليل أعمال (يُفضّل التأكد)، `missing` = لم يُعثر عليه بعد.

Collected from official company sites, distributor/dealer lists, filings and public business directories. Phone numbers are recorded only when found in a published source. `phoneStatus` says where a number came from: `official` (the company itself), `directory` (a business directory; worth a confirming call) or `missing` (not found yet). Each record carries its `source` and `sourceUrl`.

## الترخيص · License

- الكود · Code: MIT
- البيانات · Data: CC BY 4.0. Please credit "Egypt Supplier Directory, Eng. Mohamed Elrefay".

للتصحيح أو الإضافة افتح Issue أو Pull Request. Corrections and additions are welcome as issues or pull requests.
