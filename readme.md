# Stream to ETag

Calculates Etag/S3 MD5 sum given a readable stream. Uses the same algorithm that S3 uses to calculate the `ETag`.

This is especially useful for verifying large files uploaded using multipart S3 API, enabling use of `createReadStream` to keep memory usage low.

## Installation

```sh
npm install stream-to-etag
```

## Usage

```js
    const etag = await stream2etag(createReadStream(file));
```

Thanks to [this post](https://stackoverflow.com/questions/12186993/what-is-the-algorithm-to-compute-the-amazon-s3-etag-for-a-file-larger-than-5gb#answer-19896823) for helping me figure out the details ;)
