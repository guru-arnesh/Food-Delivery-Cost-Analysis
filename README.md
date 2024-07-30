**||Analyzing the Economics of Food Delivery Services||**

First things first👇

•Code Optimization Highlight:

1) Why this?👇


def extract(value):

 a = str(value).split(" ")

 return a[0]

df["Discounts and Offers"] = df["Discounts and Offers"].apply(extract)

If it can be!👇


df["Discounts and Offers"] = df["Discounts and Offers"].str.split(" ").str[0]






2) Why this?👇


def removep(value):

 if "%" in value:

 a = value.replace("%","")

 return float(a)

 else:

 return float(value)

df["Discounts and Offers"] = df["Discounts and Offers"].apply(removep)

If it can be!👇


df['Discounts and Offers'] = df['Discounts and Offers'].str.replace('%', '')

📂 𝗣𝗿𝗼𝗷𝗲𝗰𝘁 𝗢𝘃𝗲𝗿𝘃𝗶𝗲𝘄:


The dataset comprised 1,000 orders, including detailed information on:

•Order ID and Customer ID

•Restaurant ID

•Order Date and Time

•Delivery Date and Time

•Order Value and Delivery Fee

•Payment Method

•Discounts and Offers

•Commission Fees

🛠️ 𝗞𝗲𝘆 𝗦𝘁𝗲𝗽𝘀 𝗮𝗻𝗱 𝗧𝗲𝗰𝗵𝗻𝗶𝗾𝘂𝗲𝘀:

𝟭) 𝗗𝗮𝘁𝗮 𝗖𝗹𝗲𝗮𝗻𝗶𝗻𝗴 𝗮𝗻𝗱 𝗣𝗿𝗲𝗽𝗮𝗿𝗮𝘁𝗶𝗼𝗻:

•Converted date columns to datetime format for accurate calculations.

•Extracted and cleaned discount data by removing percentage symbols. •Handling missing values.

𝟮) 𝗖𝗮𝗹𝗰𝘂𝗹𝗮𝘁𝗶𝗼𝗻𝘀:

•Discount Amount: Calculated as (Discount Percentage / 100) * Order Value.

•Total Cost: Summed delivery fees, discount amounts, and payment processing fees.

•Profit: Computed as the difference between commission fees and total cost.

𝟯) 𝗩𝗶𝘀𝘂𝗮𝗹𝗶𝘇𝗮𝘁𝗶𝗼𝗻:

•Pie Chart: Displayed the distribution of costs (delivery fees, payment processing fees, discount amounts).

•Bar Chart: Illustrated the comparison of commission fees, total cost, and profit.

•Histogram: Showed the distribution of profits across orders.

🧰 𝗧𝗼𝗼𝗹𝘀 𝗨𝘀𝗲𝗱:

•Pandas: For data manipulation and cleaning.

•Matplotlib: For creating insightful visualizations.
