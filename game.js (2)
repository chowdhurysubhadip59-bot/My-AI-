
// My AI Friend ❤️

// Open AI Chat
function openAI() {
  let oldChat = document.getElementById("aiChatWindow");
  if (oldChat) oldChat.remove();

  const chat = document.createElement("div");
  chat.id = "aiChatWindow";

  chat.style.cssText = `
    position:fixed;
    inset:0;
    z-index:9999;
    background:#f8f0ff;
    display:flex;
    flex-direction:column;
    font-family:Arial,sans-serif;
  `;

  chat.innerHTML = `
    <div style="
      background:linear-gradient(120deg,#9146d9,#e85bb5);
      color:white;padding:20px;
      display:flex;justify-content:space-between;
      align-items:center;">
      <h2>🤖 AI Friend ❤️</h2>
      <button onclick="closeAI()"
        style="background:white;color:#8b44bd">✖</button>
    </div>

    <div id="chatMessages" style="
      flex:1;overflow-y:auto;padding:15px;">
      <p style="
        background:white;padding:15px;
        border-radius:15px;">
        Hello! ❤️ I am your AI Friend.
        Tell me anything!
      </p>
    </div>

    <div style="
      display:flex;padding:12px;gap:8px;
      background:white;">
      <input id="chatInput"
        placeholder="Write your message..."
        style="flex:1;min-width:0;padding:13px;
        border:1px solid #ddd;border-radius:20px;">

      <button onclick="sendAIMessage()"
        style="background:#9146d9;color:white;
        padding:12px;border:0;border-radius:20px;">
        Send
      </button>
    </div>
  `;

  document.body.appendChild(chat);

  document.getElementById("chatInput")
    .addEventListener("keydown", function(e) {
      if (e.key === "Enter") sendAIMessage();
    });
}

// Close Chat
function closeAI() {
  const chat = document.getElementById("aiChatWindow");
  if (chat) chat.remove();
}

// Send Message
function sendAIMessage() {
  const input = document.getElementById("chatInput");
  const messages = document.getElementById("chatMessages");

  const message = input.value.trim();
  if (!message) return;

  const user = document.createElement("p");
  user.textContent = "You: " + message;
  user.style.cssText =
    "background:#e9d5ff;padding:12px;border-radius:12px;text-align:right;";

  messages.appendChild(user);
  input.value = "";

  const reply = document.createElement("p");
  reply.textContent = "AI Friend: " + getAIReply(message);
  reply.style.cssText =
    "background:white;padding:12px;border-radius:12px;";

  messages.appendChild(reply);
  messages.scrollTop = messages.scrollHeight;
}

// Demo AI Reply
function getAIReply(message) {
  const text = message.toLowerCase();

  if (text.includes("hello") || text.includes("hi"))
    return "Hello my friend! ❤️ How are you?";

  if (text.includes("how are you"))
    return "I am fine! 😊 What about you?";

  if (text.includes("sad") || text.includes("মন খারাপ"))
    return "Don't worry. I am here to listen to you. ❤️";

  if (text.includes("name"))
    return "I am your AI Friend! What is your name?";

  if (text.includes("ভালো"))
    return "বাহ! শুনে খুব ভালো লাগল। ❤️";

  return "That's interesting! 😊 Tell me more, my friend.";
}

// Other Sections
function openFriends() {
  alert("👫 Real People Chat will be added next!");
}

function openVoice() {
  alert("🎤 Voice Chat will be added next!");
}

function showProfile() {
  alert("👤 Welcome to your Profile!");
}

function goHome() {
  window.scrollTo({top:0,behavior:"smooth"});
}

function setLanguage(language) {
  alert("Selected Language: " + language);
}
