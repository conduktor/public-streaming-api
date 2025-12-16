# Awesome Free Public Real-Time Data Sources

[![Awesome](https://awesome.re/badge-flat.svg)](https://awesome.re)

A curated list of **truly free**, publicly accessible real-time datasets and streaming sources. All sources listed below are accessible without API keys, authentication, or paid subscriptions (though some may have rate limits or usage caps on free tiers).

This list focuses on real-time or near real-time data accessible via HTTP APIs, WebSockets, SSE (Server-Sent Events), or other streaming protocols.

## 🎮 [Try the Live WebSocket Viewer](https://conduktor.github.io/public-streaming-api/)

Test any WebSocket endpoint instantly in your browser! Click on WebSocket links below to connect automatically.

## Table of Contents

- [Finance & Cryptocurrency](#finance--cryptocurrency)
- [Transportation](#transportation)
- [Weather & Environment](#weather--environment)
- [Seismic & Natural Events](#seismic--natural-events)
- [Space & Astronomy](#space--astronomy)
- [Information & News](#information--news)
- [Government & Public Data](#government--public-data)
- [Entertainment & Media](#entertainment--media)
- [IoT & Sensors](#iot--sensors)
- [Social & Community](#social--community)
- [Sports](#sports)
- [Cybersecurity](#cybersecurity)
- [Development & Testing](#development--testing)
- [Geographic & Location](#geographic--location)

---

## Finance & Cryptocurrency

### Cryptocurrency Exchanges (WebSocket)

- **[Coinbase Pro WebSocket](https://docs.cloud.coinbase.com/exchange/docs/websocket-overview)** - Real-time market data including order books, trades, and ticker updates. No authentication required for public channels. [🔴 Try it live](https://conduktor.github.io/public-streaming-api/?wss=wss://ws-feed.exchange.coinbase.com)
  ```
  wss://ws-feed.exchange.coinbase.com
  ```

- **[Binance WebSocket Streams](https://developers.binance.com/docs/binance-spot-api-docs/web-socket-streams)** - Real-time cryptocurrency trading data, order books, and market updates for 1000+ trading pairs. [🔴 Try it live](https://conduktor.github.io/public-streaming-api/?wss=wss://stream.binance.com:9443/ws/btcusdt@trade)
  ```
  wss://stream.binance.com:9443/ws/btcusdt@trade
  ```

- **[Blockchain.com WebSocket](https://www.blockchain.com/api/api_websocket)** - Real-time Bitcoin and Ethereum blockchain transaction notifications. [🔴 Try it live](https://conduktor.github.io/public-streaming-api/?wss=wss://ws.blockchain.info/inv)
  ```
  wss://ws.blockchain.info/inv
  ```

- **[Kraken WebSocket](https://docs.kraken.com/websockets/)** - Real-time cryptocurrency market data. Public feeds available without authentication. [🔴 Try it live](https://conduktor.github.io/public-streaming-api/?wss=wss://ws.kraken.com)
  ```
  wss://ws.kraken.com
  ```

### Cryptocurrency Market Data (SSE)

- **[DexPaprika SSE](https://coinpaprika.com/education/best-free-dex-api-2025-dexpaprika-vs-dextools-vs-geckoterminal-vs-dexscreener-vs-birdeye/)** - Real-time cryptocurrency prices and DEX data via Server-Sent Events. Multi-chain support. No authentication. [🟡 Try it live](https://conduktor.github.io/public-streaming-api/?sse=https://mcp.dexpaprika.com/sse)
  ```
  https://mcp.dexpaprika.com/sse
  ```

### Market Data APIs

- **[CoinGecko API](https://www.coingecko.com/en/api)** - Real-time prices for 12,000+ cryptocurrencies. Free tier: 50 calls/minute, no API key needed for basic endpoints.
  ```
  https://api.coingecko.com/api/v3/simple/price?ids=bitcoin&vs_currencies=usd
  ```

- **[Mempool.space API](https://mempool.space/docs/api)** - Real-time Bitcoin blockchain data including mempool, blocks, transactions. No authentication required.
  ```
  https://mempool.space/api/mempool
  https://mempool.space/api/blocks/tip/height
  ```


---

## Transportation

### Public Transit

- **[Transport for London (TfL) API](https://tfl.gov.uk/info-for/open-data-users/our-open-data)** - Real-time data for London Underground, buses, bikes. No API key required for many endpoints.
  ```
  https://api.tfl.gov.uk/StopPoint/{id}/Arrivals
  ```

- **[Helsinki Regional Transport (HSL)](https://digitransit.fi/en/developers/)** - MQTT-based real-time vehicle positions and transit data.
  ```
  mqtt://mqtt.hsl.fi:1883
  ```

- **[MTA Real-Time Data Feeds](https://new.mta.info/developers)** - NYC subway and bus real-time arrival data in GTFS format. Requires free API key registration.

- **[Transport for NSW Open Data](https://opendata.transport.nsw.gov.au/)** - Real-time public transport data for Sydney, Australia.

### Aviation & Maritime

- **[OpenSky Network API](https://openskynetwork.github.io/opensky-api/rest.html)** - Real-time flight tracking data from crowd-sourced ADS-B receivers. Free tier: 400 requests/day.
  ```
  https://opensky-network.org/api/states/all
  ```

- **[Norwegian Coastal AIS Data](https://www.kystverket.no/en/navigation-and-monitoring/ais/access-to-ais-data/)** - Ship positions via AIS within Norwegian waters.

### Bike Sharing

- **[GBFS (General Bikeshare Feed Specification)](https://github.com/MobilityData/gbfs)** - Real-time bike share data from 400+ systems worldwide.
  - NYC Citi Bike: `https://gbfs.citibikenyc.com/gbfs/gbfs.json`
  - Find more systems: [GBFS Systems List](https://github.com/MobilityData/gbfs/blob/master/systems.csv)

---

## Weather & Environment

### Weather Data

- **[Open-Meteo API](https://open-meteo.com/)** - Free weather API with no API key required. Real-time weather, forecasts, historical data.
  ```
  https://api.open-meteo.com/v1/forecast?latitude=52.52&longitude=13.41&current_weather=true
  ```

- **[NOAA Weather API](https://www.weather.gov/documentation/services-web-api)** - Real-time weather data from US National Weather Service. Requires proper User-Agent header.
  ```bash
  curl -A "YourApp/1.0 (contact@example.com)" https://api.weather.gov/gridpoints/TOP/31,80/forecast
  ```

- **[NOAA Buoy Data](https://www.ndbc.noaa.gov/data/realtime2/)** - Real-time oceanographic and meteorological data from buoys worldwide.

### Air Quality

- **[EPA AirNow API](https://docs.airnowapi.org/)** - US air quality data. Free API key with generous limits.

- **[Sensor.Community API](https://github.com/opendata-stuttgart/meta/wiki/EN-APIs)** - Global crowdsourced air quality data from 15,000+ sensors. No authentication required.
  ```
  https://data.sensor.community/airrohr/v1/filter/area=51.3,7.5,10
  ```

### Water & Flooding

- **[UK Environment Agency Flood API](https://environment.data.gov.uk/flood-monitoring/doc/reference)** - Real-time UK flood monitoring data. No authentication.
  ```
  https://environment.data.gov.uk/flood-monitoring/id/stations
  ```

- **[USGS Water Services](https://waterservices.usgs.gov/)** - Real-time stream flow, groundwater, and water quality data for US.
  ```
  https://waterservices.usgs.gov/nwis/iv/?format=json&sites=01646500&parameterCd=00060,00065
  ```

### Space Weather & Solar Data

- **[NOAA Space Weather Prediction Center (SWPC)](https://www.swpc.noaa.gov/products-and-data)** - Real-time solar wind, geomagnetic, and space weather data. No authentication.
  ```
  https://services.swpc.noaa.gov/products/solar-wind/mag-7-day.json
  https://services.swpc.noaa.gov/products/geospace/geospace-1-day.json
  ```

- **[NASA POWER API](https://power.larc.nasa.gov/docs/)** - Solar and meteorological data from NASA satellites. No authentication.
  ```
  https://power.larc.nasa.gov/api/temporal/daily/point?parameters=T2M&community=RE&longitude=-95.37&latitude=29.76&start=20241201&end=20241201&format=JSON
  ```

### Carbon & Energy

- **[UK Carbon Intensity API](https://carbonintensity.org.uk/)** - Real-time UK electricity carbon intensity. No authentication.
  ```
  https://api.carbonintensity.org.uk/intensity
  https://api.carbonintensity.org.uk/regional
  ```

---

## Seismic & Natural Events

- **[USGS Earthquake API](https://earthquake.usgs.gov/fdsnws/event/1/)** - Real-time earthquake data globally. No authentication required.
  ```
  https://earthquake.usgs.gov/earthquakes/feed/v1.0/summary/all_hour.geojson
  ```

- **[European-Mediterranean Seismological Centre (EMSC) WebSocket](https://www.seismicportal.eu/realtime.html)** - Real-time seismic events via WebSocket. [🔴 Try it live](https://conduktor.github.io/public-streaming-api/?wss=wss://www.seismicportal.eu/standing_order/websocket)
  ```
  wss://www.seismicportal.eu/standing_order/websocket
  ```

---

## Space & Astronomy

- **[NASA APIs](https://api.nasa.gov/)** - Multiple APIs including APOD, Mars Rover photos, asteroids. Free API key with high limits (1000/hour).
  ```
  https://api.nasa.gov/planetary/apod?api_key=DEMO_KEY
  ```

- **[International Space Station (ISS) Position](http://open-notify.org/Open-Notify-API/ISS-Location-Now/)** - Real-time ISS location. No authentication.
  ```
  http://api.open-notify.org/iss-now.json
  ```

- **[SpaceX API](https://github.com/r-spacex/SpaceX-API)** - Real-time data on SpaceX launches, rockets, capsules. No authentication.
  ```
  https://api.spacexdata.com/v4/launches/latest
  ```

- **[N2YO Satellite Tracking API](https://www.n2yo.com/api/)** - Real-time satellite positions. Free tier available.

---

## Information & News

### Wikipedia & Wikimedia

- **[Wikimedia EventStreams](https://wikitech.wikimedia.org/wiki/Event_Platform/EventStreams)** - Server-Sent Events (SSE) stream of real-time edits to Wikipedia and other Wikimedia projects. No authentication required. [🟡 Try it live](https://conduktor.github.io/public-streaming-api/?sse=https://stream.wikimedia.org/v2/stream/recentchange)
  ```bash
  curl -N https://stream.wikimedia.org/v2/stream/recentchange
  ```
  **Additional streams:**
  - Page creation: `https://stream.wikimedia.org/v2/stream/page-create`
  - Page deletion: `https://stream.wikimedia.org/v2/stream/page-delete`
  - Revision create: `https://stream.wikimedia.org/v2/stream/revision-create`

### News Feeds

- **[New York Times Newswire API](https://developer.nytimes.com/docs/timeswire-product/1/overview)** - Up-to-the-minute stream of published NYT articles. Free API key required.

- **[Hacker News API](https://github.com/HackerNews/API)** - Near real-time tech news. Firebase-based, no authentication. Supports both REST and SSE (set Accept header to `text/event-stream`). [🟡 Try SSE live](https://conduktor.github.io/public-streaming-api/?sse=https://hacker-news.firebaseio.com/v0/topstories.json)
  ```
  https://hacker-news.firebaseio.com/v0/topstories.json
  https://hacker-news.firebaseio.com/v0/newstories.json
  ```

### Dictionaries & Reference

- **[Free Dictionary API](https://dictionaryapi.dev/)** - English dictionary definitions. No authentication required.
  ```
  https://api.dictionaryapi.dev/api/v2/entries/en/hello
  ```

- **[DuckDuckGo Instant Answer API](https://duckduckgo.com/api)** - Instant answers for queries including weather, definitions, calculations.
  ```
  https://api.duckduckgo.com/?q=weather&format=json
  ```

---

## Government & Public Data

### Emergency Services

- **[OpenFEMA API](https://www.fema.gov/about/openfema/api)** - Real-time US disaster declarations, flood maps, and emergency management data. No authentication.
  ```
  https://www.fema.gov/api/open/v2/DisasterDeclarationsSummaries
  https://www.fema.gov/api/open/v2/FemaRegions
  ```

- **[NYC Open Data - Fire Incidents](https://data.cityofnewyork.us/)** - Real-time NYC fire department incident data. No authentication.
  ```
  https://data.cityofnewyork.us/resource/8m42-w767.json?$limit=100
  ```

### Health & Disease Tracking

- **[disease.sh COVID-19 API](https://disease.sh/)** - Real-time global COVID-19 statistics. No authentication.
  ```
  https://disease.sh/v3/covid-19/all
  https://disease.sh/v3/covid-19/countries
  ```

### Economic & Financial Data

- **[World Bank API](https://datahelpdesk.worldbank.org/knowledgebase/articles/889392-about-the-indicators-api-documentation)** - Global economic indicators for 200+ countries. No authentication.
  ```
  https://api.worldbank.org/v2/country/us/indicator/NY.GDP.MKTP.CD?format=json&date=2022
  https://api.worldbank.org/v2/country/all/indicator/SP.POP.TOTL?format=json
  ```

- **[US Treasury Fiscal Data](https://fiscaldata.treasury.gov/api-documentation/)** - US government financial data including debt, revenue, spending. No authentication.
  ```
  https://api.fiscaldata.treasury.gov/services/api/fiscal_service/v2/accounting/od/debt_to_penny
  ```

- **[FRED Economic Data (Federal Reserve)](https://fred.stlouisfed.org/docs/api/fred/)** - US economic time series data. Free API key required.
  ```
  https://api.stlouisfed.org/fred/series/observations?series_id=GNPCA&api_key=YOUR_KEY
  ```

---

## Entertainment & Media

### Music

- **[Last.fm API](https://www.last.fm/api)** - Music charts, artist info, and listening trends. Free API key with generous limits.
  ```
  https://ws.audioscrobbler.com/2.0/?method=chart.gettopartists&limit=10&format=json
  ```

- **[Radio Browser API](https://www.radio-browser.info/)** - Global internet radio station directory with 30,000+ stations. No authentication.
  ```
  https://de1.api.radio-browser.info/json/stations/bycountry/usa?limit=100
  https://de1.api.radio-browser.info/json/stations/search?name=jazz
  ```

### Movies & TV

- **[TMDb API](https://www.themoviedb.org/settings/api)** - Movie and TV show data including trending content. Free API key required.
  ```
  https://api.themoviedb.org/3/trending/all/day?api_key=YOUR_KEY
  ```

---

## IoT & Sensors

- **[ThingSpeak Public Channels](https://thingspeak.mathworks.com/channels/public)** - Crowdsourced IoT sensor data (temperature, humidity, radiation, etc.). Accessible via REST API.
  ```
  https://api.thingspeak.com/channels/{channelID}/feeds.json
  ```

- **[PurpleAir Sensors](https://www2.purpleair.com/)** - Real-time air quality from 15,000+ sensors worldwide. Public JSON endpoint available (data may be large).
  ```
  https://www.purpleair.com/data.json?opt=1/mAQI/a10/cC0&fetch=true&nwlat=38&nwlng=-122&selat=37&selng=-121
  ```

---

## Social & Community

### Social Media Streams

- **[Bluesky Firehose](https://docs.bsky.app/docs/advanced-guides/firehose)** - WebSocket stream of all public posts on the Bluesky social network. Requires authentication.

- **[Mastodon Streaming API](https://docs.joinmastodon.org/methods/streaming/)** - Real-time posts from Mastodon instances. Supports both WebSocket and SSE. Public timeline accessible without auth on many instances.
  - **WebSocket:** [🔴 Try it live](https://conduktor.github.io/public-streaming-api/?wss=wss://mastodon.social/api/v1/streaming/public)
    ```
    wss://mastodon.social/api/v1/streaming/public
    ```
  - **SSE:** [🟡 Try it live](https://conduktor.github.io/public-streaming-api/?sse=https://mastodon.social/api/v1/streaming/public)
    ```
    https://mastodon.social/api/v1/streaming/public
    https://mastodon.social/api/v1/streaming/user (requires auth)
    https://mastodon.social/api/v1/streaming/public/local
    ```

- **[Pushshift Reddit Stream](https://github.com/pushshift/reddit_sse_stream)** - Near real-time Reddit comments and submissions via SSE (2-3 second delay). No authentication. ⚠️ Service availability may be intermittent. [🟡 Try it live](https://conduktor.github.io/public-streaming-api/?sse=http://stream.pushshift.io/?type=comments)
  ```
  http://stream.pushshift.io/?type=comments
  http://stream.pushshift.io/?type=submissions
  http://stream.pushshift.io/?type=comments&subreddit=python,javascript
  ```
  **Note:** HTTP only (no SSL), one connection per IP.

- **[Reddit JSON Feeds](https://www.reddit.com/)** - Real-time posts from any subreddit. Add `.json` to any Reddit URL. Note: May require User-Agent header or may block automated access.
  ```bash
  curl -A "MyApp/1.0" https://www.reddit.com/r/programming/new.json
  ```

---

## Sports

- **[Formula 1 Timing Data](https://github.com/theOehrly/Fast-F1)** - Python library to access live F1 timing and telemetry data.

---

## Cybersecurity

- **[Certstream](https://certstream.calidog.io/)** - Real-time certificate transparency log stream via WebSocket. [🔴 Try it live](https://conduktor.github.io/public-streaming-api/?wss=wss://certstream.calidog.io)
  ```
  wss://certstream.calidog.io
  ```

- **[Open Threat Exchange (OTX)](https://otx.alienvault.com/api)** - Threat intelligence feed. Free account required.

---

## Development & Testing

### WebSocket Testing

- **[WebSocket Echo Server](https://websocket.org/tools/websocket-echo-server/)** - Public echo server for WebSocket testing. [🔴 Try it live](https://conduktor.github.io/public-streaming-api/?wss=wss://echo.websocket.org/)
  ```
  wss://echo.websocket.org/
  wss://echo.websocket.events/
  ```

- **[Sandy WebSocket Sandbox](https://www.gosandy.io/)** - Free WebSocket testing sandbox without code.

### SSE Testing

- **[SSE.dev Test Server](https://sse.dev/)** - Public SSE testing endpoint that sends test messages. Customizable interval and data. [🟡 Try it live](https://conduktor.github.io/public-streaming-api/?sse=https://sse.dev/test)
  ```
  https://sse.dev/test
  https://sse.dev/test?interval=5000
  ```

### Image Placeholders

- **[Lorem Picsum](https://picsum.photos/)** - Random placeholder images. No authentication.
  ```
  https://picsum.photos/200/300
  ```

- **[Unsplash Source](https://source.unsplash.com/)** - High-quality random images from Unsplash. No API key for basic use.
  ```
  https://source.unsplash.com/random
  ```

### Mock Data

- **[JSONPlaceholder](https://jsonplaceholder.typicode.com/)** - Free fake REST API for testing and prototyping.
  ```
  https://jsonplaceholder.typicode.com/posts
  ```

- **[Random User Generator](https://randomuser.me/)** - Generate random user data. No authentication.
  ```
  https://randomuser.me/api/
  ```

---

## Geographic & Location

- **[REST Countries API](https://restcountries.com/)** - Country data including flags, currencies, languages. No authentication.
  ```
  https://restcountries.com/v3.1/all
  ```

- **[IP Geolocation (ipify)](https://www.ipify.org/)** - Get public IP address. No authentication.
  ```
  https://api.ipify.org?format=json
  ```

- **[IP Geolocation (ip-api.com)](https://ip-api.com/)** - Free IP geolocation. No API key required for non-commercial use.
  ```
  http://ip-api.com/json/
  ```

---

## License

[![CC0](https://licensebuttons.net/p/zero/1.0/88x31.png)](https://creativecommons.org/publicdomain/zero/1.0/)

To the extent possible under law, the contributors have waived all copyright and related rights to this work.

---

## Sources & References

This list was compiled from research across multiple sources:

- [Mixed Analytics - Free Open APIs (No Auth)](https://mixedanalytics.com/blog/list-actually-free-open-no-auth-needed-apis/)
- [Apipheny - 90+ Free APIs](https://apipheny.io/free-api/)
- [GitHub: public-apis/public-apis](https://github.com/public-apis/public-apis)
- [GitHub: awesome-public-streaming-datasets](https://github.com/ColinEberhardt/awesome-public-streaming-datasets)
- [GitHub: awesome-public-real-time-datasets (Bytewax)](https://github.com/bytewax/awesome-public-real-time-datasets)
- [Ably - 10 Realtime Data Sources](https://ably.com/blog/10-realtime-data-sources-you-wont-believe-are-free)
- [Apidog - Best Free Crypto WebSocket APIs](https://apidog.com/blog/free-crypto-websocket-api/)
- [DEV Community - Free Public APIs 2025](https://dev.to/therealmrmumba/10-free-public-apis-im-actually-using-as-a-developer-in-2025-2p3)
