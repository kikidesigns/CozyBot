# 3D Expo Web App - Screen Specifications

## 1. Welcome Screen (Agent Customization Screen)
### Purpose
- Allows users to log in and customize their AI agent.

### Components
- **Logo**: Displayed at the top center.
- **Login Inputs**: Two centered input boxes for `npub` and `nsec`.
- **3D Agent Pawn**: Represents the agent associated with the `npub`.
- **Customization Options**:
  - Name input (enabled only if `nsec` is available).
  - Color wheel for selecting pawn color.
- **Action Buttons**:
  - Checkmark button to confirm changes.
  - Refresh button to clear data and reset the agent account.

### UI Elements
- Logo (centered top)
- Text input fields (npub & nsec, centered)
- 3D agent pawn (React Three Fiber)
- Name input (centered under 3D pawn)
- Color wheel (agent customization)
- Checkmark button (confirm changes)
- Refresh button (reset agent account)

---

## 2. Home Screen
### Purpose
- Displays the agent on a 3D platform with interactive elements.

### Components
- **3D Environment**:
  - Agent pawn moving around on a platform.
  - White circle in the distance resembling the sun.
- **Game UI Elements**:
  - **Top Left**:
    - Round avatar profile picture.
    - Health bar.
    - Journal button (round shape below avatar pic).
  - **Top Right**:
    - Wallet balance displayed in a pill-shaped container (satoshis).
  - **Bottom**:
    - Chat input field.
    - **Agent Chat Overlay**: Displays chat messages from the agent above the input field, occupying up to the bottom third of the screen.
      - Scrollable chat overlay fading out towards the top.
      - Overlayed over the 3D scene, similar to the Faerie app design.

### UI Elements
- 3D platform (React Three Fiber)
- Agent pawn (movable)
- Sun-like white circle in the distance
- Profile picture (round, top left)
- Health bar (top left)
- Journal button (round, below avatar)
- Wallet balance (pill-shaped, top right)
- Chat input field (bottom)
- Scrollable chat overlay (bottom third of screen, fading effect)

---

## 3. Wallet Screen
### Purpose
- Implements the latest best practices for Lightning wallets.

### Components
- **Wallet Details**: Displays Lightning wallet balance and transaction history.
- **Transaction Controls**: Buttons for sending and receiving payments.
- **Back Button**: Returns to the previous screen.
- **Backend Functionality**:
  - The AI agent can search Nostr for items for sale, trending content, or content from a specific user or friends associated with the `npub`.

### UI Elements
- Wallet balance display
- Transaction history list
- Send/Receive payment buttons
- Back button (top left)

---

## 4. Journal Screen
### Purpose
- Displays a list of tasks for the agent.

### Components
- **Task List**: Shows available tasks.
- **Task Details**: Clicking a task opens a screen displaying:
  - Task description
  - Associated files
  - Buttons to leave a comment, confirm, or deny the task.
- **Back Button**: Returns to the previous screen.
- **Backend Functionality**:
  - The AI agent can search Nostr for relevant content related to the tasks.

### UI Elements
- Scrollable task list
- Task detail view
- Comment input field
- Confirm/Deny buttons
- Back button (top left)

---

## 5. Task Screen
### Purpose
- Displays task details and action options.

### Components
- **Task Information**: Detailed description of the task.
- **Action Buttons**:
  - Leave a comment.
  - Confirm task completion.
  - Deny task.
- **Back Button**: Returns to the journal screen.
- **Backend Functionality**:
  - The AI agent can retrieve Nostr-based content relevant to the task.

### UI Elements
- Task description panel
- Associated files section
- Comment input field
- Confirm/Deny buttons
- Back button (top left)

---

## Navigation Flow
1. **Welcome Screen** → Log in & Customize Agent → **Home Screen**
2. **Home Screen** → Journal button → **Journal Screen**
3. **Home Screen** → Wallet balance → **Wallet Screen**
4. **Journal Screen** → Select Task → **Task Details Screen**
5. **Task Details Screen** → Back Button → **Journal Screen**
6. **Wallet Screen** → Back Button → **Home Screen**
