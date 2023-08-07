# UMLpractice

# Task 1: Creating a Comprehensive Class Diagram
**Objective:** Create an in-depth Class Diagram for an Online Shopping System. 
The PlantUML diagram outlines an online shopping system. Customers can register, log in, update profiles, and place orders. They manage items in a cart, which connects to products. Each order includes items from the cart, and payments are processed via a PaymentGateway interface. This setup enables seamless shopping interactions

**Classes:**

- **Customer:** Represents a customer with attributes like id, name, email, password, and address. It has methods for registering, logging in, updating the profile, and placing orders.

- **Product:** Represents a product with attributes like pid, name, description, and price. It has a method to retrieve product details.

- **Order:** Represents an order with attributes like id, product id (pid), date, status, and items. It has methods for adding/removing products to/from the order and updating the order status.

- **Cart_Item:** Represents an item in the cart with attributes like id, product id (pid), and quantity. It has a method to update the quantity.

- **Cart:** Represents a customer's shopping cart with attributes like id and items. It has methods for adding/removing items, clearing the cart, and placing an order.

- **Payment:** Represents a payment with attributes like id, amount, and paymentMethod. It has a method to process the payment.

- **PaymentGateway:** An interface representing a payment gateway with a method to process payments.

2. **Relationships:**

- Customer is associated with Cart using a one-to-one relationship.
- Cart has multiple Cart_Items, and each Cart_Item includes a Product.
- Customer can place multiple Orders, and each Order includes multiple Cart_Items.
- Order is associated with Payment, indicating payment for the order.
- Payment uses the PaymentGateway interface for processing payments.

The diagram showcases the basic flow of an online shopping system, from customers registering and browsing products to adding items to the cart, placing orders, and processing payments through a payment gateway.

# Task 3: Develop a Sequence Diagram 
**Objective:** Create a Sequence Diagram that details the sequence of interactions in the "Place Order" use case within the Online Shopping System. 

The provided PlantUML code illustrates a "Place Order" Sequence Diagram with the following interactions:

1. The Customer, represented as an actor, adds items to their shopping cart and reviews the cart.
2. The Shopping Cart creates an Order.
3. The Order adds payment details and sends them to the Payment Gateway.
4. The Payment Gateway processes the payment.
5. The Order updates the Inventory System to reflect the purchase.
6. The Inventory System confirms the inventory update.
7. The Order sends an order confirmation to the Customer.

   
