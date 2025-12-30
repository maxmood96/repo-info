## `influxdb:data`

```console
$ docker pull influxdb@sha256:48c52be245532f368ef410e1116638665b77aa2d32fc6098afa2f188a3adbf52
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:data` - linux; amd64

```console
$ docker pull influxdb@sha256:59ff0c552413774b3d6b385faae73eb305a023eb4185c1b715ddd09f3a28f201
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 MB (114827586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a43cbebfe667441d3f471acc3de4203c13b3e4855e1b47c2d5c1dd5ef03e2eb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:44:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 01:31:18 GMT
ENV INFLUXDB_VERSION=1.12.2-c1.12.2
# Tue, 30 Dec 2025 01:31:18 GMT
RUN curl -fsSLO "https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc"          -fssLO "https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc"         "influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb" &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         "/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb" &&     rm -r "influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc"           "influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb"           /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 01:31:18 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Tue, 30 Dec 2025 01:31:18 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 30 Dec 2025 01:31:18 GMT
VOLUME [/var/lib/influxdb]
# Tue, 30 Dec 2025 01:31:18 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 30 Dec 2025 01:31:18 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Tue, 30 Dec 2025 01:31:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Dec 2025 01:31:18 GMT
CMD ["influxd"]
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
	-	`sha256:5a4703e68bd36f5bcb8b2214bab1bbb6ba374a5c20c043154da748f3361921dd`  
		Last Modified: Tue, 30 Dec 2025 01:31:43 GMT  
		Size: 42.3 MB (42315670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41017fe2f59e61beba6e4c0a2d83b618810945b92af80b28894f51be37d86051`  
		Last Modified: Tue, 30 Dec 2025 01:31:37 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1660405a86b92ee6b29340ec8076f9cc40e0f3ddebc4cb6f55dd2ed21de5ad0a`  
		Last Modified: Tue, 30 Dec 2025 01:31:37 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac8b0220b4de5db27d8578d560c61c069579680553c7bd4de3421fa45cb19ffc`  
		Last Modified: Tue, 30 Dec 2025 01:31:38 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:data` - unknown; unknown

```console
$ docker pull influxdb@sha256:b776b538cdbd99fa57093351c24de79ccc588a9473f49ef51726368cb46f5f6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4699230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:874ed27b2a5144ac9452ccc025be647aca0a231354bd6fef1200ccf51a9954ac`

```dockerfile
```

-	Layers:
	-	`sha256:abd6d9c653d6411a9471bb744ee4b2a895594421861c2e10bb06fa1d1db73ee9`  
		Last Modified: Tue, 30 Dec 2025 06:21:03 GMT  
		Size: 4.7 MB (4685451 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27131ca66cd9a9515bd87afd32c5d0c14dc2e042ccb2120638b47804cd6aeab5`  
		Last Modified: Tue, 30 Dec 2025 06:21:04 GMT  
		Size: 13.8 KB (13779 bytes)  
		MIME: application/vnd.in-toto+json
