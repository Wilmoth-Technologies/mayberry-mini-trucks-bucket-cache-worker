export default {
  async fetch(request) {
    const url = new URL(request.url);
    const bucket = "mayberry-mini-trucks-inventory-images";

    const gcsOrigin = `https://storage.googleapis.com/${bucket}${url.pathname}`;

    return fetch(gcsOrigin, {
      cf: {
        cacheEverything: true,
        cacheTtl: 2592000
      }
    });
  }
};
