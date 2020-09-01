## `influxdb:meta`

```console
$ docker pull influxdb@sha256:07aea0a0675a39dd81f65cbbf8dc89339cf748a0c20962b3b7c0e6f92f4bffb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:meta` - linux; amd64

```console
$ docker pull influxdb@sha256:a5b4e8086f3ee62f22cde69fda92eef3f85dacd1f31f96db08cf4915d96273e3
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.3 MB (83310713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d94f36502c1fa4d24a85a9e653db8f80a7d5f989491ae65ca0a91c327d4980e3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Tue, 04 Aug 2020 15:45:32 GMT
ADD file:a28d8a949b7577768d87fcbac346797fc5f7bad0539625339edcd09a32d6bf77 in / 
# Tue, 04 Aug 2020 15:45:33 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 23:35:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 23:36:04 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 05 Aug 2020 16:33:30 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Tue, 01 Sep 2020 00:59:55 GMT
ENV INFLUXDB_VERSION=1.8.2-c1.8.2
# Tue, 01 Sep 2020 01:00:36 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}_amd64.deb*
# Tue, 01 Sep 2020 01:00:36 GMT
COPY file:5d8d1b0acfd7ca05cf6698246b28d240206fa448f4aa5ac839c9ad323adbeac2 in /etc/influxdb/influxdb-meta.conf 
# Tue, 01 Sep 2020 01:00:36 GMT
EXPOSE 8091
# Tue, 01 Sep 2020 01:00:37 GMT
VOLUME [/var/lib/influxdb]
# Tue, 01 Sep 2020 01:00:37 GMT
COPY file:126b1f7e41b4975cf2ce23037cf6a46253fb817023062317380c48ff5df47228 in /entrypoint.sh 
# Tue, 01 Sep 2020 01:00:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 01 Sep 2020 01:00:38 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:419e7ae5bb1e4875c367f3249b7bb7f8f39dd27dfceb4ee9d6a92191ed1c452f`  
		Last Modified: Tue, 04 Aug 2020 15:52:05 GMT  
		Size: 45.4 MB (45366706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:848839e0cd3b3acc96db8a39c4520a40f98dc8f3a2a5f80b575ff4a1c88f1fcf`  
		Last Modified: Tue, 04 Aug 2020 23:42:18 GMT  
		Size: 10.8 MB (10750599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de30e8b35015c7302e071e9c2b449290f270feaf2a419f6466a555b6907e7d72`  
		Last Modified: Tue, 04 Aug 2020 23:42:17 GMT  
		Size: 4.3 MB (4339945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95a43b78da5c81aca131b2d8a546d90ced7de3336296ea931086cbafe0a5b68f`  
		Last Modified: Wed, 05 Aug 2020 16:35:07 GMT  
		Size: 2.8 KB (2775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:116c924a3547a258fec0c1c9ed1bc7eb17a0de71baa11af6bf0ed1f60bbe33eb`  
		Last Modified: Tue, 01 Sep 2020 01:03:51 GMT  
		Size: 22.9 MB (22850117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:518ab3e2f070b215ac3064077bb5e0abf31640051d34604f0f36e613a046ecb4`  
		Last Modified: Tue, 01 Sep 2020 01:03:46 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e197bcd8c3822fa41d333588d2f07e34b5b5ef44ad533e56ddb5938d38ce372f`  
		Last Modified: Tue, 01 Sep 2020 01:03:46 GMT  
		Size: 375.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
