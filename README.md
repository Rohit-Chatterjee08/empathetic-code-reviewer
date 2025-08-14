title: The Empathetic Code Reviewer emoji: 🤝 colorFrom: indigo colorTo: blue sdk: gradio sdk_version: 4.31.0 app_file: app.py pinned: false
🤝 The Empathetic Code Reviewer
Hackathon Mission 1: "Freedom from Mundane: AI for a Smarter Life"
This application is my solution for Mission 1: The Empathetic Code Reviewer. It addresses the often friction-filled and mundane task of code reviews by using Generative AI to transform blunt, critical feedback into supportive, educational, and constructive guidance.

🎯 My Approach
My strategy was to build a reliable and user-friendly tool that directly addresses the core problem: the negative emotional impact of poorly delivered feedback.

Model Selection & Prompt Engineering: I chose to use a powerful Large Language Model (LLM) as the core of the application. The main challenge was designing a "master prompt" that could consistently instruct the AI to act as an expert, empathetic mentor. The prompt engineering was iterative, focusing on getting the AI to not just rephrase comments, but to also explain the underlying software principles (the "why") and provide concrete, corrected code examples.

Implementing "Stand-Out" Features: To go beyond the basic requirements, I focused on two key features mentioned in the problem statement:

Linking to Resources: I explicitly instructed the AI to include URLs to official documentation (like Python's PEP 8) to add credibility and further educational value.

Holistic Summary: I added a final, separate AI call to generate an encouraging summary, ensuring the review ends on a positive and motivating note.

User Interface (UI): I used Gradio to create a simple, "low-code" web interface. This makes the tool accessible to anyone with a web browser, requiring no complex setup and allowing for easy testing with a single click.

⚙️ Testing Instructions
This application is deployed as a public Hugging Face Space. You can test it directly in your browser.

Open the Application: Navigate to the application's public URL.

Use the Example: The app loads with the default example from the problem statement. Simply click the "Generate Empathetic Report" button to see a live demonstration.

Test with Your Own Input:

Enter any Python code snippet into the "Code Snippet" box.

Enter one or more critical review comments into the "Review Comments" box. Ensure each comment is on a new line.

Click the "Generate Empathetic Report" button.

Verify the Output: The AI-generated report will appear in the output panel on the right. Check for the key components: a positive rephrasing, a clear explanation ("The 'Why'"), a code suggestion, and the final summary.

🔑 API Key Configuration
This application requires access to a Large Language Model API to function. The code is written to be flexible.

Primary Method (Google Gemini)
The application is configured by default to use the Google Gemini API. To run this Space, a GOOGLE_API_KEY must be set in the repository's secrets.

Alternative LLM Providers (e.g., Groq, Local LLMs)
As per the hackathon guidelines, the application can be easily adapted to use other LLM providers like Groq for open-source models (e.g., Llama 3, Mixtral) or a locally hosted LLM.

To adapt the code:

Modify the call_gemini_api function in app.py:

Change the api_url to the endpoint for your chosen provider (e.g., Groq's API endpoint).

Adjust the payload structure to match the specific format required by the new API.

Update the API key handling to use the relevant secret name (e.g., GROQ_API_KEY).

Update Repository Secrets: Add the new API key to the Hugging Face Space secrets under the appropriate name.