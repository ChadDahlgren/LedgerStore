
# LedgerStore

**LedgerStore** is a flexible, Python-based financial data library designed for securely and consistently storing income and expense records. Built with simplicity and extensibility in mind, LedgerStore offers a foundation for managing financial data in applications ranging from personal budgeting to complex financial systems.

## 🚀 Key Features

- **Secure and Immutable**: Append-only data design ensures auditability and maintains an accurate history of financial records.
- **Document Store Design**: Combines the flexibility of a document store with the reliability of Postgres.
- **Income and Expense Tracking**: Focused on solving the core problems of storing and retrieving financial ledger data.
- **Extensible by Design**: Provides a foundation for categorization, budgeting, and other financial concepts in future versions.
- **Open and Reusable**: Publicly available with an Apache 2.0 license for community collaboration and innovation.

---

## 🛠️ Installation

To use LedgerStore in your project, clone the repository and install dependencies:

\`\`\`bash
git clone https://github.com/yourusername/ledgerstore.git
cd ledgerstore
pip install -r requirements.txt
\`\`\`

---

## 📚 Usage

### Initialize the LedgerStore

\`\`\`python
from ledgerstore import LedgerStore

# Connect to Postgres
ledger = LedgerStore(db_url="postgresql://user:password@localhost:5432/ledgerdb")
\`\`\`

### Add Income

\`\`\`python
income = {
    "type": "W2",
    "gross": 5000.00,
    "net": 4000.00,
    "date": "2024-12-01"
}
ledger.add_income(income)
\`\`\`

### Add Expense

\`\`\`python
expense = {
    "category": "Groceries",
    "amount": 200.00,
    "date": "2024-12-02"
}
ledger.add_expense(expense)
\`\`\`

### Retrieve Data

\`\`\`python
# Retrieve all income
income_records = ledger.get_income()

# Retrieve expenses by category
expenses = ledger.get_expenses(filters={"category": "Groceries"})
\`\`\`

---

## 🌟 Why LedgerStore?

LedgerStore is **not an ORM**—it's a focused library for storing financial ledger data with an eye toward simplicity and consistency. It’s designed to:
- Provide a reliable data layer for financial applications.
- Lay the groundwork for extensibility into advanced features like budgeting and categorization.
- Stay agnostic to how data is generated or consumed.

---

## 🔮 Future Plans

- Add support for categorization and budget tracking.
- Explore integration with local-first storage (e.g., SQLite) for mobile applications.
- Build an immutable audit log for SOX compliance-like use cases.
- Expand extensibility for domain-specific applications (e.g., gig work, law firm billables).

---

## 🛡️ License

LedgerStore is licensed under the **Apache License 2.0**. See [LICENSE](LICENSE) for details.

---

## 🤝 Contributing

Contributions are welcome! Please open an issue to discuss potential features or bug fixes.

---

## 📬 Contact

If you have questions or ideas, feel free to open an issue or contact me at [your email/contact link].
