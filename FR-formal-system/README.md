<<<<<<< HEAD
# FR — تعاریف رسمی (Formal Definitions)

**منبع:** جنت‌خواه دوست، *نظریه آزادی، ایران و دین* (۱۴۰۵)
**روش:** استخراج مستقیم از متن + صورت‌بندی منطقی

---

## اصل صورت‌بندی

هر تعریف FR سه لایه دارد:
1. **متن اصلی** — نقل مستقیم از کتاب
2. **صورت منطقی** — فرمول‌بندی رسمی
3. **نتیجه** — آنچه از تعریف مشتق می‌شود

---

## D1 — آزادی (Freedom)

**متن کتاب:**
> «آزادی، در صورت عینی خود، چیزی جز حقوق مالکیت فردی نیست.»
> «آزادی باید به امری قابل توافق، قابل سنجش و قابل صورت‌بندی تبدیل شود.»

**صورت منطقی:**
```
Freedom(x) ≡ ∀y ∈ Domain(x): Property(x, y) ∧ ¬Coerce(any, x)

Domain(x) = {
  body(x),     — بدن
  will(x),     — اراده
  time(x),     — زمان
  labor(x),    — کار
  honor(x),    — آبرو
  family(x),   — خانواده
  contract(x), — قرارداد
  land(x),     — زمین
  output(x),   — دستاورد
  responsibility(x) — مسئولیت
}
```

**نتیجه:**
- آزادی objective است (قابل توافق بین‌الاذهانی) نه subjective
- نقض هر عنصر Domain(x) = نقض آزادی x
- تعریف subjective از آزادی = ابزار بردگی در دست قدرت

---

## D2 — مالکیت (Property)

**متن کتاب:**
> «مالکیت در این کتاب فقط مالکیت بر مال نیست؛ مالکیت بر بدن، جان، اراده، زمان، کار، آبرو، خانواده، قرارداد، زمین، دستاورد و مسئولیت است.»

**صورت منطقی:**
```
Property(x, y) is primitive for y = body(x)          [A1 — خودمالکیتی اولیه]

Property(x, y) is derived iff:
  Labor(x, y) ∧ ¬Prior_Claim(y)                      [A3 — اشتقاق از کار]
  ∨ Transfer(z, y, x) ∧ Transfer_Valid(z, y, x)       [A4 — انتقال معتبر]
```

**مراتب مالکیت (از پایه به مشتق):**
```
Tier 0: Property(x, body(x))         — اولیه، غیرمشتق
Tier 1: Property(x, labor(x))        — از Tier 0 مشتق می‌شود
Tier 2: Property(x, output(labor(x))) — از Tier 1 مشتق می‌شود
Tier 3: Property(x, transferred(y))  — از Transfer معتبر مشتق می‌شود
```

**نتیجه:**
- انکار Tier 0 = انکار همه مراتب
- دولتی که Labor(x) را مصادره می‌کند = نقض Tier 1

---

## D3 — اجبار (Coercion)

**متن کتاب:**
> [ضمنی از سرتاسر کتاب — سه صورت]

**صورت منطقی:**
```
Coerce(z, x) ≡ C_physical(z, x) ∨ C_desperation(z, x) ∨ C_epistemic(z, x)

C_physical(z, x):
  z threatens or applies force → changes action-set of x

C_desperation(z, x):
  z reduces Options(x) → {only_one_option}
  ∴ consent(x) is void — "اجبار از جنس ضرورت"

C_epistemic(z, x):
  z withholds or distorts Information(x)
  ∴ consent(x) is based on false model of world — "اجبار معرفتی"
```

**قانون مشروعیت:**
```
Consent(x, action) is FR-valid iff:
  ¬Coerce(any, x) at time of consent
  Options(x) ≥ 2 at time of consent
  Information(x) ≈ complete at time of consent
```

**نتیجه:**
- رأی اکثریت تحت C_epistemic = consent void
- قرارداد تحت C_desperation = قرارداد باطل
- «رضایت داوطلبانه» بدون Options ≥ 2 = اکراه پنهان

---

## D4 — دین (Religion — تعریف FR)

**متن کتاب:**
> «دین یعنی نظام صوری منسجم اصل موضوعی برای آزادی و حقوق مالکیت فردی که بند بندش عقل و منطق و استدلال است.»
> «دین حقیقی، پیمان آزادی است.»
> «دین، اگر درست فهمیده شود، نظام تعیین حدود مالکیت است.»

