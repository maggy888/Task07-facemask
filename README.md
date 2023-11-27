import requests
import json

#利用requests對API來源發送一個請求

facemask = ("https://raw.githubusercontent.com/kiang/pharmacies/master/json/points.json")
response = requests.get(facemask)

#請求回應的內容存成一個字串格式
d = response.text

# 將長得像 json 格式的字串解析成字典或列表
data = json.loads(d)

print(data)
