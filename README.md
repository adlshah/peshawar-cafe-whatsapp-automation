 ☕ Peshawar Café WhatsApp Automation

Automated WhatsApp ordering and FAQ system for Peshawar Café, built using n8n, WhatsApp Cloud API, and Google Sheets.  
This project helps automate customer interactions — including order taking, café information, and stock checking — without writing any code.


 Project Overview

This system allows customers to:
- 🛒 Place café orders directly through WhatsApp  
- ℹ️ Ask FAQs or get café information instantly  
- 📦 Check current menu and item availability  

The workflow is powered by n8n, connected to **Google Sheets** for live data management:
- `Orders Sheet` – stores confirmed customer orders  
- `FAQ Sheet` – stores all common questions and answers  
- `Food Items Sheet` – maintains menu and stock status  

💬 How It Works

 🔹 Step 1: Greeting Message

When someone sends “Hi” or “Hey”, they receive:

> Welcome to Peshawar Café ☕ 
> How can I help you today?  
> - 🛒 Place an order  
> - ℹ FAQ / Information  
> - 📦 Check order / stock  



🔹 Step 2: Placing an Order

If the customer chooses “Place an order”, the bot guides them step by step:

1. Ask for name → “Please tell me your name.”  
2. Ask for food item → “What would you like to order?”  
3. Ask for quantity → “How many would you like?”  
4. Check stock from the **Food Items Sheet**  
5. Confirm the order and record it in the **Orders Sheet**

If the item is out of stock, the bot responds:
> “Sorry, that item is currently out of stock. Please choose another item.”

Customer: Hi
Bot: Welcome to Peshawar Café ☕
How can I help you today?

🛒 Place an order

ℹ FAQ / Information

📦 Check order / stock

Example conversation:

Customer: Place an order
Bot: Please tell me your name.
Customer: Ali
Bot: Hi Ali 👋 What would you like to order?
Customer: Cappuccino
Bot: How many would you like?
Customer: 2
Bot: Your order for 2 Cappuccinos has been confirmed ✅
Thank you, Ali!



🔹 Step 3: FAQ / Information

If the customer selects “FAQ / Information”**, the bot fetches responses directly from the FAQ Sheet, such as:

| Question | Answer |
|-----------|---------|
| What are your opening hours? | We are open daily from **11:00 AM to 10:00 PM**. |
| Do you offer home delivery? | Yes, we deliver within **5 km across Peshawar** via FoodPanda and WhatsApp orders. |
| What is your refund policy? | Refunds are available only for canceled orders before preparation starts. |
| Where are you located? | University Town, Peshawar, right near KFC. |
| How can I place an order? | You can order via phone, WhatsApp, or our website.|
| Do you accept online payments? | Yes, we accept Easypaisa, JazzCash, and Cash on Delivery. |

🔹 Step 4: Check Order / Stock

If the customer chooses “📦 Check order / stock”, the bot sends the latest menu with item availability:

| Food Item        | Quantity | Status        |
|------------------|-----------|---------------|
| Green Tea        | 10        | Available     |
| Cappuccino       | 15        | Available     |
| Iced Coffee      | 12        | Available     |
| Fresh Juice      | 8         | Available     |
| Milk Shake       | 20        | Available     |
| Cold Mocha       | 0         | Out of Stock  |
| Chocolate Cake   | 20        | Available     |
| Donut            | 7         | Out of Stock  |



 ⚙️ Tools & Integrations

| Tool | Purpose |
|------|----------|
| n8n | Workflow automation engine |
| WhatsApp Cloud API | Message automation |
| Google Sheets | Menu, FAQ, and Orders data |
| Function Node (JS) | Handles logic for name, item, and quantity |
| Webhook Node | Connects n8n to WhatsApp API |

Demo Video :https://youtu.be/kGY-_AHOEVQ