**صورت منطقی:**
```
Religion_FR(R) ≡ FormalSystem(R) ∧
  Axioms(R) ⊨ Property_Rights(all individuals) ∧
  Axioms(R) ⊨ ¬Coerce(any, any) ∧
  R does not claim State_Exemption(R) from A6 ∧
  R is consistent (non-contradictory internally)
```

**معیار تشخیص دین اصیل از دین کنترلی:**
```
Religion_legitimate(R) iff:
  R enforces property rights for ALL individuals including non-believers
  R competes in open market of ideas (no monopoly claim)
  R does not require State enforcement of its rules
  ¬(R claims exclusive access to truth not verifiable by others)
```

**نتیجه:**
- «لا اکراه فی الدین» = تعریف دین از درون؛ هر دینی که اکراه بخواهد ضد خودش است
- دین دولتی = خودنقض (self-refuting)
- دین اصیل = سپر مردم در برابر دولت، نه ابزار دولت

---

## D5 — عرفان (Mysticism — تعریف FR)

**متن کتاب:**
> «عرفان در این کتاب نام هر دستگاهی است که انسان را از مالکیت، بدن، زمین، عقل، وحی و آزادی جدا کند و او را به اطاعت از یک کل مبهم بسپارد: مرشد، دولت، تاریخ، طبقه، امت، ملت، روح جهان، دیالکتیک، حزب یا ایدئولوژی.»
> «معیار تشخیص آن ساده است: هرجا مالکیت انسان، آزادی انسان، اراده آزاد انسان... تحقیر شود، با صورتی از عرفان ضدآزادی روبه‌رو هستیم.»

**صورت منطقی:**
```
Mysticism_FR(M) ≡ ∃C (Collective(C)) such that:
  M claims: Property(individual, x) → Property(C, x)
  ∨ M claims: Will(individual) → Will(C)
  ∨ M dissolves individual identity into C

Collective(C) includes:
  State, Nation, Class, Ummah, History, Dialectic,
  Party, Master (مرشد), Race, Ideology, World-Spirit
```

**شناسه عرفان در هر لباس:**
```
detect_mysticism(system S):
  if S.deprecates(material_world) → flag
  if S.dissolves(individual, collective) → flag
  if S.claims(inner_revelation > public_reasoning) → flag
  if S.requires(obedience_to_hierarchy) without property_justification → flag
  return FR_MYSTICAL_COLLAPSE
```

**نتیجه:**
- هگل، مارکس، گنوسیسم، وحدت وجود، دولت مدرن — همه instance‌های یک pattern
- عرفان = نرم‌افزار تاریخی نابودی آزادی (جمله خود نویسنده)
- فلسفه اسلامی (ابن‌عربی، ملاصدرا، سهروردی) = بازنسخه همان pattern

---

## D6 — دولت (State — تعریف FR)

**متن کتاب:**
> «دولت در این نظریه، نه صرفاً یک سازمان اداری، بلکه نهادی است که اگر مهار نشود، به بزرگترین ناقض حقوق مالکیت فردی تبدیل می‌شود.»
> «دولت ابتدا زندگی عادی انسان را جرم‌خیز می‌کند، سپس مردم را مجرم بالقوه نشان می‌دهد، و بعد برای نجات مردم از ناامنی‌ای که خود ساخته، قدرت، بودجه و اطاعت بیشتری مطالبه می‌کند.»

**صورت منطقی:**
```
State_FR(S) ≡ Organization(S) that claims:
  Monopoly on legitimate force within territory T
  Authority to define what is criminal in T
  Right to extract resources from individuals in T

State_legitimate(S) iff:
  Function(S) ⊆ {Enforce(A6), Adjudicate(disputes), Defend(territory)}
  ∧ ¬Tax(S, Labor(x)) beyond commons_maintenance_threshold
  ∧ ¬Monopolize(S, {education, health, currency, religion})
  ∧ Exit(individual, S.territory) is possible

State_illegitimate(S) iff:
  ∃ function ∈ Function(S) \ legitimate_functions
  → FR-STATE-OVERREACH
```

**مکانیزم توسعه دولت:**
```
State_expansion_cycle:
  1. Criminalize(ordinary_behavior)
  2. Generate(fear, insecurity)
  3. Present(S) as solution to fear S created
  4. Demand(more_power, more_budget, more_obedience)
  5. goto 1
```

