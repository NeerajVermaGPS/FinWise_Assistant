# FinWise_Assistant
A financial management chatbot designed to help users manage debt, track expenses, and provide financial advice. Users interact naturally with the bot, receiving guidance on debt repayment strategies, savings plans, and budgeting. The bot securely collects necessary financial information and provides accurate responses and step-by-step guidance.
This project demonstrates how to integrate IBM Watson Assistant into a web application using JavaScript.

## IBM Watson Assistant Integration

To integrate IBM Watson Assistant into your own project, follow these steps:

1. **Sign up for IBM Cloud:**
   - If you haven't already, sign up for an IBM Cloud account at [IBM Cloud](https://cloud.ibm.com/).

2. **Create an instance of Watson Assistant:**
   - Go to the [IBM Cloud Catalog](https://cloud.ibm.com/catalog/services/watson-assistant) and create an instance of Watson Assistant.
   - Note down the `Service Instance ID`, `Integration ID`, and `Region` provided in the IBM Cloud dashboard for your Watson Assistant instance.

3. **Configure the integration in your project:**
   - Open the `index.html` or relevant HTML file where you want to integrate Watson Assistant.
   - Locate the JavaScript configuration for Watson Assistant (usually in `<script>` tags or a separate JavaScript file).

4. **Update the integration settings:**
   - Replace `{Integration ID}`, `{Region}`, and `{Service Instance ID}` in the JavaScript configuration with the values obtained from your Watson Assistant instance on IBM Cloud.
   
     Example:
     ```javascript
     window.watsonAssistantChatOptions = {
       integrationID: "your_integration_id",
       region: "your_region",
       serviceInstanceID: "your_service_instance_id",
       onLoad: async (instance) => { await instance.render(); }
     };
     ```

5. **Include Watson Assistant script:**
   - Ensure that the script tag importing WatsonAssistantChatEntry.js includes the correct version and path:
   
     Example:
     ```javascript
     setTimeout(function(){
       const t=document.createElement('script');
       t.src="https://web-chat.global.assistant.watson.appdomain.cloud/versions/" + (window.watsonAssistantChatOptions.clientVersion || 'latest') + "/WatsonAssistantChatEntry.js";
       document.head.appendChild(t);
     });
     ```

6. **Testing:**
   - Open your web application to test the integration of Watson Assistant.
   - You should see the Watson Assistant chat widget loaded with your assistant's configuration.

## Find more at [My Website](https://neerajvermagps.000webhostapp.com/)

