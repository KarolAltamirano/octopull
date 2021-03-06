![octopull logo](https://cloud.githubusercontent.com/assets/6654199/22862692/168e8cb6-f14d-11e6-9dec-500819127c5c.png)

# octopull

**octopull** /ˈɒktəpəs/ *noun*
~~a cephalopod mollusc with eight sucker-bearing arms, a soft sac-like body, strong beak-like jaws, and no internal shell.~~ Your multi repo pull request buddy :) **octopull** your git repos!

## Why?
The microlibs and webcomponents era annd their multi repository nature, introduces
a new complexity for chores and repository updating. After cloning, updating a
travis files for 50 different repos, you'll get the point :P

**octopull** makes updating any set of files to any set of repositories a breeze.


## RDD - README driven development :P

```js
const octopull = require('octopull')

const repos = [
  {
      owner: 'alvaropinot',
      repo: 'test-redesigned-broccoli',
      defaultBranch: 'master',
      platform: 'github',
      token: 'your github api here'
  },
  {
      owner: 'alvaropinot',
      repo: 'test-supreme-bassoon',
      defaultBranch: 'master',
      platform: 'github',
      token: 'your github api here'
  }
]

const options = {
  files: ['foo.yml', 'bar.yml'],
  branch: 'update-foo-and-bar', // autogenerated if blank
  message: 'a cool commit msg', // autogenerated if blank
  // OPTIONAL
  pullRequest: {
    title: 'a cool PR title', // autogenerated if blank
    body: 'a cool PR body', // autogenerated if blank
    // OPTIONAL
    // assignees: ['username1', 'username2']
    // reviewers: ['username3', 'username4']
  }
}

repos.forEach((config) => octopull.commit(config, options))
```

## Example PR's created by *octopull*
* https://github.com/alvaropinot/test-redesigned-broccoli/pull/10
* https://github.com/alvaropinot/test-supreme-bassoon/pull/4

## Develop

### Setup

```sh
git clone https://github.com/alvaropinot/octopull

cd octopull
npm install
```

### Run

```sh
# You will need to use `--harmony-async-await` flag to run async/await code.
node --harmony-async-await lib/index.js
```

## License

MIT - [@alvaropinot](http://twitter.com/alvaropinot) Alvaro Pinot

* CC Logo Octopus by Mark Aventura from the Noun Project
* CC Logo Octopus Tentacles by Iconic from the Noun Project
