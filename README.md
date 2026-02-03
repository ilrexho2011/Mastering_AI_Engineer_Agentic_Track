### Code and deploy AI Agents with OpenAI Agents SDK, CrewAI, LangGraph, AutoGen and MCP

![Autonomous Agent](assets/ai_agent.jpeg)

### Important notes for CrewAI

Windows PC users: you will need to have checked the "gotcha #4" at the top of the [SETUP-PC](setup/SETUP-PC.md) instructions -- installing Microsoft Build Tools.  
If you don't do this, then CrewAI will fail with an obscure error involving Chroma..


Then, you will need to run this command in a Cursor Terminal in the project root directory in order to run the Crew commands:  
`uv tool install crewai==0.130.0 --python 3.12`   
And in case you've used Crew before, it might be worth doing this to make sure you have the latest:  
`uv tool upgrade crewai==0.130.0 --python 3.12`  

If you have any problems with Crew, you could try using the latest version instead, by running this command:  
`uv tool upgrade crewai --python 3.12`  

At any point, you can see which version of Crew you have installed with this:  
`uv tool list`

Sidenote: a "tool" with uv is a utility that is installed globally by uv. After installing this tool, you can use "crewai" as a command, and it runs the code associated with this tool.

Then please keep in mind for Crew:

1. There are two ways that you can work on the CrewAI project. Either review the code for each project while I build it, and then do `crewai run` to see it in action. Or if you prefer to be more hands-on, then create your own Crew project from scratch to mirror mine; for example, create `my_debate` to go alongside `debate`, and write the code alongside me. Either approach works!  
2. Windows users: there's a new issue that was recently introduced by one of Crew's libraries. Until this is fixed, you might get a "unicode" error when you try to run `crewai create crew`.  If that happens, please try running this command in the Terminal first: `$env:PYTHONUTF8 = "1"`  
3. Gemini users: in addition to a key in your `.env` file for `GOOGLE_API_KEY`, you will need an identical key for `GEMINI_API_KEY`

### API costs - please read me!

This course does involve making calls to OpenAI and other frontier models, requiring an API key and a small spend, which we set up in the SETUP instructions. If you'd prefer not to spend on API calls, there are cheaper alternatives like DeepSeek and free alternatives like using Ollama!

Be sure to monitor your API costs to ensure you are totally happy with any spend. For OpenAI, the dashboard is [here](https://platform.openai.com/usage).
