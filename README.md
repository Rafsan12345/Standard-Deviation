import pandas as pd

# ডেটাসেট
data = [38, 44, 48, 50, 55, 44, 74]

# DataFrame তৈরি
df = pd.DataFrame(data, columns=["Results"])

# গড় (Mean)
mean_value = df["Results"].mean()

# নমুনা Standard Deviation (Sample STD)
sample_std_dev = df["Results"].std()

# পূর্ণ সেটের Standard Deviation (Population STD)
population_std_dev = df["Results"].std(ddof=0)

# নমুনা Variance (Sample Variance)
sample_variance = df["Results"].var()

# পূর্ণ সেটের Variance (Population Variance)
population_variance = df["Results"].var(ddof=0)

# সর্বনিম্ন মান (Minimum)
minimum_value = df["Results"].min()

# সর্বোচ্চ মান (Maximum)
maximum_value = df["Results"].max()

# যোগফল (Sum)
total_sum = df["Results"].sum()

# Percentiles (25%, 50%, 75%)
percentiles = df["Results"].quantile([0.25, 0.50, 0.75])

# ফলাফল প্রিন্ট করা
print(f"Mean (গড়): {mean_value:.2f}")
print(f"Sample Standard Deviation (প্রমিত বিচ্যুতি - নমুনা): {sample_std_dev:.2f}")
print(f"Population Standard Deviation (প্রমিত বিচ্যুতি - জনসংখ্যা): {population_std_dev:.2f}")
print(f"Sample Variance (বিচ্যুতি - নমুনা): {sample_variance:.2f}")
print(f"Population Variance (বিচ্যুতি - জনসংখ্যা): {population_variance:.2f}")
print(f"Minimum Value (সর্বনিম্ন মান): {minimum_value}")
print(f"Maximum Value (সর্বোচ্চ মান): {maximum_value}")
print(f"Total Sum (মোট যোগফল): {total_sum}")
print("Percentiles (পারসেন্টাইল):")
print(percentiles)

cv = (sample_std_dev / mean_value) * 100
print(f"Coefficient of Variation: {cv:.2f}%")



