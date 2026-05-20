## `influxdb:data`

```console
$ docker pull influxdb@sha256:9319bb876d60b6611d7314e40ced0a9093badec94380fd788d26fd2ae2258e7f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:data` - linux; amd64

```console
$ docker pull influxdb@sha256:579ca334f033a171c682d34b1c340d2fe8880c3dea2edb1b861f32cbd8a4ab9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.7 MB (115730454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7c666f3a65cbb37594d2787f9802d5d13604d24770dd4ac72f6ff5254ed4f02`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:23:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 00:29:41 GMT
ENV INFLUXDB_VERSION=1.12.4-c1.12.4
# Wed, 20 May 2026 00:29:41 GMT
ENV INFLUXDB_PR=
# Wed, 20 May 2026 00:29:41 GMT
ENV INFLUXDB_PV=1.12.4-c1.12.4
# Wed, 20 May 2026 00:29:41 GMT
RUN curl -fsSLO "https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_PV}_amd64.deb.asc"          -fsSLO "https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_PV}_amd64.deb" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb-data_${INFLUXDB_PV}_amd64.deb.asc"         "influxdb-data_${INFLUXDB_PV}_amd64.deb" &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         "/influxdb-data_${INFLUXDB_PV}_amd64.deb" &&     rm -r "influxdb-data_${INFLUXDB_PV}_amd64.deb.asc"           "influxdb-data_${INFLUXDB_PV}_amd64.deb"           /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 00:29:41 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Wed, 20 May 2026 00:29:41 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 20 May 2026 00:29:41 GMT
VOLUME [/var/lib/influxdb]
# Wed, 20 May 2026 00:29:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 20 May 2026 00:29:41 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Wed, 20 May 2026 00:29:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 20 May 2026 00:29:41 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:4887723d153cfd7fd9e356c8730311c36a64e4f9329f9d3ae1929e05715f2e73`  
		Last Modified: Tue, 19 May 2026 22:36:12 GMT  
		Size: 48.5 MB (48495432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e51c50554dce9c9549d76c40bfea45780a8342aea81ba8b270ba1bf46a2aec5`  
		Last Modified: Tue, 19 May 2026 23:23:20 GMT  
		Size: 24.0 MB (24043374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:122828ed9828493a392d3bbd9540521410cf9cf21e14801d4368427ab3cd94b3`  
		Last Modified: Wed, 20 May 2026 00:29:55 GMT  
		Size: 43.2 MB (43189878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6de91331488774fe9e2d09549cd5a5d1e4d157b3accfc4f111eb66f7e8a78ec4`  
		Last Modified: Wed, 20 May 2026 00:29:54 GMT  
		Size: 242.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c650389a0929f427ce6e58d1ef4b9e97645e7409a49c8eae0691bb95ccf3d10`  
		Last Modified: Wed, 20 May 2026 00:29:54 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1f5de10629d35972965ab74df4e979631016090bf6e698d40b7bfb3c9399125`  
		Last Modified: Wed, 20 May 2026 00:29:54 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:data` - unknown; unknown

```console
$ docker pull influxdb@sha256:c0e349314838ec27086c03fedc8033ce30c3a691cfe1c4bb0d22ee06c43435d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4707295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb1fc2a0bec89acfd2cad38c8f018acc50a6fd978d2be2f8502e23fecf642dab`

```dockerfile
```

-	Layers:
	-	`sha256:5493b0b0c59fe03e660e43bf5164927cb17f7eaa8fb42fa6778eb7409226336c`  
		Last Modified: Wed, 20 May 2026 00:29:54 GMT  
		Size: 4.7 MB (4693141 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d3c95869539703cb6ec78b80a3a4fe4b11f4db2ccdf8b38cb792807c5a67dbe2`  
		Last Modified: Wed, 20 May 2026 00:29:54 GMT  
		Size: 14.2 KB (14154 bytes)  
		MIME: application/vnd.in-toto+json
