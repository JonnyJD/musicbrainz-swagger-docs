This is a prototype of a better documentation of the
[MusicBrainz Web Service](http://musicbrainz.org/doc/Development/XML_Web_Service/Version_2).

See also
[MBS-5307](http://tickets.musicbrainz.org/browse/MBS-5307)

The result can currently be seen on
http://mbsandbox.org/~jonnyjd/swagger/

Install
-------

Put the complete archive to a web accessible location.
The location is currently hard-coded in `api-docs.json`.
You can use the provided `Makefile` to change between
locations quickly.

To display the documentation you need an instance of
[swagger-ui](https://github.com/wordnik/swagger-ui),
which can be built with

    git clone https://github.com/wordnik/swagger-ui.git
    npm install
    npm run-script build

The dist folder is static and can be copied to a web accessible location.
You should change the `discoveryUrl` in `dist/index.html`
so it points to your `api-docs.json`.

The documentation and swagger don't need to be on the same server.
However, you might need to set up cross origin resource sharing (CORS)
for this to work.
