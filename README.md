📬 Mail-box
A console-based messaging system built in C++ that simulates a basic email/mailbox experience — right from your terminal. Users can create accounts, send messages, manage their inbox and sent box, search messages, star important ones, and handle deleted messages via a trash system.

🚀 Features

Account Management — Sign up, log in, change password, and delete your account
Send Messages — Message any registered user with timestamped delivery
Inbox — View all received messages with read/unread status
Sent Box — Track all messages you've sent
Star / Unstar — Mark important messages in inbox or sent box
Search — Find messages sent to or received from a specific user
Trash — Deleted messages go to trash; permanently delete or read them from there
Input Validation — Handles invalid input gracefully without crashing


🛠️ Tech Stack
ComponentDetailLanguageC++Data StructuresSingly Linked List (messages), Doubly Linked List (users), Vector (trash)Standard Libraries<iostream>, <iomanip>, <ctime>, <vector>, <limits>

📁 Project Structure
Mail-box/
└── main.cpp      # Complete source code (single-file project)

⚙️ How to Compile & Run
Prerequisites

A C++ compiler (g++ recommended)

Steps
bash# Clone the repository
git clone https://github.com/ShivanshPandey07/Mail-box.git
cd Mail-box

# Compile
g++ main.cpp -o mailbox

# Run
./mailbox
On Windows (MinGW):
bashg++ main.cpp -o mailbox.exe
mailbox.exe

🖥️ Usage
On launch, you'll see the main menu:
**** WELCOME TO MESSAGER ****
0. Exit application
1. Create new account
2. Login to your account
3. Delete an existing account
4. Change Password
Once logged in, you can:
***** HELLO @username ! *****
0. Logout
1. Check inbox messages
2. Send a message
3. View sent messages
4. Search messages sent to a user
5. Search messages received from a user
6. View deleted messages
7. View starred messages in Inbox
8. View starred messages in Sentbox

🧠 How It Works

Users are stored in a Doubly Linked List — each node holds the user's credentials and pointers to their sent/received message lists.
Messages are stored in Singly Linked Lists (one for sent, one for received per user), with the newest message always inserted at the head.
Trash is a vector<msg*> that holds pointers to deleted messages for each user.
When a message is sent, two nodes are created — one added to the receiver's inbox and one to the sender's sent box — to keep data independent.
Timestamps are generated using ctime at the moment of sending.


📌 Limitations

Data is not persistent — all accounts and messages are lost when the program exits (no file/database storage).
Runs only in the terminal/console.
Passwords are stored and displayed in plain text (no encryption).


🔭 Possible Future Improvements

 Add file I/O to persist user data between sessions
 Encrypt passwords (e.g., hashing with SHA-256)
 Add a reply-to-message feature
 Support group messaging
 Build a GUI using Qt or a web frontend
