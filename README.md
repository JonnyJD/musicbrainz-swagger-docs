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
[swagger-ui](https://github.com/wordnik/swagger-ui):

You can get a copy with:

    git clone https://github.com/wordnik/swagger-ui.git
    npm install

Apply the patches in the `patches` folder of this repository.
This can be done manually or with quilt:

    cp -a ../musicbrainz-swagger-docs/patches .
    quilt push -a

The result needs some building:

    npm run-script build

The now complete `dist` folder is static
and can be copied to a web accessible location.
You should change the `discoveryUrl` in `dist/index.html`
so it points to your `api-docs.json`.

The documentation and swagger don't need to be on the same server.
However, you might need to set up cross origin resource sharing (CORS)
for this to work.


Update
------

On the
[swagger-core wiki](https://github.com/wordnik/swagger-core/wiki/API-Declaration)
there is documentation on how to do the api documentation with swagger.
Please open a pull request here if you have updates or additions.
