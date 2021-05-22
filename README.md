# SpiderKeeper
### This is a fork of [SpiderKeeper-2-1](https://github.com/shiaukuan/SpiderKeeper)

## Features

- Manage your spiders from a dashboard. Schedule them to run automatically
- With a single click deploy the scrapy project
- Show spider running stats
- Provide api


Current Support spider service
- [Scrapy](https://github.com/scrapy/scrapy) ( with [scrapyd](https://github.com/scrapy/scrapyd))

## Screenshot
![job dashboard](https://raw.githubusercontent.com/DormyMo/SpiderKeeper/master/screenshot/screenshot_1.png)
![periodic job](https://raw.githubusercontent.com/DormyMo/SpiderKeeper/master/screenshot/screenshot_2.png)
![running more_stats](https://github.com/jrbeduardo/SpiderKeeper/blob/master/screenshot/Screenshot%20at%202021-05-22%2012-16-38.png)
## Getting Started


### Installing


```
pip install git+https://github.com/jrbeduardo/SpiderKeeper.git
```

### Deployment

``` 

spiderkeeper [options]

Options:

  -h, --help            show this help message and exit
  --host=HOST           host, default:0.0.0.0
  --port=PORT           port, default:5000
  --username=USERNAME   basic auth username ,default: admin
  --password=PASSWORD   basic auth password ,default: admin
  --type=SERVER_TYPE    access spider server type, default: scrapyd
  --server=SERVERS      servers, default: ['http://localhost:6800']
  --database-url=DATABASE_URL
                        SpiderKeeper metadata database default: sqlite:////home/souche/SpiderKeeper.db
  --no-auth             disable basic auth
  -v, --verbose         log level
  --executor            ThreadPoolExecutor ,default: 30
  --process             processpool ,default: 3
  

example:

spiderkeeper --server=http://localhost:6800

```

## Usage

```
Visit: 

- web ui : http://localhost:5000

1. Create Project

2. Use [scrapyd-client](https://github.com/scrapy/scrapyd-client) to generate egg file 

   scrapyd-deploy --build-egg output.egg

2. upload egg file (make sure you started scrapyd server)

3. Done & Enjoy it

- api swagger: http://localhost:5000/api.html

``` 

## Authors

- *Initial work* - [DormyMo](https://github.com/DormyMo)
- *Fork author* - [kalombo](https://github.com/kalombos/)
- *Fork kalombo* - [shiaukuan](https://github.com/shiaukuan/)
- *Fork jrbeduardo* - [jrbeduardo](https://github.com/jrbeduardo/)

## Contributing

Contributions are welcomed!


