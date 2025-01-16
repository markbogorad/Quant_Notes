up:: [[Computer Science MOC]]
tags:: #Programming  
# MVC
- A software design pattern commonly used for developing user interfaces that divides the related program logic into three interconnected elements. 
- This separation helps to manage complexity and enables efficient code reusability, modular development, and separation of concerns.
![[Pasted image 20240726093541.png]]
### Components of MVC:
1. **Model:**
    - **Definition:** The model represents the data and the business logic of the application.
    - **Responsibilities:**
        - Manages the data and business rules.
        - Responds to requests for information (queries) and updates (commands) from the view and controller.
        - Notifies the view when data changes so the view can update itself.
    - **Example:** In a shopping cart application, the model would handle the data related to the products, pricing, and user’s cart contents.
2. **View:**
    - **Definition:** The view is the user interface of the application.
    - **Responsibilities:**
        - Displays data to the user.
        - Sends user commands (e.g., button clicks) to the controller.
    - **Example:** In the same shopping cart application, the view would be the HTML/CSS pages that display the product listings and the shopping cart to the user.
3. **Controller:**
    - **Definition:** The controller acts as an intermediary between the model and the view.
    - **Responsibilities:**
        - Receives input from the view (user actions) and processes it.
        - Commands the model to update its state.
        - Decides which view to display based on the model’s state.
    - **Example:** In the shopping cart application, the controller would handle actions like adding a product to the cart or checking out, updating the model accordingly, and then selecting the appropriate view to display the updated cart.
### Advantages of MVC:
- **Separation of Concerns:** Divides the application into three distinct components, making it easier to manage and scale.
- **Modularity:** Each component can be developed, tested, and maintained independently.
- **Reusability:** The same model can be used with multiple views.
- **Maintainability:** Changes in one component typically require minimal changes in others.