# 🎬 Netflix Data Analysis & Dashboard Project  

### 📊 **Overview**
This project analyzes Netflix’s catalog of movies and TV shows using **Python (EDA)** and **Excel (Dashboard)**.  
It provides insights into content trends across **countries, genres, ratings, and release years**, helping understand Netflix’s content strategy and audience focus.

---

## 🧾 **Project Files**
| File | Description |
|------|--------------|
| `Netflix_Project.ipynb` | Python notebook for data cleaning, transformation, and exploratory data analysis (EDA). |
| `Netflix DashBoard Main.xlsx` | Excel dashboard with visualizations and interactive slicers (Country, Genre, Rating, Year, Type). |

---

## 🎯 **Objectives**
- Analyze Netflix’s content library (Movies and TV Shows).  
- Identify trends by **country, genre, and rating**.  
- Visualize year-wise content growth.  
- Build an interactive dashboard to explore insights.  

---

## 🧰 **Tools & Technologies**
| Tool | Purpose |
|------|----------|
| **Python (Pandas, Seaborn, Matplotlib)** | Data cleaning and visualization |
| **Excel / Power Query** | Data transformation and dashboard creation |
| **Power BI (optional)** | Interactive data exploration |
| **Jupyter Notebook** | EDA and reporting environment |

---

## 🧹 **Data Cleaning Steps**
Performed using Power Query & Python:
1. Removed duplicate records using `show_id`.  
2. Filled missing values (`country`, `rating`, `director`) with `"Unknown"`.  
3. Extracted `year_added` and `month_added` from `date_added`.  
4. Split `duration` into **minutes** (Movies) and **seasons** (TV Shows).  
5. Grouped by `Country` → Kept **Top 50 Countries**.  
6. Grouped by `listed_in` (Genre) → Kept **Top Genres**.  
7. Filtered only **recent years (>=2015)**.  

---

## 📊 **Dashboard Visualizations (Excel)**
| Chart Title | Visualization Type | Description |
|--------------|---------------------|--------------|
| Movies vs TV Shows | Pie Chart | Shows distribution between content types |
| Top 10 Countries by Titles | Bar Chart | Displays which countries produce the most content |
| Ratings Distribution | Column Chart | Shows Netflix’s audience focus (Kids/Teen/Adult) |
| Genre Distribution | Bar Chart | Displays top genres |
| Titles Released Over Years | Line Chart | Visualizes content growth trend |
| Audience Category | Pie Chart | Divides content by Kids, Teen, and Adult categories |

🎛 **Slicers Used:**
- Country  
- Genre (listed_in)  
- Release Year  
- Rating  
- Type (Movie / TV Show)

---

## 🔍 **Key Insights**
- **Movies** make up about 70% of Netflix’s library; **TV Shows** ~30%.  
- **TV-MA** and **TV-14** dominate the ratings — focusing on **teen/adult audiences**.  
- **USA, India, and UK** lead in content production.  
- **Drama, Comedy, and Action** are the top-performing genres.  
- Content addition peaked between **2018–2020**.  

---

## 💡 **Recommendations**
✅ Expand content in **Kids and Family** categories.  
✅ Increase investments in **Asian & European** content (India, Korea, Spain).  
✅ Focus more on **Docuseries and Animated** genres.  
✅ Maintain balance between Movies and TV Shows.  

---

## 🧠 **Sample Python Visuals**
```python
# Movies vs TV Shows
sns.countplot(x='type', data=df, palette='pastel')
plt.title('Movies vs TV Shows on Netflix')
plt.show()

# Top 10 Countries
top_countries = df['country'].value_counts().head(10)
sns.barplot(x=top_countries.values, y=top_countries.index)
plt.title('Top 10 Countries on Netflix')
plt.show()
