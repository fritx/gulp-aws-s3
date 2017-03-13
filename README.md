# AWS S3 plugin for Gulp

## Installation
```bash
$ npm install gulp-aws-s3
```

## Configuration

####Using environment variables
```bash
export AWS_ACCESS_KEY_ID="<value>"
export AWS_SECRET_ACCESS_KEY="<value>"
export AWS_REGION="<value>"
export AWS_BUCKET="<value>"
```

####Using plugin `setup()` method
```javascript
var gulpAwsS3 = require('gulp-aws-s3').setup({
    key    : '<value>',
    secret : '<value>',
    region : '<value>',
    bucket : '<value>'
});
```

####During method execution
```javascript
...
    .pipe(gulpAwsS3.upload({<options>}, {
        key    : '<value>',
        secret : '<value>',
        region : '<value>',
        bucket : '<value>'
    });
...
```

## Api

### gulpAwsS3#upload(options:Object, config:Object)

Upload file to s3

The following options are supported:

* `acl` the canned ACL to apply to the object, defaults to `public-read`.
* `path` s3 base path, defaults to `/`.

Possible values of `acl` include: `private`, `public-read`, `public-read-write`, `authenticated-read`, `bucket-owner-read`, `bucket-owner-full-control`.

## Test
```bash
export AWS_ACCESS_KEY_ID="<value>"
export AWS_SECRET_ACCESS_KEY="<value>"
export AWS_REGION="<value>"
export AWS_BUCKET="<value>"

$ npm test
```

## License

The MIT License
```
Copyright (c) 2017 Stanislaw Glogowski

Permission is hereby granted, free of charge, to any person obtaining
a copy of this software and associated documentation files (the
'Software'), to deal in the Software without restriction, including
without limitation the rights to use, copy, modify, merge, publish,
distribute, sublicense, and/or sell copies of the Software, and to
permit persons to whom the Software is furnished to do so, subject to
the following conditions:

The above copyright notice and this permission notice shall be
included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED 'AS IS', WITHOUT WARRANTY OF ANY KIND,
EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF
MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NON-INFRINGEMENT.
IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY
CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT,
TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE
SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
```
