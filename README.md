### README: Bank Control System Design

#### Overview:
This project demonstrates the implementation of various **design patterns** in a bank control system. The system incorporates patterns like Singleton, Factory, Observer, Decorator, Strategy, Command, Adapter, and Proxy, providing an extensible and scalable banking system architecture.

#### Key Features:
1. **Singleton Pattern**: 
   - Ensures that only one instance of `BankControlSystem` exists throughout the application.

2. **Factory Pattern**:
   - Provides a way to create specific types of bank accounts (Savings and Checking) dynamically using the `BankAccountFactory`.

3. **Observer Pattern**:
   - Allows the `TransactionSystem` to notify its observers (`UserObserver`) when any transaction is recorded.

4. **Decorator Pattern**:
   - Dynamically adds functionality like `OverdraftProtection` to bank accounts, enhancing their behavior at runtime.

5. **Strategy Pattern**:
   - Enables the application of different interest calculation methods (Simple or Compound interest) for accounts using the `InterestStrategy` interface.

6. **Command Pattern**:
   - Encapsulates transactions (like deposits and withdrawals) as command objects that can be queued and executed by an `Invoker`.

7. **Adapter Pattern**:
   - Facilitates integration with a third-party payment system using the `PaymentAdapter`.

8. **Proxy Pattern**:
   - Controls access to accounts by users with different permission levels (Admin or Regular User) using the `AccountProxy`.

#### Classes and Design Patterns Breakdown:

- **BankControlSystem**: 
  - Implements the Singleton pattern to manage all accounts in the bank.
  
- **BankAccount and its subclasses** (`SavingsAccount`, `CheckingAccount`): 
  - Abstract base class and concrete implementations for different types of bank accounts.

- **BankAccountFactory**:
  - Implements the Factory pattern to create and return specific bank accounts.

- **Subject and Observer**:
  - Implements the Observer pattern to notify users when a transaction is recorded.

- **AccountDecorator and OverdraftProtection**:
  - Implements the Decorator pattern to add overdraft protection to accounts dynamically.

- **InterestStrategy, SimpleInterestStrategy, CompoundInterestStrategy**:
  - Implements the Strategy pattern to allow dynamic selection of different interest calculation methods.

- **Command, DepositCommand, WithdrawCommand, Invoker**:
  - Implements the Command pattern to encapsulate transactions as commands and execute them.

- **ThirdPartyPaymentSystem, PaymentAdapter**:
  - Implements the Adapter pattern to allow third-party payment system integration.

- **User and AccountProxy**:
  - Implements the Proxy pattern to control user access to accounts based on their roles.

#### How to Use:

1. **Create Accounts**:
   - Choose between Savings or Checking accounts.
   
2. **Add Overdraft Protection**:
   - Enable overdraft protection for checking accounts with a specified limit.

3. **Apply Interest to Savings Accounts**:
   - Apply either simple or compound interest to savings accounts.

4. **Perform Transactions**:
   - Perform deposits and withdrawals using the Command pattern for transaction encapsulation.

5. **Use Third-Party Payment System**:
   - Make payments via the third-party payment system using the Adapter pattern.

6. **Set Up Proxy Users**:
   - Create users with different roles and control their access to the bank accounts.

7. **Exit the Program**:
   - Terminate the session.

#### Running the Program:
- Simply run the main script in any Python environment.
- Follow the menu-driven interface to interact with the system.

#### Future Enhancements:
- **Persistence**: Add a database for storing account details persistently.
- **User Interface**: Create a GUI for enhanced user experience.
- **Security**: Implement additional security measures such as authentication and encryption for transactions.

#### Dependencies:
- Python 3.x

#### Note
This project is for practicing python only. No framework or database is used in this project.