**نتیجه:**
- تقوای سیاستمدار = اندازه دولتی که تحویل می‌دهد کمتر از آنچه تحویل گرفت
- دولت رفاه = دین جعلی که وعده بهشت زمینی می‌دهد
- مالیات بر کار = جریمه خلاقیت = نقض D2/Tier 1

---

## D7 — قرارداد (Contract)

**متن کتاب:**
> «مسئله، اخلاق‌گرایی مبهم نیست؛ قرارداد، رضایت، و عقل سلیم است.»
> «انتقال داوطلبانه و قراردادی» به‌عنوان تنها مسیر مشروع انتقال مالکیت.

**صورت منطقی:**
```
Contract(x, y, terms) is FR-Valid iff:
  (i)  Property(x, subject_of_contract)          — x چیزی را که ندارد نمی‌تواند ببخشد
  (ii) Consent(x) ∧ ¬Coerce(any, x)              — رضایت واقعی x
  (iii) Consent(y) ∧ ¬Coerce(any, y)             — رضایت واقعی y
  (iv) Information(x) ≈ Information(y)           — عدم تقارن اطلاعاتی مادی
  (v)  Options(x, post) ≥ Options_min             — x بعد از قرارداد زنده می‌ماند
  (vi) Options(y, post) ≥ Options_min             — y بعد از قرارداد زنده می‌ماند
  (vii) Exit(x, contract) possible without catastrophic_cost
  (viii) Exit(y, contract) possible without catastrophic_cost
```

**انواع قرارداد باطل:**
```
Contract_void if:
  C_desperation at time of signing → (vii) or (viii) violated
  C_epistemic at time of signing   → (iv) violated
  Subject not owned by x           → (i) violated
  State compels terms               → (ii) or (iii) violated
```

---

## D8 — سلام (Salutation — تعریف FR)

**متن کتاب:**
> «سلام، اعلام صلح مالکانه است: من به جان، مال، بدن، اراده، آبرو و مالکیت تو تعرض نمی‌کنم، و تو نیز همین پیمان را می‌پذیری.»

**صورت منطقی:**
```
Salam(x → y) ≡ Contract_declaration:
  ¬Coerce(x, y)  [x اعلام می‌کند]
  ∧ x recognizes Property(y, Domain(y))
  ∧ x expects Salam(y → x) as reciprocal

Salam_as_pact ≡ bilateral_Contract(x, y, {
  ¬Coerce(x, y),
  ¬Coerce(y, x),
  Recognize_Property(x, Domain(y)),
  Recognize_Property(y, Domain(x))
})
```

**نتیجه:**
- سلام = کوچکترین قرارداد آزادی ممکن
- نقض مالکیت بعد از سلام = نقض contract صریح
- «اسلام» = تسلیم در برابر این پیمان (نه تسلیم در برابر قدرت)

---

## D9 — قاعده تسلیط (Rule of Dominion)

**متن کتاب:**
> «قاعده تسلیط؛ صورت دینی آزادی»
> «الناس مسلطون علی اموالهم» — مردم بر اموال خود مسلطند.

**صورت منطقی:**
```
Taslit(x, y) ≡ Property(x, y) →
  x has_right_to: Use(y) ∧ Transform(y) ∧ Transfer(y) ∧ Defend(y)
  ∧ ¬any_authority can override without x's consent

Taslit_principle:
  ∀x, y: Property(x, y) → Taslit(x, y)
  State_Exception: ∄
  Religious_Exception: ∄
  Majority_Exception: ∄
```

**نتیجه:**
- «خوردن مال مردم به باطل، حتی با واسطه حاکم، مشروع نمی‌شود» = قاعده تسلیط در برابر دولت
- هر مصادره دولتی = نقض قاعده تسلیط = FR-PROPERTY-VOID

---

## D10 — دیالکتیک (Dialectic — تعریف FR)

**متن کتاب:**
> «دیالکتیک بهمثابه پرده‌ای بر یک دین پنهان»
> «رد دیالکتیک با یک آیه»
> «دیالکتیک، قربانی می‌خواهد»

