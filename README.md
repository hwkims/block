# 🪙 Block Messenger: A Simple Blockchain-Based Messenger with Coin Features (Simulation)

[![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)](https://www.javascript.com/)
[![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/Guide/HTML/HTML5)
[![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/CSS)

**Block Messenger** is an educational project that simulates a basic blockchain-based messenger with integrated coin functionality.  It's built using pure HTML, CSS, and JavaScript, demonstrating fundamental blockchain concepts in a simplified, interactive way.  This project is intended for learning purposes and is *not* suitable for real-world cryptocurrency transactions or secure messaging.

**[Important Note]:** This project is a *simulation* and does not implement a true distributed network, robust consensus algorithm, or secure smart contracts. It is designed to illustrate concepts, not to provide production-ready functionality.

## ✨ Features

*   **Simulated Blockchain:**  Messages and coin transactions are added to a simplified blockchain structure.  This includes:
    *   **Block Creation:**  Each block contains a timestamp, data (messages or transactions), the previous block's hash, and a nonce (for Proof-of-Work simulation).
    *   **Hashing:**  Uses CryptoJS's SHA256 algorithm for hashing.
    *   **Proof-of-Work (PoW):**  Simulates mining with adjustable difficulty.  A loading animation visually represents the mining process.
    *   **Chain Validation:**  Includes a basic `isChainValid()` function to demonstrate integrity checks.
*   **Messaging:**
    *   Send and receive text messages.
    *   Messages are displayed in a chat-like interface with timestamps.
    *   Emoji support.
    *   Distinguishes between messages sent by the current user and other (simulated) users.
*   **Coin System (Simulated):**
    *   Each "node" (browser tab) starts with an initial coin balance.
    *   Users earn a small "mining reward" for each block created (when sending a message or a transaction).
    *   Coin transactions are recorded on the blockchain.
    *   A simple modal allows users to send coins (to a placeholder "otherNode").
    *   Balance updates are reflected in the UI.
*   **UI/UX:**
    *   Mobile-first design, resembling an iPhone-style messaging app.
    *   Basic animations (loading spinner, button hover effects).
*   **Debugging:**  A hidden section (toggleable) displays the current blockchain data in JSON format.

## 🛠️ Technologies Used

*   **HTML5:**  For structure and content.
*   **CSS3:**  For styling and layout.
*   **JavaScript (Vanilla JS):**  For all logic, including blockchain simulation, message handling, and UI interactions.
*   **CryptoJS:**  For SHA256 hashing ([https://cdnjs.cloudflare.com/ajax/libs/crypto-js/4.1.1/crypto-js.min.js](https://cdnjs.cloudflare.com/ajax/libs/crypto-js/4.1.1/crypto-js.min.js)).

## 🚀 How to Run

1.  **Clone the repository:**

    ```bash
    git clone https://github.com/hwkims/block.git
    ```
2.  **Navigate to the project directory:**

    ```bash
    cd block
    ```
3.  **Open `index.html` in your web browser.**  No server is required; you can simply double-click the file.

## 🧪 Testing and Interaction

*   **Send Messages:** Type a message in the input field and press Enter or click the "Send" button.  A loading animation will appear briefly, simulating the mining process.
*   **Send Coins:** Click the coin icon to open the coin transfer modal. Enter an amount and click "Send".  Again, a loading animation will simulate mining.
*   **Open Multiple Tabs:** For a better simulation of a multi-node network, open the `index.html` file in multiple browser tabs.  Each tab represents a separate "node." *Note:*  There is no actual data synchronization between tabs. Each tab maintains its own independent blockchain.
*   **Developer Tools:**  Use your browser's developer tools (usually F12) to:
    *   Inspect the console for "Block mined" messages.
    *   Examine the `myBlockchain` object to see the current state of the blockchain.
    *   (Optional)  Unhide the `#blockchain-info` div to view the blockchain data directly on the page.
    *   Experiment with modifying the blockchain data manually to test the `isChainValid()` function.

## ⚠️ Limitations and Future Improvements

This project is a simplified simulation and has several limitations:

*   **No Real P2P Network:**  There's no actual peer-to-peer communication.  Opening multiple tabs simulates multiple nodes, but they don't interact.  True P2P would require technologies like WebRTC and a signaling server (which needs a backend like Node.js).
*   **Simplified Consensus:** The project uses a basic Proof-of-Work simulation and a rudimentary "longest chain" rule, but it doesn't handle real-world consensus challenges (like forks or network latency).
*   **No Smart Contracts:** The "coin" functionality is implemented directly in JavaScript.  It does not represent true smart contract capabilities.
*   **Security:**  This project is *not* secure and should *never* be used for real-world cryptocurrency or sensitive data.  There is no key management, transaction signing, or protection against various attacks.
*   **Persistence:**  Data is lost when the browser tab is closed.  Persistence would require a backend (database) or distributed storage (like IPFS).

**Potential Future Enhancements (Beyond the Scope of this Simple Project):**

*   Implement basic P2P communication using WebRTC (requires a signaling server).
*   Explore more sophisticated consensus algorithms.
*   Simulate basic smart contract features with more complex JavaScript functions.
*   Add a visual representation of the blockchain (blocks and connections).
*   Use a library like `localForage` for basic data persistence within the browser.

## 🧑‍💻 Contributing

This project is primarily for educational purposes, but contributions to improve clarity, fix bugs, or enhance the simulation are welcome!  Please submit pull requests with clear explanations of your changes.

## 📜 License

This project is open-source and available under the [MIT License](LICENSE) (You'll need to create a LICENSE file).
