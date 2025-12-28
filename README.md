# Retail Workflow & Point of Sale (POS) System

A hybrid monolithic application designed to streamline retail operations. This system integrates point-of-sale transaction processing with a custom workflow engine to track order states from initiation to fulfillment.

Built using **Laravel (PHP)** for robust backend logic and **Vue.js** for a reactive, seamless user interface.

## 🏗 System Architecture

### Core Stack
* **Backend:** Laravel 10 (PHP)
* **Frontend:** Vue.js (Integrated via Vite)
* **Database:** MySQL
* **State Management:** Pinia / Vuex (implied)
* **Architecture:** MVC with Service-Repository Pattern

### Key Modules

#### 🛍 Point of Sale Interface
* **Real-time Transaction Processing:** capable of handling high-volume order inputs.
* **Dynamic Cart Management:** Client-side state handling for immediate UI feedback.
* **Inventory Synchronization:** Automated stock deduction upon transaction completion.

#### 🔄 Workflow Management Engine
* **Custom State Machine:** Tracks orders through defined lifecycles (e.g., *Pending -> Processing -> Quality Check -> Dispatched*).
* **Role-Based Access Control (RBAC):** Differentiates permissions between Cashiers, Store Managers, and Admins.
* **Audit Logging:** Tracks all state changes for security and accountability.

## 📂 Repository Structure

```bash
├── app             # Core Laravel Application Logic (Models, Controllers)
├── database        # Migrations and Seeders
├── pos-frontend    # Vue.js Source Code
│   ├── components  # Reusable UI Elements
│   └── views       # Page-level Logic
├── routes          # API and Web Routes
└── tests           # PHPUnit Feature and Unit Tests
```
##🚀 Installation & Setup
Prerequisites
PHP 8.1+
Composer
Node.js & NPM

## Setup Instructions
Clone the Repository

```Bash

git clone [https://github.com/vadhh/laravel-vue-pos-system.git](https://github.com/vadhh/laravel-vue-pos-system.git)
cd laravel-vue-pos-system
Install Backend Dependencies
```
```Bash

composer install
Install Frontend Dependencies
```
```Bash

npm install
Environment Configuration
```
```Bash

cp .env.example .env
php artisan key:generate
Configure your database credentials in the .env file.
```
## Database Migration

```Bash

php artisan migrate --seed
Run Application Terminal 1 (Backend):
```
```Bash

php artisan serve
Terminal 2 (Frontend compilation):
```
```Bash

npm run dev
```
###🛠 Future Improvements
API Decoupling: Migrating to a fully headless architecture (Laravel API + Standalone Vue SPA).

Offline Mode: Implementing Service Workers for transaction queuing during network outages.

Reporting Module: Integration with Chart.js for sales analytics.

© 2025 Vadhh. MIT License.