**صورت منطقی:**
```
Dialectic_FR(D) ≡ Logic(D) such that:
  D allows: P ∧ ¬P → Synthesis(P, ¬P) = P'
  where P' justifies violation of A1 or A6

In FR:
  ¬(P ∧ ¬P)  [law of non-contradiction — absolute]

Therefore:
  Dialectic_FR ⊨ contradiction
  → Any policy justified by dialectical logic is FR-INVALID
  → Label: FR-DIALECTIC-TRAP
```

**نمونه‌های دیالکتیک در عمل:**
```
"مالکیت فردی (P) و برابری (¬P) → مالکیت جمعی (P')"  — کمونیسم
"آزادی (P) و امنیت (¬P) → دولت ناظر (P')"           — لیبرالیسم مدرن
"دین (P) و دولت (¬P) → دولت دینی (P')"              — ولایت مطلقه
```

**نتیجه:**
- هر استدلالی که از تضاد به ترکیب می‌رسد و توجیه تصرف مالکیت می‌کند = FR-DIALECTIC-TRAP
- منطق FR: linear, axiomatic, non-contradictory (مانند هندسه اقلیدسی)

---

## D11 — توحید (Monotheism — تعریف FR)

**متن کتاب:**
> «توحید بهمثابه اصل تضمین آزادی»
> «کسی که آتئیست است... اگر دیگران را به بندگی نگیرد، مسئله‌ای علیه آزادی ایجاد نمی‌کند.»

**صورت منطقی:**
```
Tawhid_FR ≡ ∄ authority_x such that:
  x claims absolute_sovereignty over individual(y)
  ∧ x ≠ God

Corollary_1: State(S) claiming absolute sovereignty → shirk (بت‌پرستی مدرن)
Corollary_2: Master(M) claiming sovereignty over follower → shirk
Corollary_3: Atheist who respects Property(others) → functionally compatible with FR
```

**نتیجه:**
- توحید = نفی هر ارباب غیرخدا = اصل آزادی فردی
- «کفر» در FR = کسی که دیگران را به بندگی می‌گیرد، نه کسی که خدا را باور ندارد
- دولت‌پرستی = شرک (از منظر FR)

---

## D12 — معاد (Eschatology — تعریف FR)

**متن کتاب:**
> «معاد، دزدی، و ناپایداری آزادی در جهان بی‌خدا»
> ربط به نظریه بازی‌ها: «مشکل دست آخر» (Last Round Problem)

**صورت منطقی:**
```
Last_Round_Problem:
  In finite game G with known end-time T:
    Rational_agent(x) at T: defect (steal) if P(punishment) → 0
    Backward induction: defect at T-1, T-2, ... → Nash equilibrium = steal

Maad_solution:
  Game G has no known end-time ∨ punishment persists beyond death
  → P(punishment) > 0 for all rounds including last
  → Defect is no longer dominant strategy
  → Cooperation becomes rational
```

**نتیجه:**
- بدون معاد، جامعه آزاد ناپایدار است (مشکل game-theoretic)
- معاد = ابزار حل مشکل دست آخر در نظریه بازی‌ها
- رفاه دولتی = جایگزین موقت معاد که منابع را تمام می‌کند

---

## جدول خلاصه تعاریف

| مفهوم | تعریف FR | نقیض FR |
|-------|----------|---------|
| آزادی | Property(x, Domain(x)) ∧ ¬Coerce | تعریف subjective آزادی توسط قدرت |
| مالکیت | Self-ownership + Labor-derivation + Valid-transfer | مصادره، مالیات بر کار، ملی‌سازی |
| اجبار | Physical ∨ Desperation ∨ Epistemic | «رضایت داوطلبانه» زیر فشار |
| دین | Formal system for property rights | دین دولتی، دین اجباری |
| عرفان | هر سیستمی که فرد را در جمع حل کند | — |
| دولت | سازمان انحصار قوه قاهره | دولت محدود مشروع |
| قرارداد | 8 شرط، exit ممکن | قرارداد اضطراری، اطلاعات نامتقارن |
| سلام | کوچکترین قرارداد آزادی | تعارف بدون commitment |
| تسلیط | حق کامل بر مال خود | استثنا برای دولت یا دین |
| دیالکتیک | P ∧ ¬P → P' برای توجیه تصرف | منطق خطی، آکسیوماتیک |
| توحید | نفی هر ارباب غیرخدا | شرک = دولت‌پرستی |
=======
# FR — تعاریف رسمی (Formal Definitions)

