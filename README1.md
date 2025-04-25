Explanation

Import Libraries:
streamlit for creating the web interface.
requests for making HTTP requests to the Ollama API.
json to handle JSON payloads.
Streamlit Setup:
st.title(): Sets the title of the app.
st.session_state: Used to store chat history, persisting across user interactions.
Sidebar elements for model selection and system prompt.
Ollama API Interaction:
ollama_url: The endpoint for the Ollama API. This assumes Ollama is running on the default port.
send_message_to_ollama():
Sends the user's message to the Ollama API using a POST request.
Includes the model name and system prompt in the request.
Handles potential errors (connection issues, invalid JSON, API errors).
Returns the response text from Ollama, or an error message.
Chat Interface:
Displays previous chat messages using st.session_state.messages.
st.chat_input(): Creates the input field for the user to type their message.
When the user enters a message:
The message is added to st.session_state.messages.
The message is displayed in the chat interface.
The message is sent to Ollama using send_message_to_ollama().
The response from Ollama is displayed.
The response is added to st.session_state.messages.
Key Improvements

Error Handling: Robust error handling for API requests and JSON parsing. Includes the response text in the error message to help with debugging.
Clearer Structure: The code is organized into functions for better readability.
Comments: Detailed comments explain each section of the code.
State Management: Uses st.session_state to maintain chat history.
Model Selection: Added a dropdown to select the Ollama model.
System Prompt: Added a text area to set the system prompt.
Clearer error messages.
Handles edge cases where the Ollama API might not return a 'message' or 'content' field.
