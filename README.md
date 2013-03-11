# puid - primary unique id
Generate an unique ID depends on time, machine and process for use in distributed environment.

Each unique ID has 4 sections which are:

  - timestamp:    'he5fps6l'  // Timestamp in microseconds
  - machineId:    '2504cd'    // the first external device, md5 to the address (IPv4/IPv6)
  - processId:    '1w3a'      // pid
  - counter:      'g8ut8e'    // high-resolution real time; nanoseconds

All values are converted to base36

## Installation

```
$ npm install puid
```

## Running unit tests

```
$ npm test
```

## Usage

```javascript
    var puid = require('puid');
    console.log(puid.generate());
    console.log(puid.generate());

    // Output:
    // he5gawzw2504cd1w6x83z1kr
    // he5gawzw2504cd1w6x83ziw1
```

## License

[MIT](LICENSE)