**منبع:** جنت‌خواه دوست، *نظریه آزادی، ایران و دین* (۱۴۰۵)
**روش:** استخراج مستقیم از متن + صورت‌بندی منطقی

---

## اصل صورت‌بندی

هر تعریف FR سه لایه دارد:
1. **متن اصلی** — نقل مستقیم از کتاب
2. **صورت منطقی** — فرمول‌بندی رسمی
3. **نتیجه** — آنچه از تعریف مشتق می‌شود

---

## D1 — آزادی (Freedom)

**متن کتاب:**
> «آزادی، در صورت عینی خود، چیزی جز حقوق مالکیت فردی نیست.»
> «آزادی باید به امری قابل توافق، قابل سنجش و قابل صورت‌بندی تبدیل شود.»

**صورت منطقی:**
```
Freedom(x) ≡ ∀y ∈ Domain(x): Property(x, y) ∧ ¬Coerce(any, x)

Domain(x) = {
  body(x),     — بدن
  will(x),     — اراده
  time(x),     — زمان
  labor(x),    — کار
  honor(x),    — آبرو
  family(x),   — خانواده
  contract(x), — قرارداد
  land(x),     — زمین
  output(x),   — دستاورد
  responsibility(x) — مسئولیت
}
```

**نتیجه:**
- آزادی objective است (قابل توافق بین‌الاذهانی) نه subjective
- نقض هر عنصر Domain(x) = نقض آزادی x
- تعریف subjective از آزادی = ابزار بردگی در دست قدرت

---

## D2 — مالکیت (Property)

**متن کتاب:**
> «مالکیت در این کتاب فقط مالکیت بر مال نیست؛ مالکیت بر بدن، جان، اراده، زمان، کار، آبرو، خانواده، قرارداد، زمین، دستاورد و مسئولیت است.»

**صورت منطقی:**
```
Property(x, y) is primitive for y = body(x)          [A1 — خودمالکیتی اولیه]

Property(x, y) is derived iff:
  Labor(x, y) ∧ ¬Prior_Claim(y)                      [A3 — اشتقاق از کار]
  ∨ Transfer(z, y, x) ∧ Transfer_Valid(z, y, x)       [A4 — انتقال معتبر]
```

**مراتب مالکیت (از پایه به مشتق):**
```
Tier 0: Property(x, body(x))         — اولیه، غیرمشتق
Tier 1: Property(x, labor(x))        — از Tier 0 مشتق می‌شود
Tier 2: Property(x, output(labor(x))) — از Tier 1 مشتق می‌شود
Tier 3: Property(x, transferred(y))  — از Transfer معتبر مشتق می‌شود
```

**نتیجه:**
- انکار Tier 0 = انکار همه مراتب
- دولتی که Labor(x) را مصادره می‌کند = نقض Tier 1

---

## D3 — اجبار (Coercion)

**متن کتاب:**
> [ضمنی از سرتاسر کتاب — سه صورت]

**صورت منطقی:**
```
Coerce(z, x) ≡ C_physical(z, x) ∨ C_desperation(z, x) ∨ C_epistemic(z, x)

C_physical(z, x):
  z threatens or applies force → changes action-set of x

C_desperation(z, x):
  z reduces Options(x) → {only_one_option}
  ∴ consent(x) is void — "اجبار از جنس ضرورت"

C_epistemic(z, x):
  z withholds or distorts Information(x)
  ∴ consent(x) is based on false model of world — "اجبار معرفتی"
```

**قانون مشروعیت:**
```
Consent(x, action) is FR-valid iff:
  ¬Coerce(any, x) at time of consent
  Options(x) ≥ 2 at time of consent
  Information(x) ≈ complete at time of consent
```

**نتیجه:**
- رأی اکثریت تحت C_epistemic = consent void
- قرارداد تحت C_desperation = قرارداد باطل
- «رضایت داوطلبانه» بدون Options ≥ 2 = اکراه پنهان

---

## D4 — دین (Religion — تعریف FR)

**متن کتاب:**
> «دین یعنی نظام صوری منسجم اصل موضوعی برای آزادی و حقوق مالکیت فردی که بند بندش عقل و منطق و استدلال است.»
> «دین حقیقی، پیمان آزادی است.»
> «دین، اگر درست فهمیده شود، نظام تعیین حدود مالکیت است.»

