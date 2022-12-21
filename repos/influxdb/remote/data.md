## `influxdb:data`

```console
$ docker pull influxdb@sha256:b8d023d1285c70cfebc10026dcb52ab0bf193e829c0889d75fdb49a2d409535a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `influxdb:data` - linux; amd64

```console
$ docker pull influxdb@sha256:3b66c5c8ee6b2b8680349849451f0c84ac8346fe661404ed1130625ef7dec0a2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.8 MB (127774937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df2be3f6981bd2b34e491930f37718182381a272da2f4747b43fd13be7ee3ec0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 21 Dec 2022 01:20:21 GMT
ADD file:c13b430c8699df107ffd9ea5230b92238bc037a8e1cbbe35d6ab664941d575da in / 
# Wed, 21 Dec 2022 01:20:22 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 11:13:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 11:13:58 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 21 Dec 2022 20:00:55 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 21 Dec 2022 20:01:06 GMT
ENV INFLUXDB_VERSION=1.8.10-c1.8.10
# Wed, 21 Dec 2022 20:01:12 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}_amd64.deb*
# Wed, 21 Dec 2022 20:01:13 GMT
COPY file:bf2f42b62a32a7ee3ab93d9a5e451b7d59af1a97e40dc4a76b8aaf2f64383d7a in /etc/influxdb/influxdb.conf 
# Wed, 21 Dec 2022 20:01:13 GMT
EXPOSE 8086
# Wed, 21 Dec 2022 20:01:13 GMT
VOLUME [/var/lib/influxdb]
# Wed, 21 Dec 2022 20:01:13 GMT
COPY file:182a0176834db40043100d082d05e5aded9887c94b02416f6e3154c827c07360 in /entrypoint.sh 
# Wed, 21 Dec 2022 20:01:13 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Wed, 21 Dec 2022 20:01:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 21 Dec 2022 20:01:13 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:32de3c850997ce03b6ff4ae8fb00b34b9d7d7f9a35bfcdb8538e22cc7b77c29d`  
		Last Modified: Wed, 21 Dec 2022 01:24:10 GMT  
		Size: 55.0 MB (55025166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa1d4c8d85a4e064e50cea74d4aa848dc5fc275aef223fcc1f21fbdb1b5dd182`  
		Last Modified: Wed, 21 Dec 2022 11:21:24 GMT  
		Size: 5.2 MB (5163298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c796299bbbddc7aeada9539a4e7874a75fa2b6ff421f8d5ad40f227b40ab4d86`  
		Last Modified: Wed, 21 Dec 2022 11:21:24 GMT  
		Size: 10.9 MB (10876681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5d3e05d16cd1d3c21c0c1001e437e4bcebc7d4a5deae70b54d55948d6d99ab0`  
		Last Modified: Wed, 21 Dec 2022 20:03:41 GMT  
		Size: 2.9 KB (2903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:237578ced2c487cb6be41a98e661c8f75d953efdbac024482ee6b37bef8267e6`  
		Last Modified: Wed, 21 Dec 2022 20:04:05 GMT  
		Size: 56.7 MB (56705115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc95bf8713df5bd0e84a26e388429a03fdc9518db60a1af74cdcbf165b8fe269`  
		Last Modified: Wed, 21 Dec 2022 20:03:57 GMT  
		Size: 242.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d077efca810f9118484bf64834721e32fd40f5b177051c2b26fea3ddd1ed3188`  
		Last Modified: Wed, 21 Dec 2022 20:03:57 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc664d61eb087c3d1789223b39d7b8ba6cdc4250cdfdc67ccc2bd9f60db1c5c1`  
		Last Modified: Wed, 21 Dec 2022 20:03:57 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
