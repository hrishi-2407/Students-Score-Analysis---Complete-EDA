# Students-Score-Analysis---Complete-EDA

## 📊📚 Project Title:
Exploratory Data Analysis (EDA) and Correlation Study on Student Performance Data

## 📌 Objective:
To perform a comprehensive exploratory data analysis (EDA) on student performance data, identify patterns, visualize relationships between categorical and numerical variables, handle missing data effectively, encode categorical variables for numerical analysis, and analyze correlations among variables including subject scores.

## 📑 Dataset Overview:
- The dataset contains information about students' demographic details, family background, and performance in three academic subjects:
- MathScore, ReadingScore, WritingScore
- As well as categorical attributes like:
- Gender, EthnicGroup, ParentEduc, ParentMaritalStatus, LunchType, WklyStudyHours, PracticeSport, TestPrep, NrSiblings, IsFirstChild, TransportMeans

## 📈 Project Workflow:
### 🔍 1️⃣ Data Inspection
- Load dataset into a DataFrame
- View dataset shape and structure using df.head(), df.info()
- Check for duplicates
- Check missing values per column
- Get unique values for each column to understand categorical distributions

### 🧹 2️⃣ Data Cleaning & Imputation
- Handle missing values:
- For categorical variables → imputed using mode (reason: mode preserves category distribution better than mean/median for non-numeric data)
- For numeric variables (if any missing) → imputed with mean or median
- Removed unwanted columns (e.g., MathScore, ReadingScore, WritingScore for certain steps as requested)

### 📊 3️⃣ Univariate Analysis
- Visualize distributions for individual categorical features:
- Bar plots for Gender, EthnicGroup, ParentEduc, WklyStudyHours, PracticeSport, TestPrep, TransportMeans
- Box plots for subject scores
- Pie chart of Ethnic Groups distribution
- Bar plots of category-wise counts

### 📉 4️⃣ Bivariate Analysis
- Boxplots of each subject score against categorical variables:
- Gender, EthnicGroup, ParentMaritalStatus
- Understand how different groups perform in each subject.

### 🎻 5️⃣ Multivariate Analysis
- Violin plots to analyze subject score distributions across combinations:
- Gender vs ParentEduc
- Gender vs EthnicGroup
- Gender vs TestPrep
- Gender vs WklyStudyHours

### 📊 6️⃣ Aggregated Score Analysis
- Create a new feature: OverallScore = mean of Math, Reading, and Writing scores
- Bin OverallScore into intervals of 10 marks using pd.cut() for better visualization.

### 📝 7️⃣ Grade Categorization
- Map OverallScore bins into Grades (like A, B, C, D)
- Pie chart showing the percentage distribution of grades

### 📈 8️⃣ Comparative Aggregate Analysis
- Bar plots for average OverallScore against: ParentEduc, WklyStudyHours, NrSiblings, IsFirstChild, EthnicGroup, PracticeSport
- Box plot for OverallScore by ParentEduc

### 📊 9️⃣ Correlation Analysis
- Encode all categorical features:
- Label Encoding for binary categories (Gender, PracticeSport, TestPrep, IsFirstChild)
- Ordinal Encoding for WklyStudyHours
- One-Hot Encoding for multi-class categories (EthnicGroup, ParentEduc, ParentMaritalStatus, NrSiblings, LunchType, TransportMeans)
- Compute correlation matrix for encoded data
- Heatmap for entire correlation matrix
- Separate heatmaps for correlations of:
- MathScore with other features
- ReadingScore with other features
- WritingScore with other features

## 📋 Final Deliverables:
- Cleaned, processed, and well-documented notebook with:
- Clear EDA plots
- Statistical summaries
- Correlation matrices
- Insightful comments/annotations

