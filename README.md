#  نموذج ذكاء اصطناعي لإضافة علامات الترقيم للنصوص العربية
(AI Model for Punctuation Restoration in Arabic Texts)

##  فريق العمل
* **محمد عبد الرزاق كركوتلي**[cite: 1]
* **نعمات بلال اسعد**[cite: 1]
* **احمد الحاتي**[cite: 1]

##  نظرة عامة
يهدف هذا المشروع إلى بناء وتقييم نماذج تعلم عميق قادرة على فهم السياق الدلالي وإضافة علامات الترقيم تلقائياً إلى النصوص العربية. يتضمن المشروع بناء وتدريب وتقييم نموذجين أساسيين:
1. **نموذج AraBERT:** بالاعتماد على النسخة (`aubmindlab/bert-base-arabertv02`) لمهام التصنيف المقطعي (Token Classification)[cite: 1].
2. **نموذج Bi-LSTM:** مع طبقة تضمين الكلمات (Embedding) ونظام القناع (Masking) لتجاهل حشو البيانات[cite: 2].

##  الأكواد البرمجية (Notebooks)
* `AraBERT_Punctuation_Evaluation.ipynb`: دفتر ملاحظات مخصص لتحميل أوزان نموذج AraBERT وتقييم الأداء النهائي وعرض مصفوفة الارتباك (Confusion Matrix)[cite: 1].
* `BiLSTM_Data_Processing_and_Training.ipynb`: دفتر ملاحظات يتضمن خطوات تنظيف النصوص واستخراجها، وحساب أوزان الفئات للتعامل مع عدم توازن البيانات، بالإضافة إلى تدريب نموذج Bi-LSTM[cite: 2].

##  الموارد والبيانات الضخمة (Large Files & Datasets)
نظراً لحجم البيانات وأوزان النماذج الكبيرة التي تتجاوز حد الرفع المسموح به في GitHub، تم رفع الملفات عبر الروابط المباشرة التالية:
* **المجلد الشامل للمشروع (Google Drive):** [مجلد المشروع الكامل](https://drive.google.com/drive/folders/1GtHnuipzHX9RzFNCNXn9a2MhQeMtF1Nx) (يحتوي على كافة النماذج المدربة والصور البيانية والملفات الضخمة).
* **أوزان الموديل (AraBERT):** [تحميل ملف الأوزان](https://drive.usercontent.google.com/download?id=1hpfXnJ3aSklcMe6wai_YVGfK_Otb24f5&authuser=0)[cite: 1].
* **مجموعة البيانات (Dataset):** يتم استخدام مجموعة بيانات `SSAC-UNPC`، ويمكنك تحميلها عبر [هذا الرابط](https://data.mendeley.com/public-files/datasets/2pkxckwgs3/files/4f402c76-388e-4bde-b887-f1be522001db/file_downloaded)[cite: 2].

## استراتيجية التنقيب ومعالجة البيانات
للتغلب على التباين الإحصائي الكبير بين الفئات (Class Imbalance) وهيمنة فئة "الكلمات بدون ترقيم" (NO_PUNCT)، تم تطبيق تقنية موازنة البيانات (Under-sampling Strategy)[cite: 2]. يتم الاحتفاظ بكامل الجمل التي تحتوي على علامات الترقيم النادرة (مثل علامات التعجب والاستفهام) لضمان تعلم السياق، في حين يتم أخذ عينات عشوائية مخفضة من الكلمات العادية[cite: 2]."# -AImodel-for-adding-punctuation-to-Arabic-texts" 
