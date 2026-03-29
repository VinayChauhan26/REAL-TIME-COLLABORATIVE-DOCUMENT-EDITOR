# REAL-TIME-COLLABORATIVE-DOCUMENT-EDITOR

"COMPANY":CODTECH IT SOLUTIONS

"NAME":VINAY CHOUHAN

"INTERN ID":CTIS7061

"DOMAIN":FULL STACK DEVELOPMENT

"DURATION":4 WEEKS

"MENTOR":NEELA SANTOSH

Description-

My DocEditor project is a real‑time collaborative text editor built using the MERN stack along with Quill.js and Socket.IO. The idea behind the application is to allow multiple users to work on the same document simultaneously, with changes instantly reflected across all connected clients. I wanted to create something that feels similar to Google Docs but lightweight and customizable, so I combined React for the frontend, Node.js and Express for the backend, MongoDB for persistence, and Quill as the rich text editor.

On the frontend, React renders the Quill editor inside the page. Quill provides formatting options like bold, italic, headings, and lists, which makes the editing experience smooth and user‑friendly. When the editor loads, it connects to the backend using Socket.IO. The client requests a specific document, for example “doc1,” and the server responds by loading its saved content from MongoDB. Initially, the editor is disabled and shows a “Loading…” message until the document arrives. Once the content is loaded, the editor is enabled and ready for collaboration.

The real‑time aspect is handled through Socket.IO. Whenever a user types or makes a formatting change, Quill generates a delta (a description of the change). This delta is sent to the server, which then broadcasts it to all other connected clients. Each client applies the delta to its own editor, so everyone sees the same updates instantly. This ensures that multiple users can edit together without overwriting each other’s work. To prevent unnecessary loops, only changes made by the user are sent, while incoming changes are applied silently.

Another important feature is auto‑saving. Every two seconds, the client sends the current document state to the server, which stores it in MongoDB. This means that even if users disconnect or close the editor, their work is preserved. The next time someone opens the document, they see the latest version. This combination of real‑time updates and periodic saving makes the editor reliable and collaborative.


OUTPUT-- 

<img width="1912" height="958" alt="Image" src="https://github.com/user-attachments/assets/d1448c52-cd44-4d63-b78e-46bd56369654" />
