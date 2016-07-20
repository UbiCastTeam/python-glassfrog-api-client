# python-glassfrog-api-client
A Glassfrog API client written in python to integrate Holacracy with internal tools

## Setup
Create an API key from https://app.glassfrog.com/api_keys ; duplicate the config.json.sample into config.json, replace the API key by the one you just created

## Usage

If you wish to explore the api, you can use the example methods or directly call other endpoints

```
ipython -i glassfrog_api_client.py
In [1]: gf.get_circle(include_members=True)['circles'][0]
Out[8]: 
{'id': 13366,
 'links': {'domain': [],
  'people': [37856, 37897, 37898],
  'policies': [8162235, 8162236, 8120309, 8120459],
  'roles': [8254078,
   8252616,
   8253398,
   8253868,
   8252614,
   8253780,
   8252615,
   8253778],
  'supported_role': 8252613},
 'name': 'Board',
 'short_name': 'Board',
 'strategy': 'Focus on: reach profitability\r\nThen on: ensure reliability "UbiCast: it works"\r\nEven over: innovation'}

In [2]: gf.api('circles')['circles'][0]
Out[2]: 
{'id': 13366,
 'links': {'domain': [],
  'policies': [8162235, 8162236, 8120309, 8120459],
  'roles': [8254078,
   8252616,
   8253398,
   8253868,
   8252614,
   8253780,
   8252615,
   8253778],
  'supported_role': 8252613},
 'name': 'Board',
 'short_name': 'Board',
 'strategy': 'Focus on: reach profitability\r\nThen on: ensure reliability "UbiCast: it works"\r\nEven over: innovation'}
```
