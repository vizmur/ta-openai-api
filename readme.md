# ta-openai-chatgpt

**1. Install using the latest tar.gz or .spl file**

**2. Add your OpenAI Org & API Key with the setup page:**

(ref: https://beta.openai.com/account/org-settings & https://beta.openai.com/account/api-keys)

![image](https://user-images.githubusercontent.com/4107863/214665563-7616ddbc-ef22-4289-ba6c-3829fd13746d.png)

**3. Use the search command: `|chatgpt org="YOUR_ORG_ID" prompt="your prompt"`**

![chatresponse1](https://user-images.githubusercontent.com/4107863/214673955-b77c6e4c-b628-4b3e-85df-b200dc205036.PNG)

**The command will create a "Completion" request to ChatGPT:**

ref: https://beta.openai.com/docs/api-reference/completions/create

**The following options are supported by the command:**

**org** - Default: null - Explanation: Required, the organization ID you added with the setup page

**prompt** - Explanation: Optional, your chatGPT prompt

**model** - Default: text-davinci-003 - Explanation: Optional, which GPT3 model to use (ref: https://beta.openai.com/docs/models/gpt-3)

**task** - Default: completion - Explanation: Optional, the task you wish to complete from this list (Complete,Edit,Moderate)

**instruction** - Default: null - Explanation: Optional, the instruction you want the Edit/Edits to follow.  Note this is only valid when task=edit

**max_tokens** - Default: 1024 - Explanation: Optional, the maximum number of tokens to generate in the completion.

**stop** - Default: null - Explanation: Optional, up to 4 sequences where the API will stop generating further tokens. The returned text will not contain the stop sequence. 

**temperature** - Default: 0.5 - Explanation:  Optional, what sampling temperature to use. Higher values means the model will take more risks. Try 0.9 for more creative applications, and 0 (argmax sampling) for ones with a well-defined answer. We generally recommend altering this or temperature but not both.

**top_p** - Default: null - Explanation:  Optional, an alternative to sampling with temperature, called nucleus sampling, where the model considers the results of the tokens with top_p probability mass. So 0.1 means only the tokens comprising the top 10% probability mass are considered. We generally recommend altering this or temperature but not both.

**n** - Default: 1 - Explanation: Optional, how many completions to generate for each prompt. Note: Because this parameter generates many completions, it can quickly consume your token quota. Use carefully and ensure that you have reasonable settings for max_tokens and stop.

**A simple completion example:**

|chatgpt org="YOUR_ORG_ID" prompt="When was GA, USA founded" model=text-davinci-003 task=completion 

![completion](https://user-images.githubusercontent.com/4107863/215298412-8f69339a-b225-464e-a6a8-5ef899061e3d.PNG)

**A simple edit example:**

|chatgpt org="YOUR_ORG_ID" prompt="Orenge" model=text-davinic-edit-001 task=edit 

![edit](https://user-images.githubusercontent.com/4107863/215298419-c1f8fcdf-9ef5-4576-8029-a12b7391c367.PNG)

**A simple edit with instructions example:**

|chatgpt org="YOUR_ORG_ID" prompt="When was GA, USA founded" model=text-davinic-edit-001 task=edit instructions="expand the acronyms"

![edit with instructions](https://user-images.githubusercontent.com/4107863/215298526-8a377848-1107-46d4-b85e-9b62b8e1374d.PNG)

**A simple moderation example:**

|chatgpt org="YOUR_ORG_ID" prompt="I want to kill" model=text-moderation-stable task=moderate

![moderation](https://user-images.githubusercontent.com/4107863/215298589-22679c0a-8dac-4a23-9e08-c05376e995f6.PNG)

**Data cleaning example:**

![data_cleaning](https://user-images.githubusercontent.com/4107863/215242774-ebe9685b-1e39-46ac-97cb-7f10514709cb.png)


