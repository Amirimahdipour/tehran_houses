import pandas as pd

# بارگذاری داده‌ها
df = pd.read_csv("tehran_houses.csv")

print("\n🏠 سامانه محاسبه میانگین قیمت مسکن (داده‌های آگهی)\n")

# ورودی کاربر
neighborhood = input("نام محله: ").strip()
area = int(input("متراژ (متر مربع): "))
rooms = int(input("تعداد اتاق: "))
age = int(input("سن بنا: "))
parking = int(input("پارکینگ دارد؟ (1=بله، 0=خیر): "))

# فیلتر شرطی
filtered = df[
    (df["neighborhood"] == neighborhood) &
    (df["rooms"] == rooms) &
    (df["parking"] == parking) &
    (df["area"].between(area - 10, area + 10)) &
    (df["age"].between(age - 5, age + 5))
]

print("\n🔍 تعداد آگهی‌های مشابه:", len(filtered))

if filtered.empty:
    print("❌ مورد مشابهی یافت نشد.")
else:
    print("💰 میانگین قیمت:", f"{int(filtered['price'].mean()):,}", "تومان")
    print("📉 کمترین قیمت:", f"{int(filtered['price'].min()):,}", "تومان")
    print("📈 بیشترین قیمت:", f"{int(filtered['price'].max()):,}", "تومان")