**صورت منطقی:**
```
Religion_FR(R) ≡ FormalSystem(R) ∧
  Axioms(R) ⊨ Property_Rights(all individuals) ∧
  Axioms(R) ⊨ ¬Coerce(any, any) ∧
  R does not claim State_Exemption(R) from A6 ∧
  R is consistent (non-contradictory internally)
```

**معیار تشخیص دین اصیل از دین کنترلی:**
```
Religion_legitimate(R) iff:
  R enforces property rights for ALL individuals including non-believers
  R competes in open market of ideas (no monopoly claim)
  R does not require State enforcement of its rules
  ¬(R claims exclusive access to truth not verifiable by others)
```

**نتیجه:**
- «لا اکراه فی الدین» = تعریف دین از درون؛ هر دینی که اکراه بخواهد ضد خودش است
- دین دولتی = خودنقض (self-refuting)
- دین اصیل = سپر مردم در برابر دولت، نه ابزار دولت

---

## D5 — عرفان (Mysticism — تعریف FR)

**متن کتاب:**
> «عرفان در این کتاب نام هر دستگاهی است که انسان را از مالکیت، بدن، زمین، عقل، وحی و آزادی جدا کند و او را به اطاعت از یک کل مبهم بسپارد: مرشد، دولت، تاریخ، طبقه، امت، ملت، روح جهان، دیالکتیک، حزب یا ایدئولوژی.»
> «معیار تشخیص آن ساده است: هرجا مالکیت انسان، آزادی انسان، اراده آزاد انسان... تحقیر شود، با صورتی از عرفان ضدآزادی روبه‌رو هستیم.»

**صورت منطقی:**
```
Mysticism_FR(M) ≡ ∃C (Collective(C)) such that:
  M claims: Property(individual, x) → Property(C, x)
  ∨ M claims: Will(individual) → Will(C)
  ∨ M dissolves individual identity into C

Collective(C) includes:
  State, Nation, Class, Ummah, History, Dialectic,
  Party, Master (مرشد), Race, Ideology, World-Spirit
```

**شناسه عرفان در هر لباس:**
```
detect_mysticism(system S):
  if S.deprecates(material_world) → flag
  if S.dissolves(individual, collective) → flag
  if S.claims(inner_revelation > public_reasoning) → flag
  if S.requires(obedience_to_hierarchy) without property_justification → flag
  return FR_MYSTICAL_COLLAPSE
```

**نتیجه:**
- هگل، مارکس، گنوسیسم، وحدت وجود، دولت مدرن — همه instance‌های یک pattern
- عرفان = نرم‌افزار تاریخی نابودی آزادی (جمله خود نویسنده)
- فلسفه اسلامی (ابن‌عربی، ملاصدرا، سهروردی) = بازنسخه همان pattern

---

## D6 — دولت (State — تعریف FR)

**متن کتاب:**
> «دولت در این نظریه، نه صرفاً یک سازمان اداری، بلکه نهادی است که اگر مهار نشود، به بزرگترین ناقض حقوق مالکیت فردی تبدیل می‌شود.»
> «دولت ابتدا زندگی عادی انسان را جرم‌خیز می‌کند، سپس مردم را مجرم بالقوه نشان می‌دهد، و بعد برای نجات مردم از ناامنی‌ای که خود ساخته، قدرت، بودجه و اطاعت بیشتری مطالبه می‌کند.»

**صورت منطقی:**
```
State_FR(S) ≡ Organization(S) that claims:
  Monopoly on legitimate force within territory T
  Authority to define what is criminal in T
  Right to extract resources from individuals in T

State_legitimate(S) iff:
  Function(S) ⊆ {Enforce(A6), Adjudicate(disputes), Defend(territory)}
  ∧ ¬Tax(S, Labor(x)) beyond commons_maintenance_threshold
  ∧ ¬Monopolize(S, {education, health, currency, religion})
  ∧ Exit(individual, S.territory) is possible

State_illegitimate(S) iff:
  ∃ function ∈ Function(S) \ legitimate_functions
  → FR-STATE-OVERREACH
```

**مکانیزم توسعه دولت:**
```
State_expansion_cycle:
  1. Criminalize(ordinary_behavior)
  2. Generate(fear, insecurity)
  3. Present(S) as solution to fear S created
  4. Demand(more_power, more_budget, more_obedience)
  5. goto 1
```

