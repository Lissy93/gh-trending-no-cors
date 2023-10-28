
<h1 align="center">Github Trending Repos API</h1>
<p align="center">
<i align="center">A REST API to fetch a list of trending GitHub repositories</i><br />
<i align="center">A fork of <a href="https://github.comxdgongs/github-trending">xdgongs/github-trending</a>, but with CORS enabled</i>
</p>
<p align="center">
  <img src="https://camo.githubusercontent.com/75e813184f7600d2366e22811908f672141e7569f50dd85512b8827baf7bc971/68747470733a2f2f692e6962622e636f2f37347250797a432f6f63746f6361742d636c65616e2e706e67" width="150" />
</p>

> [!WARNING]
> Heroku has recently removed all free plans, and bumped up their pricing 😔  
> Therefore the API is temporarily offline, while I find an alternative platform, suggestions welcome!

## Usage

Requests can be made to: `https://gh-trending-repos.herokuapp.com/repo`. No auth is required.

### Parameters

| Name  | Type   | Description                                                                  |
|-------|--------|------------------------------------------------------------------------------|
| lang  | string | *Optional* - The language of trending repository. Do not include `#` characters |
| since | string | *Optional* - The timeframe, can be either `daily`, `weekly` or `monthly`. Defaults to `daily` |

For example request this address: `https://gh-trending-repos.herokuapp.com/repo?lang=java&since=weekly`

<details><summary><b>Example Response</b></summary>

```json
{
"count": 25,
"msg": "suc",
"items": [
  {
    "repo": "TencentARC/GFPGAN",
    "repo_link": "https://github.com/TencentARC/GFPGAN",
    "desc": "GFPGAN aims at developing Practical Algorithms for Real-world Face Restoration.",
    "lang": "Python",
    "stars": "10,767",
    "forks": "1,635",
    "added_stars": "5,356 stars this week",
    "avatars": [
      "https://avatars.githubusercontent.com/u/17445847?s=40&v=4",
      "https://avatars.githubusercontent.com/u/81195143?s=40&v=4",
      "https://avatars.githubusercontent.com/u/18028233?s=40&v=4",
      "https://avatars.githubusercontent.com/u/36897236?s=40&v=4",
      "https://avatars.githubusercontent.com/u/17243165?s=40&v=4"
    ]
  },
  {
    "repo": "dendibakh/perf-book",
    "repo_link": "https://github.com/dendibakh/perf-book",
    "desc": "The book \"Performance Analysis and Tuning on Modern CPU\"",
    "lang": "TeX",
    "stars": "759",
    "forks": "47",
    "added_stars": "445 stars this week",
    "avatars": [
      "https://avatars.githubusercontent.com/u/4634056?s=40&v=4"
    ]
  }
  ...
]
}

```

</details>

## Deployment

Deploy to Heroku:  

<a href="https://heroku.com/deploy?template=https://github.com/lissy93/gh-trending-no-cors/tree/master">
<img src="https://camo.githubusercontent.com/6979881d5a96b7b18a057083bb8aeb87ba35fc279452e29034c1e1c49ade0636/68747470733a2f2f7777772e6865726f6b7563646e2e636f6d2f6465706c6f792f627574746f6e2e737667" alt="Deploy to Heroku" />
</a>

Or, Run locally:

- Get the code: `git clone https://github.com/Lissy93/gh-trending-no-cors.git`
- Navigate into directory: `cd gh-trending-no-cors`
- Install dependencies: `pip install -r requirements.txt`
- Start the web server: `python manage.py --port=8080`
- Then open your Postman or your browser, and visit `http://localhost:8080/repo`

## Info

### Contributing

Pull requests are welcome :)

### Dependencies

- [lxml] - Python XML toolkit
- [tornado] - Web framework, developed by FriendFeed
- [ustudio-tornado-cors] - Adds CORS support to Tornado, by @ustudio

### Credits

Full credit to the author of the original repo, @Edgar

### Privacy

See the [Heroku/ Salesforce Privacy Policy](<link_to_the_privacy_policy>) for the hosted instance, and the [GitHub Privacy Statement](<link_to_the_github_privacy_statement>) for the data fetched from the GH API.

## License

This fork is licensed under MIT - © Alicia Sykes 2021
