# api documentation for  [semver (v5.3.0)](https://github.com/npm/node-semver#readme)  [![npm package](https://img.shields.io/npm/v/npmdoc-semver.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-semver) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-semver.svg)](https://travis-ci.org/npmdoc/node-npmdoc-semver)
#### The semantic version parser used by npm.

[![NPM](https://nodei.co/npm/semver.png?downloads=true)](https://www.npmjs.com/package/semver)

[![apidoc](https://npmdoc.github.io/node-npmdoc-semver/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-semver_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-semver/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-semver/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-semver/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "bin": {
        "semver": "./bin/semver"
    },
    "bugs": {
        "url": "https://github.com/npm/node-semver/issues"
    },
    "dependencies": {},
    "description": "The semantic version parser used by npm.",
    "devDependencies": {
        "tap": "^2.0.0"
    },
    "directories": {},
    "dist": {
        "shasum": "9b2ce5d3de02d17c6012ad326aa6b4d0cf54f94f",
        "tarball": "https://registry.npmjs.org/semver/-/semver-5.3.0.tgz"
    },
    "files": [
        "bin",
        "range.bnf",
        "semver.js"
    ],
    "gitHead": "d21444a0658224b152ce54965d02dbe0856afb84",
    "homepage": "https://github.com/npm/node-semver#readme",
    "license": "ISC",
    "main": "semver.js",
    "maintainers": [
        {
            "name": "isaacs",
            "email": "isaacs@npmjs.com"
        },
        {
            "name": "othiym23",
            "email": "ogd@aoaioxxysz.net"
        }
    ],
    "name": "semver",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git+https://github.com/npm/node-semver.git"
    },
    "scripts": {
        "test": "tap test/*.js"
    },
    "version": "5.3.0"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module semver](#apidoc.module.semver)
1.  [function <span class="apidocSignatureSpan">semver.</span>Comparator (comp, loose)](#apidoc.element.semver.Comparator)
1.  [function <span class="apidocSignatureSpan">semver.</span>Range (range, loose)](#apidoc.element.semver.Range)
1.  [function <span class="apidocSignatureSpan">semver.</span>SemVer (version, loose)](#apidoc.element.semver.SemVer)
1.  [function <span class="apidocSignatureSpan">semver.</span>clean (version, loose)](#apidoc.element.semver.clean)
1.  [function <span class="apidocSignatureSpan">semver.</span>cmp (a, op, b, loose)](#apidoc.element.semver.cmp)
1.  [function <span class="apidocSignatureSpan">semver.</span>compare (a, b, loose)](#apidoc.element.semver.compare)
1.  [function <span class="apidocSignatureSpan">semver.</span>compareIdentifiers (a, b)](#apidoc.element.semver.compareIdentifiers)
1.  [function <span class="apidocSignatureSpan">semver.</span>compareLoose (a, b)](#apidoc.element.semver.compareLoose)
1.  [function <span class="apidocSignatureSpan">semver.</span>diff (version1, version2)](#apidoc.element.semver.diff)
1.  [function <span class="apidocSignatureSpan">semver.</span>eq (a, b, loose)](#apidoc.element.semver.eq)
1.  [function <span class="apidocSignatureSpan">semver.</span>gt (a, b, loose)](#apidoc.element.semver.gt)
1.  [function <span class="apidocSignatureSpan">semver.</span>gte (a, b, loose)](#apidoc.element.semver.gte)
1.  [function <span class="apidocSignatureSpan">semver.</span>gtr (version, range, loose)](#apidoc.element.semver.gtr)
1.  [function <span class="apidocSignatureSpan">semver.</span>inc (version, release, loose, identifier)](#apidoc.element.semver.inc)
1.  [function <span class="apidocSignatureSpan">semver.</span>lt (a, b, loose)](#apidoc.element.semver.lt)
1.  [function <span class="apidocSignatureSpan">semver.</span>lte (a, b, loose)](#apidoc.element.semver.lte)
1.  [function <span class="apidocSignatureSpan">semver.</span>ltr (version, range, loose)](#apidoc.element.semver.ltr)
1.  [function <span class="apidocSignatureSpan">semver.</span>major (a, loose)](#apidoc.element.semver.major)
1.  [function <span class="apidocSignatureSpan">semver.</span>maxSatisfying (versions, range, loose)](#apidoc.element.semver.maxSatisfying)
1.  [function <span class="apidocSignatureSpan">semver.</span>minSatisfying (versions, range, loose)](#apidoc.element.semver.minSatisfying)
1.  [function <span class="apidocSignatureSpan">semver.</span>minor (a, loose)](#apidoc.element.semver.minor)
1.  [function <span class="apidocSignatureSpan">semver.</span>neq (a, b, loose)](#apidoc.element.semver.neq)
1.  [function <span class="apidocSignatureSpan">semver.</span>outside (version, range, hilo, loose)](#apidoc.element.semver.outside)
1.  [function <span class="apidocSignatureSpan">semver.</span>parse (version, loose)](#apidoc.element.semver.parse)
1.  [function <span class="apidocSignatureSpan">semver.</span>patch (a, loose)](#apidoc.element.semver.patch)
1.  [function <span class="apidocSignatureSpan">semver.</span>prerelease (version, loose)](#apidoc.element.semver.prerelease)
1.  [function <span class="apidocSignatureSpan">semver.</span>rcompare (a, b, loose)](#apidoc.element.semver.rcompare)
1.  [function <span class="apidocSignatureSpan">semver.</span>rcompareIdentifiers (a, b)](#apidoc.element.semver.rcompareIdentifiers)
1.  [function <span class="apidocSignatureSpan">semver.</span>rsort (list, loose)](#apidoc.element.semver.rsort)
1.  [function <span class="apidocSignatureSpan">semver.</span>satisfies (version, range, loose)](#apidoc.element.semver.satisfies)
1.  [function <span class="apidocSignatureSpan">semver.</span>sort (list, loose)](#apidoc.element.semver.sort)
1.  [function <span class="apidocSignatureSpan">semver.</span>toComparators (range, loose)](#apidoc.element.semver.toComparators)
1.  [function <span class="apidocSignatureSpan">semver.</span>valid (version, loose)](#apidoc.element.semver.valid)
1.  [function <span class="apidocSignatureSpan">semver.</span>validRange (range, loose)](#apidoc.element.semver.validRange)
1.  object <span class="apidocSignatureSpan">semver.</span>Comparator.prototype
1.  object <span class="apidocSignatureSpan">semver.</span>Range.prototype
1.  object <span class="apidocSignatureSpan">semver.</span>re
1.  object <span class="apidocSignatureSpan">semver.</span>src
1.  string <span class="apidocSignatureSpan">semver.</span>SEMVER_SPEC_VERSION

#### [module semver.Comparator](#apidoc.module.semver.Comparator)
1.  [function <span class="apidocSignatureSpan">semver.</span>Comparator (comp, loose)](#apidoc.element.semver.Comparator.Comparator)

#### [module semver.Comparator.prototype](#apidoc.module.semver.Comparator.prototype)
1.  [function <span class="apidocSignatureSpan">semver.Comparator.prototype.</span>parse (comp)](#apidoc.element.semver.Comparator.prototype.parse)
1.  [function <span class="apidocSignatureSpan">semver.Comparator.prototype.</span>test (version)](#apidoc.element.semver.Comparator.prototype.test)
1.  [function <span class="apidocSignatureSpan">semver.Comparator.prototype.</span>toString ()](#apidoc.element.semver.Comparator.prototype.toString)

#### [module semver.Range](#apidoc.module.semver.Range)
1.  [function <span class="apidocSignatureSpan">semver.</span>Range (range, loose)](#apidoc.element.semver.Range.Range)

#### [module semver.Range.prototype](#apidoc.module.semver.Range.prototype)
1.  [function <span class="apidocSignatureSpan">semver.Range.prototype.</span>format ()](#apidoc.element.semver.Range.prototype.format)
1.  [function <span class="apidocSignatureSpan">semver.Range.prototype.</span>parseRange (range)](#apidoc.element.semver.Range.prototype.parseRange)
1.  [function <span class="apidocSignatureSpan">semver.Range.prototype.</span>test (version)](#apidoc.element.semver.Range.prototype.test)
1.  [function <span class="apidocSignatureSpan">semver.Range.prototype.</span>toString ()](#apidoc.element.semver.Range.prototype.toString)



# <a name="apidoc.module.semver"></a>[module semver](#apidoc.module.semver)

#### <a name="apidoc.element.semver.Comparator"></a>[function <span class="apidocSignatureSpan">semver.</span>Comparator (comp, loose)](#apidoc.element.semver.Comparator)
- description and source-code
```javascript
function Comparator(comp, loose) {
  if (comp instanceof Comparator) {
    if (comp.loose === loose)
      return comp;
    else
      comp = comp.value;
  }

  if (!(this instanceof Comparator))
    return new Comparator(comp, loose);

  debug('comparator', comp, loose);
  this.loose = loose;
  this.parse(comp);

  if (this.semver === ANY)
    this.value = '';
  else
    this.value = this.operator + this.semver.version;

  debug('comp', this);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.semver.Range"></a>[function <span class="apidocSignatureSpan">semver.</span>Range (range, loose)](#apidoc.element.semver.Range)
- description and source-code
```javascript
function Range(range, loose) {
  if ((range instanceof Range) && range.loose === loose)
    return range;

  if (!(this instanceof Range))
    return new Range(range, loose);

  this.loose = loose;

  // First, split based on boolean or ||
  this.raw = range;
  this.set = range.split(/\s*\|\|\s*/).map(function(range) {
    return this.parseRange(range.trim());
  }, this).filter(function(c) {
    // throw out any that are not relevant for whatever reason
    return c.length;
  });

  if (!this.set.length) {
    throw new TypeError('Invalid SemVer Range: ' + range);
  }

  this.format();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.semver.SemVer"></a>[function <span class="apidocSignatureSpan">semver.</span>SemVer (version, loose)](#apidoc.element.semver.SemVer)
- description and source-code
```javascript
function SemVer(version, loose) {
  if (version instanceof SemVer) {
    if (version.loose === loose)
      return version;
    else
      version = version.version;
  } else if (typeof version !== 'string') {
    throw new TypeError('Invalid Version: ' + version);
  }

  if (version.length > MAX_LENGTH)
    throw new TypeError('version is longer than ' + MAX_LENGTH + ' characters')

  if (!(this instanceof SemVer))
    return new SemVer(version, loose);

  debug('SemVer', version, loose);
  this.loose = loose;
  var m = version.trim().match(loose ? re[LOOSE] : re[FULL]);

  if (!m)
    throw new TypeError('Invalid Version: ' + version);

  this.raw = version;

  // these are actually numbers
  this.major = +m[1];
  this.minor = +m[2];
  this.patch = +m[3];

  if (this.major > MAX_SAFE_INTEGER || this.major < 0)
    throw new TypeError('Invalid major version')

  if (this.minor > MAX_SAFE_INTEGER || this.minor < 0)
    throw new TypeError('Invalid minor version')

  if (this.patch > MAX_SAFE_INTEGER || this.patch < 0)
    throw new TypeError('Invalid patch version')

  // numberify any prerelease numeric ids
  if (!m[4])
    this.prerelease = [];
  else
    this.prerelease = m[4].split('.').map(function(id) {
      if (/^[0-9]+$/.test(id)) {
        var num = +id;
        if (num >= 0 && num < MAX_SAFE_INTEGER)
          return num;
      }
      return id;
    });

  this.build = m[5] ? m[5].split('.') : [];
  this.format();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.semver.clean"></a>[function <span class="apidocSignatureSpan">semver.</span>clean (version, loose)](#apidoc.element.semver.clean)
- description and source-code
```javascript
function clean(version, loose) {
  var s = parse(version.trim().replace(/^[=v]+/, ''), loose);
  return s ? s.version : null;
}
```
- example usage
```shell
...

$ npm install semver
$ node
var semver = require('semver')

semver.valid('1.2.3') // '1.2.3'
semver.valid('a.b.c') // null
semver.clean('  =v1.2.3   ') // '1.2.3'
semver.satisfies('1.2.3', '1.x || >=2.5.0 || 5.0.0 - 7.2.3') // true
semver.gt('1.2.3', '9.8.7') // false
semver.lt('1.2.3', '9.8.7') // true

As a command-line utility:

$ semver -h
...
```

#### <a name="apidoc.element.semver.cmp"></a>[function <span class="apidocSignatureSpan">semver.</span>cmp (a, op, b, loose)](#apidoc.element.semver.cmp)
- description and source-code
```javascript
function cmp(a, op, b, loose) {
  var ret;
  switch (op) {
    case '===':
      if (typeof a === 'object') a = a.version;
      if (typeof b === 'object') b = b.version;
      ret = a === b;
      break;
    case '!==':
      if (typeof a === 'object') a = a.version;
      if (typeof b === 'object') b = b.version;
      ret = a !== b;
      break;
    case '': case '=': case '==': ret = eq(a, b, loose); break;
    case '!=': ret = neq(a, b, loose); break;
    case '>': ret = gt(a, b, loose); break;
    case '>=': ret = gte(a, b, loose); break;
    case '<': ret = lt(a, b, loose); break;
    case '<=': ret = lte(a, b, loose); break;
    default: throw new TypeError('Invalid operator: ' + op);
  }
  return ret;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.semver.compare"></a>[function <span class="apidocSignatureSpan">semver.</span>compare (a, b, loose)](#apidoc.element.semver.compare)
- description and source-code
```javascript
function compare(a, b, loose) {
  return new SemVer(a, loose).compare(b);
}
```
- example usage
```shell
...
exports.patch = patch;
function patch(a, loose) {
  return new SemVer(a, loose).patch;
}

exports.compare = compare;
function compare(a, b, loose) {
  return new SemVer(a, loose).compare(b);
}

exports.compareLoose = compareLoose;
function compareLoose(a, b) {
  return compare(a, b, true);
}
...
```

#### <a name="apidoc.element.semver.compareIdentifiers"></a>[function <span class="apidocSignatureSpan">semver.</span>compareIdentifiers (a, b)](#apidoc.element.semver.compareIdentifiers)
- description and source-code
```javascript
function compareIdentifiers(a, b) {
  var anum = numeric.test(a);
  var bnum = numeric.test(b);

  if (anum && bnum) {
    a = +a;
    b = +b;
  }

  return (anum && !bnum) ? -1 :
         (bnum && !anum) ? 1 :
         a < b ? -1 :
         a > b ? 1 :
         0;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.semver.compareLoose"></a>[function <span class="apidocSignatureSpan">semver.</span>compareLoose (a, b)](#apidoc.element.semver.compareLoose)
- description and source-code
```javascript
function compareLoose(a, b) {
  return compare(a, b, true);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.semver.diff"></a>[function <span class="apidocSignatureSpan">semver.</span>diff (version1, version2)](#apidoc.element.semver.diff)
- description and source-code
```javascript
function diff(version1, version2) {
  if (eq(version1, version2)) {
    return null;
  } else {
    var v1 = parse(version1);
    var v2 = parse(version2);
    if (v1.prerelease.length || v2.prerelease.length) {
      for (var key in v1) {
        if (key === 'major' || key === 'minor' || key === 'patch') {
          if (v1[key] !== v2[key]) {
            return 'pre'+key;
          }
        }
      }
      return 'prerelease';
    }
    for (var key in v1) {
      if (key === 'major' || key === 'minor' || key === 'patch') {
        if (v1[key] !== v2[key]) {
          return key;
        }
      }
    }
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.semver.eq"></a>[function <span class="apidocSignatureSpan">semver.</span>eq (a, b, loose)](#apidoc.element.semver.eq)
- description and source-code
```javascript
function eq(a, b, loose) {
  return compare(a, b, loose) === 0;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.semver.gt"></a>[function <span class="apidocSignatureSpan">semver.</span>gt (a, b, loose)](#apidoc.element.semver.gt)
- description and source-code
```javascript
function gt(a, b, loose) {
  return compare(a, b, loose) > 0;
}
```
- example usage
```shell
...
$ node
var semver = require('semver')

semver.valid('1.2.3') // '1.2.3'
semver.valid('a.b.c') // null
semver.clean('  =v1.2.3   ') // '1.2.3'
semver.satisfies('1.2.3', '1.x || >=2.5.0 || 5.0.0 - 7.2.3') // true
semver.gt('1.2.3', '9.8.7') // false
semver.lt('1.2.3', '9.8.7') // true

As a command-line utility:

$ semver -h

SemVer 5.1.0
...
```

#### <a name="apidoc.element.semver.gte"></a>[function <span class="apidocSignatureSpan">semver.</span>gte (a, b, loose)](#apidoc.element.semver.gte)
- description and source-code
```javascript
function gte(a, b, loose) {
  return compare(a, b, loose) >= 0;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.semver.gtr"></a>[function <span class="apidocSignatureSpan">semver.</span>gtr (version, range, loose)](#apidoc.element.semver.gtr)
- description and source-code
```javascript
function gtr(version, range, loose) {
  return outside(version, range, '>', loose);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.semver.inc"></a>[function <span class="apidocSignatureSpan">semver.</span>inc (version, release, loose, identifier)](#apidoc.element.semver.inc)
- description and source-code
```javascript
function inc(version, release, loose, identifier) {
  if (typeof(loose) === 'string') {
    identifier = loose;
    loose = undefined;
  }

  try {
    return new SemVer(version, loose).inc(release, identifier).version;
  } catch (er) {
    return null;
  }
}
```
- example usage
```shell
...

#### Prerelease Identifiers

The method '.inc' takes an additional 'identifier' string argument that
will append the value of the string as a prerelease identifier:

'''javascript
> semver.inc('1.2.3', 'prerelease', 'beta')
'1.2.4-beta.0'
'''

command-line example:

'''shell
$ semver 1.2.3 -i prerelease --preid beta
...
```

#### <a name="apidoc.element.semver.lt"></a>[function <span class="apidocSignatureSpan">semver.</span>lt (a, b, loose)](#apidoc.element.semver.lt)
- description and source-code
```javascript
function lt(a, b, loose) {
  return compare(a, b, loose) < 0;
}
```
- example usage
```shell
...
var semver = require('semver')

semver.valid('1.2.3') // '1.2.3'
semver.valid('a.b.c') // null
semver.clean('  =v1.2.3   ') // '1.2.3'
semver.satisfies('1.2.3', '1.x || >=2.5.0 || 5.0.0 - 7.2.3') // true
semver.gt('1.2.3', '9.8.7') // false
semver.lt('1.2.3', '9.8.7') // true

As a command-line utility:

$ semver -h

SemVer 5.1.0
...
```

#### <a name="apidoc.element.semver.lte"></a>[function <span class="apidocSignatureSpan">semver.</span>lte (a, b, loose)](#apidoc.element.semver.lte)
- description and source-code
```javascript
function lte(a, b, loose) {
  return compare(a, b, loose) <= 0;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.semver.ltr"></a>[function <span class="apidocSignatureSpan">semver.</span>ltr (version, range, loose)](#apidoc.element.semver.ltr)
- description and source-code
```javascript
function ltr(version, range, loose) {
  return outside(version, range, '<', loose);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.semver.major"></a>[function <span class="apidocSignatureSpan">semver.</span>major (a, loose)](#apidoc.element.semver.major)
- description and source-code
```javascript
function major(a, loose) {
  return new SemVer(a, loose).major;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.semver.maxSatisfying"></a>[function <span class="apidocSignatureSpan">semver.</span>maxSatisfying (versions, range, loose)](#apidoc.element.semver.maxSatisfying)
- description and source-code
```javascript
function maxSatisfying(versions, range, loose) {
  return versions.filter(function(version) {
    return satisfies(version, range, loose);
  }).sort(function(a, b) {
    return rcompare(a, b, loose);
  })[0] || null;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.semver.minSatisfying"></a>[function <span class="apidocSignatureSpan">semver.</span>minSatisfying (versions, range, loose)](#apidoc.element.semver.minSatisfying)
- description and source-code
```javascript
function minSatisfying(versions, range, loose) {
  return versions.filter(function(version) {
    return satisfies(version, range, loose);
  }).sort(function(a, b) {
    return compare(a, b, loose);
  })[0] || null;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.semver.minor"></a>[function <span class="apidocSignatureSpan">semver.</span>minor (a, loose)](#apidoc.element.semver.minor)
- description and source-code
```javascript
function minor(a, loose) {
  return new SemVer(a, loose).minor;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.semver.neq"></a>[function <span class="apidocSignatureSpan">semver.</span>neq (a, b, loose)](#apidoc.element.semver.neq)
- description and source-code
```javascript
function neq(a, b, loose) {
  return compare(a, b, loose) !== 0;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.semver.outside"></a>[function <span class="apidocSignatureSpan">semver.</span>outside (version, range, hilo, loose)](#apidoc.element.semver.outside)
- description and source-code
```javascript
function outside(version, range, hilo, loose) {
  version = new SemVer(version, loose);
  range = new Range(range, loose);

  var gtfn, ltefn, ltfn, comp, ecomp;
  switch (hilo) {
    case '>':
      gtfn = gt;
      ltefn = lte;
      ltfn = lt;
      comp = '>';
      ecomp = '>=';
      break;
    case '<':
      gtfn = lt;
      ltefn = gte;
      ltfn = gt;
      comp = '<';
      ecomp = '<=';
      break;
    default:
      throw new TypeError('Must provide a hilo val of "<" or ">"');
  }

  // If it satisifes the range it is not outside
  if (satisfies(version, range, loose)) {
    return false;
  }

  // From now on, variable terms are as if we're in "gtr" mode.
  // but note that everything is flipped for the "ltr" function.

  for (var i = 0; i < range.set.length; ++i) {
    var comparators = range.set[i];

    var high = null;
    var low = null;

    comparators.forEach(function(comparator) {
      if (comparator.semver === ANY) {
        comparator = new Comparator('>=0.0.0')
      }
      high = high || comparator;
      low = low || comparator;
      if (gtfn(comparator.semver, high.semver, loose)) {
        high = comparator;
      } else if (ltfn(comparator.semver, low.semver, loose)) {
        low = comparator;
      }
    });

    // If the edge version comparator has a operator then our version
    // isn't outside it
    if (high.operator === comp || high.operator === ecomp) {
      return false;
    }

    // If the lowest version comparator has an operator and our version
    // is less than it then it isn't higher than the range
    if ((!low.operator || low.operator === comp) &&
        ltefn(version, low.semver)) {
      return false;
    } else if (low.operator === ecomp && ltfn(version, low.semver)) {
      return false;
    }
  }
  return true;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.semver.parse"></a>[function <span class="apidocSignatureSpan">semver.</span>parse (version, loose)](#apidoc.element.semver.parse)
- description and source-code
```javascript
function parse(version, loose) {
  if (version instanceof SemVer)
    return version;

  if (typeof version !== 'string')
    return null;

  if (version.length > MAX_LENGTH)
    return null;

  var r = loose ? re[LOOSE] : re[FULL];
  if (!r.test(version))
    return null;

  try {
    return new SemVer(version, loose);
  } catch (er) {
    return null;
  }
}
```
- example usage
```shell
...
}

if (!(this instanceof Comparator))
  return new Comparator(comp, loose);

debug('comparator', comp, loose);
this.loose = loose;
this.parse(comp);

if (this.semver === ANY)
  this.value = '';
else
  this.value = this.operator + this.semver.version;

debug('comp', this);
...
```

#### <a name="apidoc.element.semver.patch"></a>[function <span class="apidocSignatureSpan">semver.</span>patch (a, loose)](#apidoc.element.semver.patch)
- description and source-code
```javascript
function patch(a, loose) {
  return new SemVer(a, loose).patch;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.semver.prerelease"></a>[function <span class="apidocSignatureSpan">semver.</span>prerelease (version, loose)](#apidoc.element.semver.prerelease)
- description and source-code
```javascript
function prerelease(version, loose) {
  var parsed = parse(version, loose);
  return (parsed && parsed.prerelease.length) ? parsed.prerelease : null;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.semver.rcompare"></a>[function <span class="apidocSignatureSpan">semver.</span>rcompare (a, b, loose)](#apidoc.element.semver.rcompare)
- description and source-code
```javascript
function rcompare(a, b, loose) {
  return compare(b, a, loose);
}
```
- example usage
```shell
...
    return exports.compare(a, b, loose);
  });
}

exports.rsort = rsort;
function rsort(list, loose) {
  return list.sort(function(a, b) {
    return exports.rcompare(a, b, loose);
  });
}

exports.gt = gt;
function gt(a, b, loose) {
  return compare(a, b, loose) > 0;
}
...
```

#### <a name="apidoc.element.semver.rcompareIdentifiers"></a>[function <span class="apidocSignatureSpan">semver.</span>rcompareIdentifiers (a, b)](#apidoc.element.semver.rcompareIdentifiers)
- description and source-code
```javascript
function rcompareIdentifiers(a, b) {
  return compareIdentifiers(b, a);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.semver.rsort"></a>[function <span class="apidocSignatureSpan">semver.</span>rsort (list, loose)](#apidoc.element.semver.rsort)
- description and source-code
```javascript
function rsort(list, loose) {
  return list.sort(function(a, b) {
    return exports.rcompare(a, b, loose);
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.semver.satisfies"></a>[function <span class="apidocSignatureSpan">semver.</span>satisfies (version, range, loose)](#apidoc.element.semver.satisfies)
- description and source-code
```javascript
function satisfies(version, range, loose) {
  try {
    range = new Range(range, loose);
  } catch (er) {
    return false;
  }
  return range.test(version);
}
```
- example usage
```shell
...
$ npm install semver
$ node
var semver = require('semver')

semver.valid('1.2.3') // '1.2.3'
semver.valid('a.b.c') // null
semver.clean('  =v1.2.3   ') // '1.2.3'
semver.satisfies('1.2.3', '1.x || >=2.5.0 || 5.0.0 - 7.2.3') // true
semver.gt('1.2.3', '9.8.7') // false
semver.lt('1.2.3', '9.8.7') // true

As a command-line utility:

$ semver -h
...
```

#### <a name="apidoc.element.semver.sort"></a>[function <span class="apidocSignatureSpan">semver.</span>sort (list, loose)](#apidoc.element.semver.sort)
- description and source-code
```javascript
function sort(list, loose) {
  return list.sort(function(a, b) {
    return exports.compare(a, b, loose);
  });
}
```
- example usage
```shell
...
compare strings.
* 'neq(v1, v2)': 'v1 != v2' The opposite of 'eq'.
* 'cmp(v1, comparator, v2)': Pass in a comparison string, and it'll call
the corresponding function above.  '"==="' and '"!=="' do simple
string comparison, but are included for completeness.  Throws if an
invalid comparison string is provided.
* 'compare(v1, v2)': Return '0' if 'v1 == v2', or '1' if 'v1' is greater, or '-1' if
'v2' is greater.  Sorts in ascending order if passed to 'Array.sort()'.
* 'rcompare(v1, v2)': The reverse of compare.  Sorts an array of versions
in descending order when passed to 'Array.sort()'.
* 'diff(v1, v2)': Returns difference between two versions by the release type
('major', 'premajor', 'minor', 'preminor', 'patch', 'prepatch', or 'prerelease'),
or null if the versions are the same.
...
```

#### <a name="apidoc.element.semver.toComparators"></a>[function <span class="apidocSignatureSpan">semver.</span>toComparators (range, loose)](#apidoc.element.semver.toComparators)
- description and source-code
```javascript
function toComparators(range, loose) {
  return new Range(range, loose).set.map(function(comp) {
    return comp.map(function(c) {
      return c.value;
    }).join(' ').trim().split(' ');
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.semver.valid"></a>[function <span class="apidocSignatureSpan">semver.</span>valid (version, loose)](#apidoc.element.semver.valid)
- description and source-code
```javascript
function valid(version, loose) {
  var v = parse(version, loose);
  return v ? v.version : null;
}
```
- example usage
```shell
...

## Usage

    $ npm install semver
    $ node
    var semver = require('semver')

    semver.valid('1.2.3') // '1.2.3'
    semver.valid('a.b.c') // null
    semver.clean('  =v1.2.3   ') // '1.2.3'
    semver.satisfies('1.2.3', '1.x || >=2.5.0 || 5.0.0 - 7.2.3') // true
    semver.gt('1.2.3', '9.8.7') // false
    semver.lt('1.2.3', '9.8.7') // true

As a command-line utility:
...
```

#### <a name="apidoc.element.semver.validRange"></a>[function <span class="apidocSignatureSpan">semver.</span>validRange (range, loose)](#apidoc.element.semver.validRange)
- description and source-code
```javascript
function validRange(range, loose) {
  try {
    // Return '*' instead of '' so that truthiness works.
    // This will throw if it's invalid anyway
    return new Range(range, loose).range || '*';
  } catch (er) {
    return null;
  }
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.semver.Comparator"></a>[module semver.Comparator](#apidoc.module.semver.Comparator)

#### <a name="apidoc.element.semver.Comparator.Comparator"></a>[function <span class="apidocSignatureSpan">semver.</span>Comparator (comp, loose)](#apidoc.element.semver.Comparator.Comparator)
- description and source-code
```javascript
function Comparator(comp, loose) {
  if (comp instanceof Comparator) {
    if (comp.loose === loose)
      return comp;
    else
      comp = comp.value;
  }

  if (!(this instanceof Comparator))
    return new Comparator(comp, loose);

  debug('comparator', comp, loose);
  this.loose = loose;
  this.parse(comp);

  if (this.semver === ANY)
    this.value = '';
  else
    this.value = this.operator + this.semver.version;

  debug('comp', this);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.semver.Comparator.prototype"></a>[module semver.Comparator.prototype](#apidoc.module.semver.Comparator.prototype)

#### <a name="apidoc.element.semver.Comparator.prototype.parse"></a>[function <span class="apidocSignatureSpan">semver.Comparator.prototype.</span>parse (comp)](#apidoc.element.semver.Comparator.prototype.parse)
- description and source-code
```javascript
parse = function (comp) {
  var r = this.loose ? re[COMPARATORLOOSE] : re[COMPARATOR];
  var m = comp.match(r);

  if (!m)
    throw new TypeError('Invalid comparator: ' + comp);

  this.operator = m[1];
  if (this.operator === '=')
    this.operator = '';

  // if it literally is just '>' or '' then allow anything.
  if (!m[2])
    this.semver = ANY;
  else
    this.semver = new SemVer(m[2], this.loose);
}
```
- example usage
```shell
...
}

if (!(this instanceof Comparator))
  return new Comparator(comp, loose);

debug('comparator', comp, loose);
this.loose = loose;
this.parse(comp);

if (this.semver === ANY)
  this.value = '';
else
  this.value = this.operator + this.semver.version;

debug('comp', this);
...
```

#### <a name="apidoc.element.semver.Comparator.prototype.test"></a>[function <span class="apidocSignatureSpan">semver.Comparator.prototype.</span>test (version)](#apidoc.element.semver.Comparator.prototype.test)
- description and source-code
```javascript
test = function (version) {
  debug('Comparator.test', version, this.loose);

  if (this.semver === ANY)
    return true;

  if (typeof version === 'string')
    version = new SemVer(version, this.loose);

  return cmp(version, this.operator, this.semver, this.loose);
}
```
- example usage
```shell
...
exports = module.exports = SemVer;

// The debug function is excluded entirely from the minified version.
/* nomin */ var debug;
/* nomin */ if (typeof process === 'object' &&
  /* nomin */ process.env &&
  /* nomin */ process.env.NODE_DEBUG &&
  /* nomin */ /\bsemver\b/i.test(process.env.NODE_DEBUG))
/* nomin */ debug = function() {
  /* nomin */ var args = Array.prototype.slice.call(arguments, 0);
  /* nomin */ args.unshift('SEMVER');
  /* nomin */ console.log.apply(console, args);
  /* nomin */ };
/* nomin */ else
/* nomin */ debug = function() {};
...
```

#### <a name="apidoc.element.semver.Comparator.prototype.toString"></a>[function <span class="apidocSignatureSpan">semver.Comparator.prototype.</span>toString ()](#apidoc.element.semver.Comparator.prototype.toString)
- description and source-code
```javascript
toString = function () {
  return this.value;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.semver.Range"></a>[module semver.Range](#apidoc.module.semver.Range)

#### <a name="apidoc.element.semver.Range.Range"></a>[function <span class="apidocSignatureSpan">semver.</span>Range (range, loose)](#apidoc.element.semver.Range.Range)
- description and source-code
```javascript
function Range(range, loose) {
  if ((range instanceof Range) && range.loose === loose)
    return range;

  if (!(this instanceof Range))
    return new Range(range, loose);

  this.loose = loose;

  // First, split based on boolean or ||
  this.raw = range;
  this.set = range.split(/\s*\|\|\s*/).map(function(range) {
    return this.parseRange(range.trim());
  }, this).filter(function(c) {
    // throw out any that are not relevant for whatever reason
    return c.length;
  });

  if (!this.set.length) {
    throw new TypeError('Invalid SemVer Range: ' + range);
  }

  this.format();
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.semver.Range.prototype"></a>[module semver.Range.prototype](#apidoc.module.semver.Range.prototype)

#### <a name="apidoc.element.semver.Range.prototype.format"></a>[function <span class="apidocSignatureSpan">semver.Range.prototype.</span>format ()](#apidoc.element.semver.Range.prototype.format)
- description and source-code
```javascript
format = function () {
  this.range = this.set.map(function(comps) {
    return comps.join(' ').trim();
  }).join('||').trim();
  return this.range;
}
```
- example usage
```shell
...
      if (num >= 0 && num < MAX_SAFE_INTEGER)
        return num;
    }
    return id;
  });

this.build = m[5] ? m[5].split('.') : [];
this.format();
}

SemVer.prototype.format = function() {
this.version = this.major + '.' + this.minor + '.' + this.patch;
if (this.prerelease.length)
  this.version += '-' + this.prerelease.join('.');
return this.version;
...
```

#### <a name="apidoc.element.semver.Range.prototype.parseRange"></a>[function <span class="apidocSignatureSpan">semver.Range.prototype.</span>parseRange (range)](#apidoc.element.semver.Range.prototype.parseRange)
- description and source-code
```javascript
parseRange = function (range) {
  var loose = this.loose;
  range = range.trim();
  debug('range', range, loose);
  // '1.2.3 - 1.2.4' => '>=1.2.3 <=1.2.4'
  var hr = loose ? re[HYPHENRANGELOOSE] : re[HYPHENRANGE];
  range = range.replace(hr, hyphenReplace);
  debug('hyphen replace', range);
  // '> 1.2.3 < 1.2.5' => '>1.2.3 <1.2.5'
  range = range.replace(re[COMPARATORTRIM], comparatorTrimReplace);
  debug('comparator trim', range, re[COMPARATORTRIM]);

  // '~ 1.2.3' => '~1.2.3'
  range = range.replace(re[TILDETRIM], tildeTrimReplace);

  // '^ 1.2.3' => '^1.2.3'
  range = range.replace(re[CARETTRIM], caretTrimReplace);

  // normalize spaces
  range = range.split(/\s+/).join(' ');

  // At this point, the range is completely trimmed and
  // ready to be split into comparators.

  var compRe = loose ? re[COMPARATORLOOSE] : re[COMPARATOR];
  var set = range.split(' ').map(function(comp) {
    return parseComparator(comp, loose);
  }).join(' ').split(/\s+/);
  if (this.loose) {
    // in loose mode, throw out any that are not valid comparators
    set = set.filter(function(comp) {
      return !!comp.match(compRe);
    });
  }
  set = set.map(function(comp) {
    return new Comparator(comp, loose);
  });

  return set;
}
```
- example usage
```shell
...
  return new Range(range, loose);

this.loose = loose;

// First, split based on boolean or ||
this.raw = range;
this.set = range.split(/\s*\|\|\s*/).map(function(range) {
  return this.parseRange(range.trim());
}, this).filter(function(c) {
  // throw out any that are not relevant for whatever reason
  return c.length;
});

if (!this.set.length) {
  throw new TypeError('Invalid SemVer Range: ' + range);
...
```

#### <a name="apidoc.element.semver.Range.prototype.test"></a>[function <span class="apidocSignatureSpan">semver.Range.prototype.</span>test (version)](#apidoc.element.semver.Range.prototype.test)
- description and source-code
```javascript
test = function (version) {
  if (!version)
    return false;

  if (typeof version === 'string')
    version = new SemVer(version, this.loose);

  for (var i = 0; i < this.set.length; i++) {
    if (testSet(this.set[i], version))
      return true;
  }
  return false;
}
```
- example usage
```shell
...
exports = module.exports = SemVer;

// The debug function is excluded entirely from the minified version.
/* nomin */ var debug;
/* nomin */ if (typeof process === 'object' &&
  /* nomin */ process.env &&
  /* nomin */ process.env.NODE_DEBUG &&
  /* nomin */ /\bsemver\b/i.test(process.env.NODE_DEBUG))
/* nomin */ debug = function() {
  /* nomin */ var args = Array.prototype.slice.call(arguments, 0);
  /* nomin */ args.unshift('SEMVER');
  /* nomin */ console.log.apply(console, args);
  /* nomin */ };
/* nomin */ else
/* nomin */ debug = function() {};
...
```

#### <a name="apidoc.element.semver.Range.prototype.toString"></a>[function <span class="apidocSignatureSpan">semver.Range.prototype.</span>toString ()](#apidoc.element.semver.Range.prototype.toString)
- description and source-code
```javascript
toString = function () {
  return this.range;
}
```
- example usage
```shell
n/a
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
