# COG DEMO

This example will walk through the process of creating a Cloud Optimized Geotiff, loading it onto a web server, and rendering it on the web and in a desktop GIS.

### 1. Create a cloud optimized geotiff using rio-cogeo

Following along with the instructions here: <https://cogeotiff.github.io/rio-cogeo/Is_it_a_COG/>

a. inspect the data

```bash
rio cogeo info duluth2011_3in_dt.tif
```

No internal tiling, so it's not a COG.

b. create the COG

```bash
rio cogeo create duluth2011_3in_dt.tif duluth2011_3in_dt_COG.tif
```

c. confirm that it worked

```bash
rio cogeo info duluth2011_3in_dt_COG.tif
```

Should see something like

```bash
...
Tiled:      True
...

IFD
Block 1
Block 2
...
```

### 2. Create web server with COG in tow

In this step, you will start up an Apache web server as a docker container. If you don't have Docker or don't want to fiddle with it, I believe there are free (or low-cost) tiers available for loading the data into AWS s3 bucket or a Google Object Store.

Windows CMD line:

```cmd
docker run -d --name my-cog-server -p 8080:80 -v %cd%/examples/data:/usr/local/apache2/htdocs/ -v "%cd%/examples/server/httpd.conf":/usr/local/apache2/conf/httpd.conf httpd:2.4
```

Bash (Mac or Linux):

```bash
docker run -d --name my-cog-server -p 8080:80 -v "$(pwd)/examples/data":/usr/local/apache2/htdocs/ -v "$(pwd)/examples/server/httpd.conf":/usr/local/apache2/conf/httpd.conf httpd:2.4
```

To see if this worked, checkout <http://localhost:8080>  
You should see your COG listed.

### 3. Load COG into a web map

### 4. Load COG into a desktop GIS (QGIS or ArcGIS Pro)
