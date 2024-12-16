
New version:
The **Music Store Rental Management System** is a Python application aimed at assisting store managers in overseeing their music record inventory and rental activities. This system allows users to search for music records, manage rentals and returns, and gather customer feedback. Additionally, it helps identify less popular music records that may be candidates for removal, thereby optimizing inventory space.

The project is developed using **JupyterLab** and utilizes `IPyWidgets` to create an intuitive graphical user interface.

---

## Features
### Core Functionalities
1. **Music Search**:
   - Users can search for records by artist, title, medium, or genre.
   - Detailed information is displayed, including the availability of each record.

2. **Music Rental**:
   - Customer subscriptions are validated through `subscriptionManager.pyc`.
   - Music records can be rented to active subscribers, ensuring compliance with subscription limits.
   - The inventory is updated following successful rentals.

3. **Music Return and Feedback**:
   - The system processes returns, updates the inventory, and collects customer feedback (including star ratings and comments).
   - Feedback is recorded using `feedbackManager.pyc`.

4. **Inventory Pruning**:
   - The system identifies and recommends the removal of records that are not frequently rented.
   - Visualizations are provided to aid in decision-making.

### Data Management
- The system maintains two text-based databases:
  1. `Music_Info.txt`: Contains details about the music inventory (artist, title, medium, etc.).
  2. `Rental.txt`: Records rental transactions (including rental and return dates, customer IDs).

- Customer feedback is automatically saved in `Music_Feedback.txt`.

---

## File Structure
### Data Files
- `Music_Info.txt`: Holds the initial inventory (a minimum of 20 records is required).
- `Rental.txt`: Keeps a log of rental history (at least 100 records are needed).

### Python Modules
- **`musicSearch`**: Responsible for searching music records.
- **`musicRent`**: Oversees the rental process.
- **`musicReturn`**: Manages returns and the collection of feedback.
- **`InventoryPruning`**: Suggests and visualizes records for potential removal based on rental frequency.
