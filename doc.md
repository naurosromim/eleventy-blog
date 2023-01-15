## file structure
```md
-- .eleventy.config
-- src
    -- index.file
    -- blog
        -- post 1
        -- blog.json
    -- pages
        -- page 1
        -- page 2
    -- _includes
        -- base.njk
```

## initialize project

`-y` answers all questions yes.

```
npm init -y
```
## install 11ty locally
```
npm install @11ty/eleventy --save-dev
```
`-dev` only for development purpose, not for publishing.

## In package.json
```
"scripts": {
    "start": "eleventy --serve",
    "build": "eleventy"
}
```

## `.eleventy.js`

```javascript
module.exports = function(eleventyConfig){
    eleventyConfig.addPassthroughCopy("./src/static");
    return {
        dir: {
            input: "src",
            output: "public"
        }
    };
}
```

## image linking
```md
/static/blog/cover.jpg
```