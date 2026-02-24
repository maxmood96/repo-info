## `influxdb:data`

```console
$ docker pull influxdb@sha256:40a5c206b6f380abae88b69ae0524895c1c2e942dba023a469101f76d2af1d31
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:data` - linux; amd64

```console
$ docker pull influxdb@sha256:155b636700f0303800c702d9a5399d444553918463a71d7c03e3001e694fbcd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 MB (114848805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ae63172d05356fc4dd7607ef82abc295d6b12d9e8cb06daa68c35b0aa3508b8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:18:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 20:07:58 GMT
ENV INFLUXDB_VERSION=1.12.2-c1.12.2
# Tue, 24 Feb 2026 20:07:58 GMT
RUN curl -fsSLO "https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc"          -fssLO "https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc"         "influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb" &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         "/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb" &&     rm -r "influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc"           "influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb"           /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 20:07:58 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Tue, 24 Feb 2026 20:07:58 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 24 Feb 2026 20:07:58 GMT
VOLUME [/var/lib/influxdb]
# Tue, 24 Feb 2026 20:07:58 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 24 Feb 2026 20:07:58 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Tue, 24 Feb 2026 20:07:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 24 Feb 2026 20:07:58 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:6a7e0620566c7dfbe5d3c9a7601d116556ec17a021b3e824f8ab09d12b0c25c6`  
		Last Modified: Tue, 24 Feb 2026 18:42:43 GMT  
		Size: 48.5 MB (48488777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aab3b37e4807fe48145826511e16a527bbc4695222ceb966669a4d16729b3b94`  
		Last Modified: Tue, 24 Feb 2026 19:18:52 GMT  
		Size: 24.0 MB (24038450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:097b775cb2b27f1be92722003efb2fdb5d4197757a50a9b95ab6a93b00497d0f`  
		Last Modified: Tue, 24 Feb 2026 20:08:11 GMT  
		Size: 42.3 MB (42319802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6f444d666081f71dfd818ed6196fe39d16150c4af02efe1c5aee1553ea30b91`  
		Last Modified: Tue, 24 Feb 2026 20:08:09 GMT  
		Size: 242.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2740311728c56c143f1b5aba87ff0fc892e297fb301843e933c9bbf4deff525f`  
		Last Modified: Tue, 24 Feb 2026 20:08:10 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:481ed7b20e0cef23ddc82013da6afb2579b45cf2c248e33227067fc6fe65ead0`  
		Last Modified: Tue, 24 Feb 2026 20:08:09 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:data` - unknown; unknown

```console
$ docker pull influxdb@sha256:5f0467d4ec768bcb4c700a4dd5f902b2ae1df8f87fe29d6259c92493799e5741
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4700469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bc8463996ea682da5336ee474467e07c1eb3be4cb528ba88155d7cc5440c2be`

```dockerfile
```

-	Layers:
	-	`sha256:92829c2cf557d9451e1bc187054f75422a5afeb34a4d86305f9d37fa7026f09c`  
		Last Modified: Tue, 24 Feb 2026 20:08:10 GMT  
		Size: 4.7 MB (4686392 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d029d29b02f092a4d1ae8cc07df0ffc48d59a2d101c776e333697e726a40f9e`  
		Last Modified: Tue, 24 Feb 2026 20:08:09 GMT  
		Size: 14.1 KB (14077 bytes)  
		MIME: application/vnd.in-toto+json
