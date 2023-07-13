# Switch branches

1. Virtual environment

```shell
python -m venv venv
source venv/bin/activate
pip install <name>
pip freeze > requirements.txt
deactivate
```

Alternatively installing packages from requirements.txt

```shell
pip install -r requirements.txt
```

## React FE + Flask BE [tutorial](https://www.youtube.com/watch?v=YW8VG_U-m48&list=WL&index=1)

Notes:

1. Create BE and FE folders

- BE has flask structure
- FE has CRA, run EJECT command `npm run eject` to configure build process

1. Change `appBuild` path in `paths.js` to `'../flask-be/static/react'`
1. in `webpack.config.js`

- remove `static/` prefixes from paths
- in `NEW HTMLWebpackPlugin config:` clause add `filename:'../../templates/index.html',`

1. Passing variables from flask to React through tokens on `window`

2. in package.json add `"homepage": "/static/react",`
3. Run `npm run build`
