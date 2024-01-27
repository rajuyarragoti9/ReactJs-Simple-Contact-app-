# Project Overview

## Architecture

This React-based Contact Manager application follows a component-based architecture, which is a popular approach for building scalable and maintainable user interfaces. The key components of the project include:

- **App Component (`src/components/App.js`):**

  - Manages the state of contacts using the `useState` hook and stores them in local storage using the `useEffect` hook.
  - Renders the `Header`, `AddContact`, and `ContactList` components.
  - Passes a function (`addContactHandler`) to `AddContact` to handle the addition of new contacts.

- **AddContact Component (`src/components/AddContact.js`):**

  - A form component for adding new contacts with input fields for name and email.
  - Uses local state to track the input values.
  - Prevents form submission if required fields are not filled.
  - Invokes a function (`addContactHandler`) passed from the parent (`App`) to add a new contact.

- **ContactList Component (`src/components/ContactList.js`):**

  - Receives a list of contacts as props and maps through them to render individual `ContactCard` components.
  - `ContactCard` components are created for each contact.

- **ContactCard Component (`src/components/ContactCard.js`):**

  - Displays a single contact with a name, email, and a placeholder avatar.
  - Includes a delete icon (trash symbol) which doesn't have functionality implemented in the provided code.

- **Header Component (`src/components/Header.js`):**
  - Displays a simple header with the text "Contact Manager".

## React Component Rendering Process

React follows a unidirectional data flow, and the rendering process involves the following steps:

1. **State Initialization:**

   - State is initialized using the `useState` hook in functional components or the `this.state` in class components.

2. **Component Rendering:**

   - Components are rendered based on their initial state and props.

3. **User Interaction:**

   - User interactions trigger events, such as form submissions or button clicks.

4. **State Update:**

   - State is updated using functions like `setState` in class components or the updater function in functional components.

5. **Re-rendering:**
   - The component re-renders with the updated state, reflecting changes in the user interface.

## Key Concepts

- **State Management:**

  - State is managed using the `useState` hook in functional components, allowing components to react to changes and update the UI accordingly.

- **Effect Hook:**

  - The `useEffect` hook is used to perform side effects in functional components, such as fetching data or updating local storage.

- **Component Composition:**

  - Components are composed together, with each component responsible for a specific part of the UI or functionality.

- **Local Storage:**

  - The `localStorage` API is used to persistently store and retrieve contact data between sessions.

- **Conditional Rendering:**

  - Conditional rendering is implemented to display error messages and handle mandatory form fields.

- **React StrictMode:**
  - The application is wrapped in `React.StrictMode` in `src/index.js` to highlight potential issues during development.

Feel free to explore and extend this Contact Manager application based on your requirements!
