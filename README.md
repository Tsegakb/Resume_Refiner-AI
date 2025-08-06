# Resume_Refiner-AI
Assignment
1 ### Overview
The Resume Refiner AI Agent is an automated workflow built using n8n that helps job seekers customize their resumes for specific job postings. By submitting a resume file, job posting URL, and email address through a form, the workflow extracts text from the resume, retrieves job details, and uses an AI model (OpenAI) to generate personalized resume suggestions. These suggestions are then emailed back to the user to improve their chances of landing the job.


2. n8n full agent workflow.
![Flow](https://github.com/user-attachments/assets/a9d39ad3-70f0-4fd4-bf54-8bf00d35e1ca)
3. I used "on form submission" as my Triger connected to HTTP Request connected to AI Agent orchestrator (connected to Open AI ChatGPT Agent ) connected to GMAIL.


4. I encountered 2 problems related with parsing, first was the uploaded token was more than the AI Agent can read so i used Function node to truncate before passing it to the Agent.
Second Agent can parse the the content of uploaded resume so i was getting my resume refined based on the Assumed content of my resume based on the naming, so i used a parser node before passing bit to the Agent. Formatting and integrating i didn't have problem.

5. I ensured the AI returned JSON reliably by crafting clear instructions in the system prompt to only produce valid JSON. I add JSON structure examples: for job description and filename
6. For the issue i faced i solved it by using addition nodes.
7. I think i can improve on the area making the flow shorter by practicing more
![2](https://github.com/user-attachments/assets/058266b1-c54b-470c-a3a2-a23378d70c70)
8
![3](https://github.com/user-attachments/assets/677465ea-55b8-44e3-8018-e19988c06b64)

10. Configuration of your AI agent node
 ![4](https://github.com/user-attachments/assets/39332ea5-9c4f-411d-9cfd-a3105388dcdc)

11`. Configuration of your trigger and email node.

![5](https://github.com/user-attachments/assets/58f3ab10-f12e-4939-9134-2e9b5f61ec88)
