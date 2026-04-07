## `influxdb:data`

```console
$ docker pull influxdb@sha256:b0f9fc41ed79bc1e206f8f581a38a85ae2ee06c87222e832129cc38e102fc844
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:data` - linux; amd64

```console
$ docker pull influxdb@sha256:d0fb97c811a4a55cacfa0e1603ab572132e6dcd16cdf5aca18ec380703e63481
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.7 MB (115719945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e58ea3b2cbfd3a2cede5003cb817408b9038eec9ddaf29642915ac7cd6e5b0ea`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:46:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:50:06 GMT
ENV INFLUXDB_VERSION=1.12.3-c1.12.3
# Tue, 07 Apr 2026 02:50:06 GMT
ENV INFLUXDB_PR=
# Tue, 07 Apr 2026 02:50:06 GMT
ENV INFLUXDB_PV=1.12.3-c1.12.3
# Tue, 07 Apr 2026 02:50:06 GMT
RUN curl -fsSLO "https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_PV}_amd64.deb.asc"          -fssLO "https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_PV}_amd64.deb" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb-data_${INFLUXDB_PV}_amd64.deb.asc"         "influxdb-data_${INFLUXDB_PV}_amd64.deb" &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         "/influxdb-data_${INFLUXDB_PV}_amd64.deb" &&     rm -r "influxdb-data_${INFLUXDB_PV}_amd64.deb.asc"           "influxdb-data_${INFLUXDB_PV}_amd64.deb"           /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:50:06 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Tue, 07 Apr 2026 02:50:06 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 07 Apr 2026 02:50:06 GMT
VOLUME [/var/lib/influxdb]
# Tue, 07 Apr 2026 02:50:06 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 07 Apr 2026 02:50:06 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Tue, 07 Apr 2026 02:50:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 07 Apr 2026 02:50:06 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:c150dd3f5fc91eabd1818cc30298a4a956782621583cadfd369c4d327584008e`  
		Last Modified: Tue, 07 Apr 2026 00:10:26 GMT  
		Size: 48.5 MB (48488823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2c3414b1d6b49c54c305584faac46aad75c67644cf4f8495e8145206d28e416`  
		Last Modified: Tue, 07 Apr 2026 01:47:02 GMT  
		Size: 24.0 MB (24038269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:248b92cf662fa078f2331dea41d8c060acd1ba70c3f8f661640b7f9893202554`  
		Last Modified: Tue, 07 Apr 2026 02:50:21 GMT  
		Size: 43.2 MB (43191078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9797b5bdc84e61929e6f198dedd24d761e89ac038c26cf62c9963c2442c1ec7e`  
		Last Modified: Tue, 07 Apr 2026 02:50:20 GMT  
		Size: 242.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:728060a77bc5d233aee3141516f37761a975fe796b1cb405c41a2101bac60939`  
		Last Modified: Tue, 07 Apr 2026 02:50:20 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8543c75c9fe2f3c0a0566407aa4109cf61e3c8017dbacb8974df4619d60cfff1`  
		Last Modified: Tue, 07 Apr 2026 02:50:20 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:data` - unknown; unknown

```console
$ docker pull influxdb@sha256:fbb0d727c4dcbc9ba0d27576908bba10c699aabd0b55a44d16acf5157bbc145a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4707287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78b84219c70ee4a6eda1b38ccde2be75010098e97c3ce2243361285ab747b601`

```dockerfile
```

-	Layers:
	-	`sha256:6deb4d5596c535f8164f0c8fc98d26064a7d90af775953056725093d21d43bd7`  
		Last Modified: Tue, 07 Apr 2026 02:50:20 GMT  
		Size: 4.7 MB (4693133 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f4d61c143e04292bb849b4cb1bfb0879fdf3f15d14bb231927ac009c0e937b6a`  
		Last Modified: Tue, 07 Apr 2026 02:50:19 GMT  
		Size: 14.2 KB (14154 bytes)  
		MIME: application/vnd.in-toto+json
