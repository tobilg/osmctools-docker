# osmctools-docker
Slim Docker image for using osmctools, based on Debian Stitch.

## Usage

You can have a look at the [Osmctools documentation](https://wiki.openstreetmap.org/wiki/Osmconvert) on how to use Osmconvert itself. 

For example, you can use the Docker image like this to unify two PBF files to a single PBF file:

´´´bash
$ docker run -v $(pwd)/data:/data tobilg/osmctools /bin/sh -c "osmconvert /data/region1.pbf --out-o5m | osmconvert - /data/region2.pbf -o=/data/all.pbf"
´´´ 
