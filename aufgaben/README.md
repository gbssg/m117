# Generierung PDF mittels Docker

## Installation Docker

Installation Docker je nach Betriebssystem.

## Generierung PDF über Konsole (WSL2)

```
docker run --rm \
    -v `pwd`:/data \
    -w /data \
    rstropek/pandoc-latex \
    -f markdown \
    --template https://git.lux.education/oliver/md2pdf/raw/branch/master/template/eisvogel.latex \
    -t latex \
-N \
    -o mydoc.pdf \
    --metadata-file=mydoc.yaml \
--toc \
-V lang=de \
    mydoc.md
    
```