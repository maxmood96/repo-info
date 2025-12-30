## `influxdb:meta`

```console
$ docker pull influxdb@sha256:a0f9c61dc18ed8aefd14d5038d3ca12a98c2761518c24728c4d03f92eae05ad5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:meta` - linux; amd64

```console
$ docker pull influxdb@sha256:b8d5353f82e2bcc9fabca62cba9ba7876392cb4c0d264632ad973591fd290736
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.3 MB (91289725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9718ab8f0c96d9df0ca5ccac148026aeffc54aa8d69a6065947040a2c6e8accd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:44:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 01:31:41 GMT
ENV INFLUXDB_VERSION=1.12.2-c1.12.2
# Tue, 30 Dec 2025 01:31:41 GMT
RUN curl -fsSLO "https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc"          -fssLO "https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc"         "influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb" &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         "/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb" &&     rm -r "influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc"           "influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb"           /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 01:31:41 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Tue, 30 Dec 2025 01:31:41 GMT
EXPOSE map[8091/tcp:{}]
# Tue, 30 Dec 2025 01:31:41 GMT
VOLUME [/var/lib/influxdb]
# Tue, 30 Dec 2025 01:31:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 30 Dec 2025 01:31:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Dec 2025 01:31:41 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:32a5bf163bd75109aaa8d446f1570117432475cbb2df3fb6f89dd243bcedd1f3`  
		Last Modified: Mon, 29 Dec 2025 22:26:43 GMT  
		Size: 48.5 MB (48480796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16afb0fdc4694732853f4fbf5125c1dcb35f20cca5bec77a98d73d0d3124f855`  
		Last Modified: Mon, 29 Dec 2025 23:45:17 GMT  
		Size: 24.0 MB (24029344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fac420b8d1add9a518c8be0cadbd02cf2b0d721e683660ab29558b57a53f39e`  
		Last Modified: Tue, 30 Dec 2025 01:31:57 GMT  
		Size: 18.8 MB (18779017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e85d0585009faa68a9368aae4bc84c767729a35826873821dfbc4aa6141e2b5`  
		Last Modified: Tue, 30 Dec 2025 01:31:56 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eefee4201d499772783be5a913f67391bb488eff5f377af4f36a20755a5932a5`  
		Last Modified: Tue, 30 Dec 2025 01:31:56 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:meta` - unknown; unknown

```console
$ docker pull influxdb@sha256:97fd89bcfe95081acf6933a13aba093f1c0e44b2f8d66558881dbf209b861d5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4602907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7dd5fb5e2737dbc4eeaad475dc69ad7263fd7b4e523f9efaa0a340db32911432`

```dockerfile
```

-	Layers:
	-	`sha256:5e1e2fa8558e6841daae3568cdf28ed1410c6d2d55f39e4eae5943032a64bbe7`  
		Last Modified: Tue, 30 Dec 2025 06:21:08 GMT  
		Size: 4.6 MB (4590614 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d7e461b14c9d975dd22648bf2177071baab81c1c357c7d7e280b6ea515e3d3c`  
		Last Modified: Tue, 30 Dec 2025 06:21:09 GMT  
		Size: 12.3 KB (12293 bytes)  
		MIME: application/vnd.in-toto+json