**نتیجه:**
- تقوای سیاستمدار = اندازه دولتی که تحویل می‌دهد کمتر از آنچه تحویل گرفت
- دولت رفاه = دین جعلی که وعده بهشت زمینی می‌دهد
- مالیات بر کار = جریمه خلاقیت = نقض D2/Tier 1

---

## D7 — قرارداد (Contract)

**متن کتاب:**
> «مسئله، اخلاق‌گرایی مبهم نیست؛ قرارداد، رضایت، و عقل سلیم است.»
> «انتقال داوطلبانه و قراردادی» به‌عنوان تنها مسیر مشروع انتقال مالکیت.

**صورت منطقی:**
```
Contract(x, y, terms) is FR-Valid iff:
  (i)  Property(x, subject_of_contract)          — x چیزی را که ندارد نمی‌تواند ببخشد
  (ii) Consent(x) ∧ ¬Coerce(any, x)              — رضایت واقعی x
  (iii) Consent(y) ∧ ¬Coerce(any, y)             — رضایت واقعی y
  (iv) Information(x) ≈ Information(y)           — عدم تقارن اطلاعاتی مادی
  (v)  Options(x, post) ≥ Options_min             — x بعد از قرارداد زنده می‌ماند
  (vi) Options(y, post) ≥ Options_min             — y بعد از قرارداد زنده می‌ماند
  (vii) Exit(x, contract) possible without catastrophic_cost
  (viii) Exit(y, contract) possible without catastrophic_cost
```

**انواع قرارداد باطل:**
```
Contract_void if:
  C_desperation at time of signing → (vii) or (viii) violated
  C_epistemic at time of signing   → (iv) violated
  Subject not owned by x           → (i) violated
  State compels terms               → (ii) or (iii) violated
```

---

## D8 — سلام (Salutation — تعریف FR)

**متن کتاب:**
> «سلام، اعلام صلح مالکانه است: من به جان، مال، بدن، اراده، آبرو و مالکیت تو تعرض نمی‌کنم، و تو نیز همین پیمان را می‌پذیری.»

**صورت منطقی:**
```
Salam(x → y) ≡ Contract_declaration:
  ¬Coerce(x, y)  [x اعلام می‌کند]
  ∧ x recognizes Property(y, Domain(y))
  ∧ x expects Salam(y → x) as reciprocal

Salam_as_pact ≡ bilateral_Contract(x, y, {
  ¬Coerce(x, y),
  ¬Coerce(y, x),
  Recognize_Property(x, Domain(y)),
  Recognize_Property(y, Domain(x))
})
```

**نتیجه:**
- سلام = کوچکترین قرارداد آزادی ممکن
- نقض مالکیت بعد از سلام = نقض contract صریح
- «اسلام» = تسلیم در برابر این پیمان (نه تسلیم در برابر قدرت)

---

## D9 — قاعده تسلیط (Rule of Dominion)

**متن کتاب:**
> «قاعده تسلیط؛ صورت دینی آزادی»
> «الناس مسلطون علی اموالهم» — مردم بر اموال خود مسلطند.

**صورت منطقی:**
```
Taslit(x, y) ≡ Property(x, y) →
  x has_right_to: Use(y) ∧ Transform(y) ∧ Transfer(y) ∧ Defend(y)
  ∧ ¬any_authority can override without x's consent

Taslit_principle:
  ∀x, y: Property(x, y) → Taslit(x, y)
  State_Exception: ∄
  Religious_Exception: ∄
  Majority_Exception: ∄
```

**نتیجه:**
- «خوردن مال مردم به باطل، حتی با واسطه حاکم، مشروع نمی‌شود» = قاعده تسلیط در برابر دولت
- هر مصادره دولتی = نقض قاعده تسلیط = FR-PROPERTY-VOID

---

## D10 — دیالکتیک (Dialectic — تعریف FR)

**متن کتاب:**
> «دیالکتیک بهمثابه پرده‌ای بر یک دین پنهان»
> «رد دیالکتیک با یک آیه»
> «دیالکتیک، قربانی می‌خواهد»

**صورت منطقی:**
```
Dialectic_FR(D) ≡ Logic(D) such that:
  D allows: P ∧ ¬P → Synthesis(P, ¬P) = P'
  where P' justifies violation of A1 or A6

In FR:
  ¬(P ∧ ¬P)  [law of non-contradiction — absolute]

Therefore:
  Dialectic_FR ⊨ contradiction
  → Any policy justified by dialectical logic is FR-INVALID
  → Label: FR-DIALECTIC-TRAP
```

