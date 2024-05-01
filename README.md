# @devtea2027/laborum-dolor-doloribus-et

![NPM](https://img.shields.io/npm/l/@devtea2027/laborum-dolor-doloribus-et?color=blue&style=flat-square) ![npm](https://img.shields.io/npm/v/@devtea2027/laborum-dolor-doloribus-et?color=blue&style=flat-square)

The `@devtea2027/laborum-dolor-doloribus-et` is a tiny library that could convert file to arraybuffer, dataUrl and text

## Intall

```shell
npm i @devtea2027/laborum-dolor-doloribus-et -S
```

or

```shell
pnpm add @devtea2027/laborum-dolor-doloribus-et -S
```

## Useage

Here is a simple [demo](https://react-ts-dsbxwk.stackblitz.io).

```javascript
import { toAny } from "@devtea2027/laborum-dolor-doloribus-et";

// You can get file by input tag with type that is file
toAny(file, "arrayBuffer").then((value) => {
  console.log(value); // value is a arrayBuffer
});
```

## API

### toAny

The all-purpose api to convert file to others.

- Params
  - `file` **Blob | File** The file to convert.
  - `options` **"arrayBuffer" | "dataUrl" | "objectUrl" | "text" | object**
    - `options.type` **"arrayBuffer" | "dataUrl" | "objectUrl" | | "text"**
    - `options.encoding` **"string" | undefined** _Only used for "text"_
- Returns
  - `Promise<any>` Returns the associated result according to the specified parameter.

### toBinaryString

Convert file to binaryString.

- Params
  - `file` **Blob | File** The file to convert.
  - Returns
    - `Promise<string>` Returns a binaryString.

### toArrayBuffer

Convert file to [arrayBuffer](https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/ArrayBuffer).

- Params
  - `file` **Blob | File** The file to convert.
  - Returns
    - `Promise<ArrayBuffer>` Returns a arrayBuffer.

### toDataUrl

Convert file to [dataUrl](https://developer.mozilla.org/zh-CN/docs/Web/HTTP/Basics_of_HTTP/Data_URLs).

- Params
  - `file` **Blob | File** The file to convert.
  - Returns
    - `Promise<string>` Returns a dataUrl.

### toObjectUrl

Convert file to [objectUrl](https://developer.mozilla.org/en-US/docs/Web/API/URL/createObjectURL_static).

- Params
  - `file` **Blob | File** The file to convert.
  - Returns
    - `Promise<string>` Returns a objectUrl.

### toText

Convert file to string.

- Params
  - `file` **Blob | File** The file to convert.
  - `encoding` **"string" | undefined** Encoding type.
  - Returns
    - `Promise<string>` Returns a string.
