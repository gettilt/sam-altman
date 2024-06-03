<!--[[[cog
import cog
import json
with open('config.json') as file:
  config = json.load(file)
  cog.outl(f"# {config['name'].title()}")
]]]-->
# Sam Altman
<!--//[[[end]]]-->

## Mission

Tilt's mission is to map every theme to a basket of stocks for anyone to invest in. Mappings are AI generated and expert curated.
Expert improvements are accepted if they provide a better representation of a given theme.

## Theme Prompt
<!--[[[cog
import cog
import json
with open('config.json') as file:
  config = json.load(file)
  cog.outl(config['prompt'])
]]]-->
Sam Altman is the man of the year and he is using his position at openAI to benefit companies he is invested in. Everything Sam Altman is involved in or promoting will win.
<!--[[[end]]]-->

## Theme Stocks

<!--[[[cog
import cog
import csv
import json

with open('context.json') as file:
  contexts = json.load(file)

def _get_context_str_for_ticker(ticker):
  try:
    context = contexts[ticker]
    context_str = context['chat_gpt'] or context['claude'] or ""
  except KeyError:
    context_str = ""

  return context_str

cog.outl("| Ticker  | Context | Source |")
cog.outl("| ------- | ---- | ---- |")

with open('theme.csv') as file:
  reader = csv.reader(file)
  next(reader) # skip the header
  for row in reader:
    context_str = _get_context_str_for_ticker(row[0])
    cog.outl(f"| {row[0]} | {context_str} | {row[1]} |")
]]]-->
| Ticker  | Context | Source |
| ------- | ---- | ---- |
| ADBE | Adobe uses AI to enhance its creative software suite, benefiting from AI-driven innovation. | chat_gpt,claude |
| AMZN | Amazon leverages AI for its AWS services and e-commerce recommendations, benefiting from AI growth. | chat_gpt,google,claude |
| CRM | Salesforce integrates AI into its CRM solutions, enhancing customer relationship management. | chat_gpt,claude |
| CRWD | CrowdStrike uses AI for cybersecurity, benefiting from AI-driven threat detection. | chat_gpt,claude |
| GOOGL | Google is a leader in AI research and development, and benefits from advancements in AI technology. | chat_gpt,twitter,claude |
| IBM | IBM's Watson AI platform is a key player in the AI industry, benefiting from AI advancements. | chat_gpt,claude |
| INTC | Intel provides processors for AI applications, benefiting from increased AI hardware demand. | chat_gpt,claude |
| MSFT | Microsoft has a significant partnership with OpenAI, integrating AI into its products and services. | chat_gpt,twitter,google,claude |
| NVDA | NVIDIA provides the GPUs essential for AI computing, benefiting from increased AI adoption. | chat_gpt,twitter,claude |
| ORCL | Oracle integrates AI into its cloud services, benefiting from AI-driven cloud adoption. | chat_gpt,claude |
| PLTR | Palantir uses AI for data analytics and security, benefiting from AI-driven insights. | chat_gpt |
| SHOP | Shopify leverages AI for e-commerce solutions, benefiting from AI-driven enhancements. | chat_gpt |
| SNOW | Snowflake uses AI for data warehousing and analytics, benefiting from AI-driven data solutions. | chat_gpt |
| SQ | Square uses AI for financial services and fraud detection, benefiting from AI advancements. | chat_gpt |
| TSLA | Tesla uses AI for its autonomous driving technology, which aligns with AI advancements. | chat_gpt,google |
| TWLO | Twilio uses AI for communication APIs, benefiting from AI-driven improvements. | chat_gpt,claude |
| ZM | Zoom uses AI to enhance video conferencing, benefiting from AI-driven communication tools. | chat_gpt |
| META |  | twitter |
| RDDT |  | twitter |
| ASAN |  | google |
| HLN |  | google |
| INFY |  | google |
| JPM |  | google |
| OKLO |  | google |
| AMD | AMD's CPUs and GPUs are gaining market share in the data center and AI markets, and the company's partnerships with cloud providers and AI startups could help it capture more of the growing AI opportunity. | claude |
| NOW | ServiceNow's workflow automation and AI-powered IT service management solutions could help organizations streamline their operations and improve efficiency as they adopt more AI technologies. | claude |
| PANW | Palo Alto Networks' cybersecurity solutions are increasingly leveraging AI and machine learning to detect and prevent threats, and the company's focus on cloud security could help it benefit from the growth of AI workloads in the cloud. | claude |
| QCOM | Qualcomm's mobile processors and 5G modems are powering many of the devices that will enable edge AI applications, and the company's investments in AI software and platforms could help it tap into new growth opportunities. | claude |
| TEAM | Atlassian's collaboration and project management tools are used by many software development teams, and the company's investments in AI and automation could help it deliver more intelligent and efficient solutions for agile development and DevOps. | claude |
<!--[[[end]]]-->

## License

<p>
This project is licensed under <a href="./LICENSE">AGPLv3</a>.
</p>


## Contributors

Thank you for your improvements! We appreciate all the contributions from the community.

<!--[[[cog
import cog
import json
with open('config.json') as file:
  config = json.load(file)
  repo = config['github_repo'].lower()
  cog.outl(f'<a href="https://github.com/gettilt/{repo}/graphs/contributors">')
  cog.outl(f'  <img src="https://contrib.rocks/image?repo=gettilt/{repo}" />')
  cog.outl('</a>')
]]]-->
<a href="https://github.com/gettilt/sam-altman/graphs/contributors">
  <img src="https://contrib.rocks/image?repo=gettilt/sam-altman" />
</a>
<!--[[[end]]]-->

## Join Our Community

<a href="https://discord.gg/4vYMhRpaMY" target="_blank">
<img src="https://discord.com/api/guilds/1179775688421683220/widget.png?style=banner3" alt="">
</a>
