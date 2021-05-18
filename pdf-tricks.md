# PDF Tricks

## Compress pdf

```
gs -sDEVICE=pdfwrite -dCompatibilityLevel=1.4 -dPDFSETTINGS=/ebook \
-dNOPAUSE -dQUIET -dBATCH -sOutputFile=output.pdf input.pdf
```

## Decrypt pdf

```
qpdf --decrypt --password=18138367601 $file --replace-input 
```

## Convert PDF to JPG

```
gs -sDEVICE=pngalpha -o file-%03d.jpg -r144 cover.pdf
```