**نمونه‌های دیالکتیک در عمل:**
```
"مالکیت فردی (P) و برابری (¬P) → مالکیت جمعی (P')"  — کمونیسم
"آزادی (P) و امنیت (¬P) → دولت ناظر (P')"           — لیبرالیسم مدرن
"دین (P) و دولت (¬P) → دولت دینی (P')"              — ولایت مطلقه
```

**نتیجه:**
- هر استدلالی که از تضاد به ترکیب می‌رسد و توجیه تصرف مالکیت می‌کند = FR-DIALECTIC-TRAP
- منطق FR: linear, axiomatic, non-contradictory (مانند هندسه اقلیدسی)

---

## D11 — توحید (Monotheism — تعریف FR)

**متن کتاب:**
> «توحید بهمثابه اصل تضمین آزادی»
> «کسی که آتئیست است... اگر دیگران را به بندگی نگیرد، مسئله‌ای علیه آزادی ایجاد نمی‌کند.»

**صورت منطقی:**
```
Tawhid_FR ≡ ∄ authority_x such that:
  x claims absolute_sovereignty over individual(y)
  ∧ x ≠ God

Corollary_1: State(S) claiming absolute sovereignty → shirk (بت‌پرستی مدرن)
Corollary_2: Master(M) claiming sovereignty over follower → shirk
Corollary_3: Atheist who respects Property(others) → functionally compatible with FR
```

**نتیجه:**
- توحید = نفی هر ارباب غیرخدا = اصل آزادی فردی
- «کفر» در FR = کسی که دیگران را به بندگی می‌گیرد، نه کسی که خدا را باور ندارد
- دولت‌پرستی = شرک (از منظر FR)

---

## D12 — معاد (Eschatology — تعریف FR)

**متن کتاب:**
> «معاد، دزدی، و ناپایداری آزادی در جهان بی‌خدا»
> ربط به نظریه بازی‌ها: «مشکل دست آخر» (Last Round Problem)

**صورت منطقی:**
```
Last_Round_Problem:
  In finite game G with known end-time T:
    Rational_agent(x) at T: defect (steal) if P(punishment) → 0
    Backward induction: defect at T-1, T-2, ... → Nash equilibrium = steal

Maad_solution:
  Game G has no known end-time ∨ punishment persists beyond death
  → P(punishment) > 0 for all rounds including last
  → Defect is no longer dominant strategy
  → Cooperation becomes rational
```

**نتیجه:**
- بدون معاد، جامعه آزاد ناپایدار است (مشکل game-theoretic)
- معاد = ابزار حل مشکل دست آخر در نظریه بازی‌ها
- رفاه دولتی = جایگزین موقت معاد که منابع را تمام می‌کند

---

## جدول خلاصه تعاریف

| مفهوم | تعریف FR | نقیض FR |
|-------|----------|---------|
| آزادی | Property(x, Domain(x)) ∧ ¬Coerce | تعریف subjective آزادی توسط قدرت |
| مالکیت | Self-ownership + Labor-derivation + Valid-transfer | مصادره، مالیات بر کار، ملی‌سازی |
| اجبار | Physical ∨ Desperation ∨ Epistemic | «رضایت داوطلبانه» زیر فشار |
| دین | Formal system for property rights | دین دولتی، دین اجباری |
| عرفان | هر سیستمی که فرد را در جمع حل کند | — |
| دولت | سازمان انحصار قوه قاهره | دولت محدود مشروع |
| قرارداد | 8 شرط، exit ممکن | قرارداد اضطراری، اطلاعات نامتقارن |
| سلام | کوچکترین قرارداد آزادی | تعارف بدون commitment |
| تسلیط | حق کامل بر مال خود | استثنا برای دولت یا دین |
| دیالکتیک | P ∧ ¬P → P' برای توجیه تصرف | منطق خطی، آکسیوماتیک |
| توحید | نفی هر ارباب غیرخدا | شرک = دولت‌پرستی |
>>>>>>> 3823bf7c7c7c2f1dcbf80ccde03171d00ceb28ad
| معاد | حل مشکل دست آخر در game theory | جهان بدون پاسخ‌گویی |