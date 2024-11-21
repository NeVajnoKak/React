# Drag and Drop Card Sorting Application

This project is a simple React-based application that demonstrates how to implement a drag-and-drop functionality for reordering cards. Each card can be dragged and dropped to change its order dynamically.

## Features

- **Drag-and-Drop Functionality**: Cards can be reordered by dragging and dropping them into new positions.
- **Dynamic State Management**: The application uses React's `useState` hook to manage the state of the card list and update the order.
- **Visual Feedback**: Provides visual cues (e.g., background color changes) during drag-and-drop operations.

## Installation and Setup

1. **Clone the Repository**:  
   ```bash
   git clone <repository-url>
   ```
2. **Navigate to the Project Directory**:
   ```bash
   cd <project-directory>
   ```
3. **Install Dependencies**:
   ```bash
   npm install
   ```
4. **Run the Application**:
   ```bash
   npm start
    ```
The application will be available at http://localhost:3000.

## How It Works

### State Management
- The cardList state holds an array of card objects, each with an id, order, and text.
- The currentCard state tracks the card being dragged.
### Event Handlers
1. dragStartHandler(e, card):

- Triggered when a drag operation starts.
- Sets the currentCard to the card being dragged.
2. dragEndHandler(e):
  
- Triggered when the drag operation ends.
- Resets the card's background color.
3. dragOverHandler(e):

- Triggered when a card is dragged over another card.
- Prevents default behavior and provides a visual cue.
4. dropHandler(e, card):

- Triggered when a card is dropped onto another card.
- Updates the order of the cards in the list based on their new positions.
### Sorting
- The sortCard function ensures the cards are displayed in the correct order based on their order property.
### Rendering
- The cardList is sorted and mapped to render draggable div elements, each representing a card.
### File Structure
- App.js: Contains the main application logic, including the drag-and-drop functionality.
- App.css: Styles for the cards and application layout.
### Example
Initially, the cards are displayed in the following order:

1. КАРТОЧКА 1
2. КАРТОЧКА 2
3. КАРТОЧКА 3
4. КАРТОЧКА 4
You can drag a card (e.g., "КАРТОЧКА 3") and drop it above another card (e.g., "КАРТОЧКА 1") to reorder them.

### Customization
- Modify the cardList array in the useState hook to add or remove cards.
- Update styles in App.css to customize the appearance of the cards.
### Technologies Used
- React
- JavaScript
- CSS
### Future Enhancements
- Add animations for smoother transitions during reordering.
- Save the updated order in a database or local storage.
- Enhance accessibility for better keyboard navigation.
