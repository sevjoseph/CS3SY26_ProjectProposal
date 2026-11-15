# CS3SY26_ProjectProposal

### Project Title or Name of the Application : Buy or Bye
### Section			   	      : 9 - Rubidium
### Group Members			    : FAJARDO, Jonathan; QUIATCHON, Mirawen Carissa; SEVILLA, Joseph Gene
### Date (Proposal Date)  : Nov 13, 2026

### Project Description:

#### **Summary**
Buy or Bye is a financial planning application that helps users track their income, expenses, budgets, and saving goals. It also features an evaluator that checks planned purchases based on the user’s balance and priorities (e.g., classifying as a need or a want). It is needed to help individuals manage limited finances and avoid unnecessary spending. It also encourages users to make more responsible purchases.

#### **Features**
Buy or Bye features user management; it handles basic user information. This includes user registration and login, profile management, and access to financial information/dashboard. It also features income and expense tracking, which allows users to record and organize categorize their income and expenses. The app also includes budget management, allowing users to set spending limits for different categories and monitor their remaining budget. The app also allows users to manage savings goals by recording additional savings and monitoring their progress. In addition to this, the app also has a smart purchase evaluator, which lets users enter planned purchases. It evaluates them based on the current balance, category, and savings goals, then provides recommendations such as “Reasonable to Buy”, “Wait and Save”, “Not Affordable Right Now.” Lastly, the app features financial reports, displaying summaries of the user’s income, expenses, current balance, budget status, savings progress, and any planned purchases

#### **Expected Output**
Buy or Bye will feature a dashboard displaying the user’s information, balance, income, expenses, and savings progress, with a navigation menu containing tabs for Dashboard, Transactions, Budgets, Savings Goals, Planned Purchases, and Financial Reports. Each tab will have its own interface for managing financial records, setting goals and budgets, evaluating planned purchases, and viewing summaries.

#### **Class, Attributes, and Methods**
- The User class manages the user’s account and personal information. Its attributes include userID, name, email, balance, and password, while its methods include registerAccount(), login(), updateProfile(), viewDashboard(), and calculateBalance().
- The Transaction class stores information about changes in balance through attributes such as transactionID, amount, date, category, and description. Its methods include addTransaction(), editTransaction(), and deleteTransaction().
- The Income class handles money received by the user. It has an additional attribute incomeSource and methods recordIncome() and calculateTotalIncome(). The Expense class handles spending. All its attributes are inherited from Transaction, and its methods include recordExpense() and calculateTotalExpense().
- The Category class organizes income, expenses, and purchases into groups such as food, transportation, education, and entertainment. It contains  categoryID, categoryName, and description for attributes, and addCategory(), deleteCategory(), editCategory(), and viewCategory() for methods.
- The Budget class manages the spending limits for different categories. It has attributes such as budgetID, spendingLimit, amountSpent, and category. Its methods include setBudget(), removeBudget(), calculateRemainingBudget(), and checkBudgetLimit().
- The SavingsGoal class manages the user’s financial targets and monitors their progress. Its attributes are goalID, goalName, targetAmount, currentAmount, and targetDate. Its methods are createGoal(), removeGoal(), addSavings(), and calculateProgress().
- The PurchaseItem class stores information about items the user plans to buy. Its attributes are itemID, itemName, price, category, and priority (whether a need/want). Its methods include addItem(), editItem(), removeItem(), and viewItemDetails().
- The PurchaseEvaluator class checks planned purchases using the current balance, remaining budget, and savings goals. Its attributes are evaluationDate, and its methods are evaluatePurchase(), checkAffordability(), checkBudgetLimit(), checkSavingsImpact(), and giveRecommendation(). The methods that start with check give back either True or False, then the evaluator gives a recommendation based on these. checkAffordability() checks whether the price of the item is less than the balance, checkBudgetLimit() checks whether it exceeds the category budget, and checkSavingsImpact() evaluates its effect on the user's savings goals.
- The FinancialReport class summarizes the user’s financial information. It contains reportID, startDate and endDate for attributes and generateReport() for methods. generateReport() gathers information from the user's income, expenses, balance, savings goals, and planned purchases.

The User class has a composition relationship with Transaction, Budget, SavingsGoal, and Purchase Item because these belong to a specific user and cannot exist without that user. The Income and Expense classes both inherit from Transaction, sharing its attributes and methods. The Category class has association relationships with Transaction, PurchaseItem, and Budget to organize them into different categories. The PurchaseEvaluator class has dependency relationships with User, PurchaseItem, Budget, and SavingsGoal since it checks planned purchases based on the user’s financial information (balance, budget, and savings goals). FinancialReport has dependency relationships with User, Income, Expense, PurchaseItem, Budget, and SavingsGoal since it uses these to gather financial information and generate a report.

#### **Target Users**
The target users of the application are students, young adults, and working individuals, especially those who want to improve their financial management skills. It is designed for students who need to budget their allowances for necessities, as well as those who want to monitor their income and expenses. The app is also suitable for those who struggle with impulsive spending.

#### **Class Diagram**
<img width="854" height="567" alt="image" src="https://github.com/user-attachments/assets/7439e37e-7de4-4f29-a5a1-5b9b4cea8ada" />

### Goals:
The long-term outcomes of our project include better financial planning through classification of possible purchases as either wants or needs, efficient tracking of savings made, and identification of the attainability of financial goals set.

- Objective 1: Track transactions through user input by allowing users to record, categorize, edit, and delete these transactions.
- Objective 2: Assist users' decision-making by identifying purchases as needs or wants and evaluating them based on their affordability.
- Objective 3: Evaluate how users' purchases influence the attainability of their set financial goals by evaluating their impact on progress and providing recommendations.
