# 免费 API 节点大全

> 50+ 类别，无需注册即可使用的免费 API 节点

## 目录

- [文本生成/对话](#文本生成对话)
- [图像生成/处理](#图像生成处理)
- [语音合成(TTS)](#语音合成tts)
- [语音转文字(STT)](#语音转文字stt)
- [翻译](#翻译)
- [OCR文字识别](#ocr文字识别)
- [天气](#天气)
- [新闻](#新闻)
- [地图/地理](#地图地理)
- [IP查询](#ip查询)
- [二维码/条形码](#二维码条形码)
- [货币汇率](#货币汇率)
- [加密货币](#加密货币)
- [股票数据](#股票数据)
- [DNS查询](#dns查询)
- [URL缩短](#url缩短)
- [测试API](#测试api)
- [GitHub API](#github-api)
- [文本处理](#文本处理)
- [UUID生成](#uuid生成)
- [颜色工具](#颜色工具)
- [单位转换](#单位转换)
- [天文/太空](#天文太空)
- [地震数据](#地震数据)
- [游戏数据](#游戏数据)
- [体育数据](#体育数据)
- [菜谱/食物](#菜谱食物)
- [医疗健康](#医疗健康)
- [Meme生成](#meme生成)
- [安全工具](#安全工具)
- [占位图](#占位图)
- [Webhook测试](#webhook测试)
- [邮件发送](#邮件发送)
- [推送通知](#推送通知)
- [端口扫描](#端口扫描)
- [免费AI聚合平台](#免费ai聚合平台)

---

## 文本生成/对话

| 服务 | 地址 | 特点 |
|------|------|------|
| Pollinations.ai | `https://text.pollinations.ai/{prompt}` | GET直接用 |
| KeylessAI | `https://keylessai.thryx.workers.dev/v1` | OpenAI兼容 |
| ApiAirforce | `https://api.airforce/v1/chat/completions` | 多免费模型 |
| LLM7.io | `https://api.llm7.io/v1` | 30+模型 |
| OVH AI | `https://oai.endpoints.kepler.ai.cloud.ovh.net/v1` | 2req/min |
| Carpathian AI | `https://api.carpathian.ai/ai` | 无上限 |
| DevToolBox | `https://devtoolbox-api.devtoolbox-api.workers.dev/ai/generate` | 26个端点 |

```bash
# 示例
curl "https://text.pollinations.ai/What%20is%20AI"
curl "https://keylessai.thryx.workers.dev/v1/chat/completions" -X POST -H "Content-Type: application/json" -d '{"model":"gpt-3.5-turbo","messages":[{"role":"user","content":"Hello"}]}'
```

## 图像生成/处理

| 服务 | 地址 | 功能 |
|------|------|------|
| Pollinations.ai | `https://image.pollinations.ai/prompt/{prompt}` | 文生图 |
| BGNinja | `https://bgninja.com/api/remove` | 背景去除 |
| wsrv.nl | `https://wsrv.nl/` | 图片resize |
| reSmush.it | `http://api.resmush.it/ws.php` | 图片压缩 |
| img2txt | `https://img2txt.genzouw.com` | 图片转ASCII |

```bash
# 示例
curl -o img.jpg "https://image.pollinations.ai/prompt/a%20cat"
curl -X POST https://bgninja.com/api/remove -F "image=@photo.jpg" -o result.png
curl -o resized.jpg "https://wsrv.nl/?url=example.com/image.jpg&w=300"
```

## 语音合成(TTS)

| 服务 | 地址 | 特点 |
|------|------|------|
| Edge TTS | `pip install edge-tts` | 400+声音 |
| TTS.ai | `https://api.tts.ai/v1/tts/` | 5000字符/天 |
| UncloseAI | `https://speech.ai.unturf.com/v1` | OpenAI兼容 |
| SpeechSter | `https://ahm7xmakki.com/api/tts` | 580+声音 |
| tts-free.com | 浏览器端 | 完全本地运行 |

```bash
# 示例
edge-tts --text "你好世界" --write-media hello.mp3
curl "https://speech.ai.unturf.com/v1/audio/speech" -X POST -H "Content-Type: application/json" -d '{"model":"tts-1","input":"Hello","voice":"alloy"}' --output speech.mp3
```

## 语音转文字(STT)

| 服务 | 地址 | 特点 |
|------|------|------|
| Puter.js | `https://api.puter.com/v1/ai/speech2txt` | 无需Key |
| Mod9 ASR | `https://mod9.io/rest/api/speech:recognize` | 无限制 |
| WhisperWeb | `https://whisperweb.dev` | 浏览器端 |

## 翻译

| 服务 | 地址 | 特点 |
|------|------|------|
| Google非官方 | `https://translate.googleapis.com/translate_a/single` | 100+语言 |
| MyMemory | `https://api.mymemory.translated.net/get` | 200+语言 |
| Lingva | `https://lingva.ml/api/v1/{sl}/{tl}/{text}` | 隐私前端 |
| LibreTranslate | `https://libretranslate.com/translate` | 开源可自部署 |

```bash
# 示例
curl "https://translate.googleapis.com/translate_a/single?client=gtx&sl=en&tl=zh-CN&dt=t&q=hello"
curl "https://api.mymemory.translated.net/get?q=Hello&langpair=en|zh-CN"
```

## OCR文字识别

| 服务 | 地址 | 特点 |
|------|------|------|
| OCR.space | `https://api.ocr.space/Parse/Image` | Key填`helloworld` |
| Tesseract.js | 本地运行 | 完全免费 |

```bash
# 示例
curl -H "apikey:helloworld" -F "file=@image.jpg" https://api.ocr.space/Parse/Image
```

## 天气

| 服务 | 地址 | 特点 |
|------|------|------|
| Open-Meteo | `https://api.open-meteo.com/v1/forecast` | 10000次/天 |
| wttr.in | `https://wttr.in/{城市}?format=j1` | 多格式输出 |

```bash
# 示例
curl "https://api.open-meteo.com/v1/forecast?latitude=39.9&longitude=116.4&current=temperature_2m"
curl "https://wttr.in/Beijing?format=j1"
```

## 新闻

| 服务 | 地址 | 特点 |
|------|------|------|
| freenewsapi.ai | `https://freenewsapi.ai/v1/search` | 20req/s |
| Hacker News | `https://hacker-news.firebaseio.com/v0/` | 无限 |
| Reddit RSS | `https://www.reddit.com/r/news/.rss` | 无限 |

```bash
# 示例
curl "https://freenewsapi.ai/v1/search?q=AI&size=5"
curl "https://hacker-news.firebaseio.com/v0/topstories.json"
```

## 地图/地理

| 服务 | 地址 | 特点 |
|------|------|------|
| Nominatim | `https://nominatim.openstreetmap.org/search` | 1req/s |
| Photon | `https://photon.komoot.io/api/` | 自动补全 |

```bash
# 示例
curl "https://nominatim.openstreetmap.org/search?q=Beijing&format=json"
curl "https://photon.komoot.io/api/?q=Berlin"
```

## IP查询

| 服务 | 地址 | 特点 |
|------|------|------|
| ip-api.com | `http://ip-api.com/json` | 45次/分 |
| ipapi.co | `https://ipapi.co/{ip}/json/` | 字段丰富 |
| ipwhois.io | `http://ipwho.is/{ip}` | VPN检测 |

```bash
# 示例
curl "http://ip-api.com/json/"
curl "https://ipapi.co/8.8.8.8/json/"
curl "http://ipwho.is/8.8.8.8"
```

## 二维码/条形码

| 服务 | 地址 | 特点 |
|------|------|------|
| QRCode.Fun | `https://qrcode.fun/api/qr-image?data={content}` | 无限制 |
| qrserver.com | `https://api.qrserver.com/v1/create-qr-code/` | 多格式 |
| BarcodeAPI | `https://barcodeapi.org/api/128/{text}` | 多种条码 |

```bash
# 示例
curl -o qr.png "https://qrcode.fun/api/qr-image?data=hello"
curl -o qr.png "https://api.qrserver.com/v1/create-qr-code/?size=200x200&data=Hello"
curl -o barcode.png "https://barcodeapi.org/api/128/Hello"
```

## 货币汇率

| 服务 | 地址 | 特点 |
|------|------|------|
| Frankfurter | `https://api.frankfurter.dev/v2/rates` | 201种货币 |
| ExchangeRate-API | `https://open.er-api.com/v6/latest/USD` | 每日更新 |

```bash
# 示例
curl "https://api.frankfurter.dev/v2/rates/EUR/USD"
curl "https://open.er-api.com/v6/latest/USD"
```

## 加密货币

| 服务 | 地址 | 特点 |
|------|------|------|
| CoinGecko | `https://api.coingecko.com/api/v3/simple/price` | 最全面 |
| Coinbase | `https://api.coinbase.com/v2/prices/BTC-USD/spot` | 简单快速 |
| Binance | `https://api.binance.com/api/v3/ticker/price` | 交易对数据 |

```bash
# 示例
curl "https://api.coingecko.com/api/v3/simple/price?ids=bitcoin,ethereum&vs_currencies=usd"
curl "https://api.coinbase.com/v2/prices/BTC-USD/spot"
curl "https://api.binance.com/api/v3/ticker/price?symbol=BTCUSDT"
```

## 股票数据

| 服务 | 地址 | 特点 |
|------|------|------|
| Alpha Vantage | `https://www.alphavantage.co/query?apikey=demo` | demo可用 |
| Yahoo Finance | `https://query1.finance.yahoo.com/v8/finance/chart/` | 非官方 |

```bash
# 示例
curl "https://www.alphavantage.co/query?function=TIME_SERIES_DAILY&symbol=IBM&apikey=demo"
curl "https://query1.finance.yahoo.com/v8/finance/chart/AAPL?interval=1d&range=5d"
```

## DNS查询

| 服务 | 地址 | 特点 |
|------|------|------|
| Google DoH | `https://dns.google/resolve?name={domain}` | 无限制 |
| Cloudflare DoH | `https://1.1.1.1/dns-query` | 最快 |

```bash
# 示例
curl "https://dns.google/resolve?name=example.com&type=A"
curl "https://dns.google/resolve?name=example.com&type=MX"
```

## URL缩短

| 服务 | 地址 | 特点 |
|------|------|------|
| Cleanuri | `https://cleanuri.com/api/v1/shorten` | 简单 |
| v.gd | `https://v.gd/create.php` | 极简 |
| TinyURL | `https://tinyurl.com/api-create.php` | 经典 |

```bash
# 示例
curl -X POST "https://cleanuri.com/api/v1/shorten" -d "url=https://example.com"
curl "https://v.gd/create.php?url=https://example.com"
curl "https://tinyurl.com/api-create.php?url=https://example.com"
```

## 测试API

| 服务 | 地址 | 特点 |
|------|------|------|
| JSONPlaceholder | `https://jsonplaceholder.typicode.com` | 假数据REST |
| httpbin | `https://httpbin.org` | HTTP测试 |
| DummyJSON | `https://dummyjson.com` | 丰富假数据 |

```bash
# 示例
curl "https://jsonplaceholder.typicode.com/posts/1"
curl "https://httpbin.org/get"
curl "https://dummyjson.com/products/1"
```

## GitHub API

| 服务 | 地址 | 特点 |
|------|------|------|
| GitHub REST | `https://api.github.com/` | 60次/小时匿名 |

```bash
# 示例
curl "https://api.github.com/repos/facebook/react"
curl "https://api.github.com/search/repositories?q=language:javascript&sort=stars"
```

## 文本处理

| 服务 | 地址 | 功能 |
|------|------|------|
| Jina Reader | `https://r.jina.ai/{url}` | 网页转Markdown |
| DeepAI | `https://api.deepai.org/api/text-summarizer` | 文本摘要 |
| SENTIM | `https://sentim-api.onrender.com/api/v1/` | 情感分析 |

```bash
# 示例
curl "https://r.jina.ai/https://example.com"
curl -X POST "https://api.deepai.org/api/text-summarizer" -F "text=Your long text here"
curl -X POST "https://sentim-api.onrender.com/api/v1/" -H "Content-Type: application/json" -d '{"text":"I love this product!"}'
```

## UUID生成

| 服务 | 地址 | 特点 |
|------|------|------|
| uuid.rocks | `https://uuid.rocks/json` | 最快 |
| createuuid.com | `https://createuuid.com/api/v4` | 多版本 |

```bash
# 示例
curl "https://uuid.rocks/json"
curl "https://createuuid.com/api/v4"
```

## 颜色工具

| 服务 | 地址 | 功能 |
|------|------|------|
| ColorUI | `https://colorui.io/api/v1/` | 调色板+转换 |
| The Color API | `https://thecolorapi.com/id` | 颜色信息 |

```bash
# 示例
curl "https://thecolorapi.com/id?hex=FF5733"
curl "https://colorui.io/api/v1/random"
```

## 单位转换

| 服务 | 地址 | 特点 |
|------|------|------|
| Convertitive | `https://convertitive.com/api/v1/convert/unit` | 无限制 |
| UnitFYI | `https://unitfyi.com/api/convert/` | 200+单位 |

```bash
# 示例
curl "https://convertitive.com/api/v1/convert/unit?value=1&from=km&to=miles"
curl "https://unitfyi.com/api/convert/?value=100&from=celsius&to=fahrenheit"
```

## 天文/太空

| 服务 | 地址 | 特点 |
|------|------|------|
| NASA APOD | `https://api.nasa.gov/planetary/apod?api_key=DEMO_KEY` | 每日天文图 |
| ISS位置 | `https://api.wheretheiss.at/v1/satellites/25544` | 实时位置 |
| NASA图片 | `https://images-api.nasa.gov/search` | 海量图片 |

```bash
# 示例
curl "https://api.nasa.gov/planetary/apod?api_key=DEMO_KEY"
curl "https://api.wheretheiss.at/v1/satellites/25544"
curl "https://images-api.nasa.gov/search?q=apollo%2011"
```

## 地震数据

| 服务 | 地址 | 特点 |
|------|------|------|
| USGS | `https://earthquake.usgs.gov/fdsnws/event/1/query` | 实时数据 |

```bash
# 示例
curl "https://earthquake.usgs.gov/fdsnws/event/1/query?format=geojson&minmagnitude=5"
```

## 游戏数据

| 服务 | 地址 | 特点 |
|------|------|------|
| FreeToGame | `https://www.freetogame.com/api/games` | 400+免费游戏 |
| GamerPower | `https://www.gamerpower.com/api/giveaways` | 赠品追踪 |

```bash
# 示例
curl "https://www.freetogame.com/api/games"
curl "https://www.gamerpower.com/api/giveaways"
```

## 体育数据

| 服务 | 地址 | 特点 |
|------|------|------|
| TheSportsDB | `https://www.thesportsdb.com/api/v1/json/1/` | Key填`1` |
| OpenLigaDB | `https://api.openligadb.de/` | 德甲无限 |

```bash
# 示例
curl "https://www.thesportsdb.com/api/v1/json/1/lookup_all_teams.php?l=English_Premier_League"
curl "https://api.openligadb.de/getmatchdata/bl1/2023"
```

## 菜谱/食物

| 服务 | 地址 | 特点 |
|------|------|------|
| TheMealDB | `https://www.themealdb.com/api/json/v1/1/` | Key填`1` |
| Open Food Facts | `https://world.openfoodfacts.org/api/v2/` | 600万+产品 |

```bash
# 示例
curl "https://www.themealdb.com/api/json/v1/1/random.php"
curl "https://world.openfoodfacts.org/api/v2/product/3017620422003.json"
```

## 医疗健康

| 服务 | 地址 | 特点 |
|------|------|------|
| OpenFDA | `https://api.fda.gov/drug/label.json` | 药品数据 |
| ClinicalTrials | `https://clinicaltrials.gov/api/v2/studies` | 临床试验 |
| disease.sh | `https://disease.sh/v3/covid-19/all` | COVID数据 |

```bash
# 示例
curl "https://api.fda.gov/drug/label.json?limit=5"
curl "https://clinicaltrials.gov/api/v2/studies?queryCond=diabetes"
curl "https://disease.sh/v3/covid-19/all"
```

## Meme生成

| 服务 | 地址 | 特点 |
|------|------|------|
| justmeme.wtf | `https://justmeme.wtf/api/v1` | 2400+模板 |
| memegen.link | `https://api.memegen.link` | 开源 |

```bash
# 示例
curl -o meme.jpg "https://api.memegen.link/images/buzz/lightyear/everywhere/everywhere_at_once.jpg"
```

## 安全工具

| 服务 | 地址 | 功能 |
|------|------|------|
| HackMyIP | `https://hackmyip.com/api/blacklist` | IP黑名单检查 |
| Blackbox | `https://blackbox.ipinfo.app/api/v1/` | VPN/Proxy检测 |
| Netbait | `https://api.netbait.org/v1/score/` | 滥用评分 |

```bash
# 示例
curl "https://hackmyip.com/api/blacklist?ip=8.8.8.8"
curl "https://blackbox.ipinfo.app/api/v1/8.8.8.8"
curl "https://api.netbait.org/v1/score/8.8.8.8"
```

## 占位图

| 服务 | 地址 | 特点 |
|------|------|------|
| Picsum | `https://picsum.photos/200/300` | 高质量照片 |
| placeholdr.dev | `https://placeholdr.dev/800x600` | AI风格化 |

```bash
# 示例
curl -o photo.jpg "https://picsum.photos/200/300"
curl -o placeholder.jpg "https://placeholdr.dev/800x600"
```

## Webhook测试

| 服务 | 地址 | 特点 |
|------|------|------|
| Webhook.site | `https://webhook.site` | 经典 |
| Hook0 | `https://play.hook0.com` | 开源 |

## 邮件发送

| 服务 | 地址 | 特点 |
|------|------|------|
| Resend | `https://api.resend.com/emails` | 3000封/月 |
| Mailgun | `https://api.mailgun.net/v3/` | 100封/天 |

## 推送通知

| 服务 | 地址 | 特点 |
|------|------|------|
| ntfy | `https://ntfy.sh/{topic}` | 零配置 |
| Telegram Bot | `https://api.telegram.org/bot{TOKEN}/sendMessage` | 免费 |

## 端口扫描

| 服务 | 地址 | 特点 |
|------|------|------|
| Shodan InternetDB | `https://internetdb.shodan.io/{ip}` | 已知端口 |
| portscan.com | `https://api.portscan.com/v1/fast` | 自身IP扫描 |

## 免费AI聚合平台

| 服务 | 地址 | 特点 |
|------|------|------|
| OmniRoute | 本地部署 | 227提供商 |
| Free.ai | `https://free.ai` | 400+工具 |
| OpenAPIs | `https://openapis.online` | GPT+Claude |

---

## License

MIT
