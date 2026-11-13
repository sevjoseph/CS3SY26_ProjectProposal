# CS3SY26_ProjectProposal

### Project Title or Name of the Application : Buy or Bye
### Section			   	      : 9 - Rubidium
### Group Members			    : FAJARDO, Jonathan; QUIATCHON, Mirawen Carissa; SEVILLA, Joseph Gene
### Date (Proposal Date)  : Nov 13, 2026

### Project Description:

#### **Summary**
Buy or Bye is a financial planning application that helps users track their income, expenses, budgets, and saving goals. It also features an evaluator that checks planned purchases based on the user’s balance and priorities (e.g., classifying as a need or a want). It is needed to help individuals manage limited finances and avoid unnecessary spending. It also encourages users to make more responsible purchases.

#### **Features**
Buy or Bye features user management; it handles basic user information. This includes user registration and login, profile management, and access to financial information/dashboard. It also features income and expense tracking, which allows users to record and organize categorize their income and expenses. The app also includes budget management, allowing users to set spending limits for different categories and monitor their remaining budget. In addition to this, the app also has a smart purchase evaluator, which lets users enter planned purchases. It evaluates them based on the current balance, category, and savings goals, then provides recommendations such as “Reasonable to Buy”, “Wait and Save”, “Not Affordable Right Now.” Lastly, the app features financial reports, displaying summaries of the user’s income, expenses, current balance, budget status, savings progress, and any planned purchases

#### **Class, Attributes, and Methods**
- The User class manages the user’s account and personal information. Its attributes include userID, name, email, and password, while its methods include registerAccount(), login(), updateProfile(), and viewDashboard().
- The Transaction class is the parent class of Income and Expense. It stores information through attributes such as transactionID, amount, date, category, and description. Its methods include addTransaction(), editTransaction(), and deleteTransaction().
- The Income class inherits from Transaction and handles money received by the user. It has an additional attribute incomeSource and methods recordIncome() and calculateTotalIncome(). The Expense class also inherits from Transaction and handles spending. Its attributes include expenseType and merchant, and its methods include recordExpense() and calculateTotalExpense().
- The Expense class also inherits from Transaction and handles spending. Its attributes include expenseType and merchant, and its methods include recordExpense() and calculateTotalExpense().
- The Category class organizes income, expenses, and purchases into groups such as food, transportation, education, and entertainment. It contains  categoryID, categoryName, and description for attributes, and addCategory(), updateCategory(), and viewCategory() for methods.
- The Budget class manages the spending limits for different categories. It has attributes such as budgetID, spendingLimit, amountSpent, and category. Its methods include setBudget(), calculateRemainingBudget(), and checkBudgetLimit().
- The SavingsGoal class manages the user’s financial targets and monitors their progress. Its attributes are goalID, goalName, targetAmount, currentAmount, and targetDate. Its methods are createGoal(), addSavings(), calculateProgress(), and checkGoalStatus().
- The PurchaseItem class stores information about items the user plans to buy. Its attributes are itemID, itemName, price, category, and priority (whether a need/want). Its methods include addItem(), editItem(), removeItem(), and viewItemDetails().
- The PurchaseEvaluator class checks planned purchases using the current balance, remaining budget, and savings goals. Its attributes are evaluationDate, and its methods are evaluatePurchase(), checkAffordability(), checkBudgetLimit(), checkSavingsImpact(), and giveRecommendation().

The FinancialReport class summarizes the user’s financial information. It contains reportID, startDate and endDate for attributes and calculateIncome(), calculateExpenses(), calculateBalance(), and generateReport() for methods.


**Target Users**
The target users of the application are students, young adults, and working individuals, especially those who want to improve their financial management skills. It is designed for students who need to budget their allowances for necessities, as well as those who want to monitor their income and expenses. The app is also suitable for those who struggle with impulsive spending.

**Class Diagram**
- The description is then followed by the class diagram, depicting clearly what was described.

**Sample class Diagram from https://static.visual-paradigm.com/web/images/tutorials/class-diagram-tutorial/01-class-diagram-example.png:**

![Sample Diagram](https://static.visual-paradigm.com/web/images/tutorials/class-diagram-tutorial/01-class-diagram-example.png)

### Goals:

The long-term outcomes of our project include better financial planning through classification of possible purchases as either wants or needs, efficient tracking of savings made, and identification of the attainability of financial goals set.

- Objective 1: Track expenses through user input 
- Objective 2: Assist user's decision-making by identifying purchases as needs or wants
- Objective 3: Influence the attainability of set financial goals through their relation with user's purchase/s
