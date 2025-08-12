# mkqr

A command line tool for generating QR codes for the <https://nearme.lml.live>
website.

## Dependencies

The tool is built in Ruby, therefore Ruby and Bundler are required. ImageMagick
is used to put the images together. You can find installation instructions for
your OS [here](https://imagemagick.org/script/download.php).

## Usage

The tool is designed to create QR codes to be used with the
<https://nearme.lml.live> website. The source code for that website is
contained in [this
repository](https://github.com/livemusiclocator/nearme.lml.live). You can
consult the `README` there for more details on the meaning of the URLs you can
generate with this tool.

To generate a QR code based on a latitude and longitude, you can run this
command.

```
mkqr --lat=-37.7986116 --lng=144.9804752 --name='the Night Cat'
```

To generate a QR code based on a GUID you can run this command.

```
mkqr --guid=f0d2ba76-8a51-4d9d-8276-d175f3992f1c --name='the Night Cat'
```

Note that the GUID in this example corresponds to an actual GUID on the website
so you can test it out.

To clean up generated files, run `mkqr --clean`. To see all other command line
options, run `mkqr --help`.
