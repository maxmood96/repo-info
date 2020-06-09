## `rethinkdb:buster-slim`

```console
$ docker pull rethinkdb@sha256:b10f13d9bd646e4c215da7fa37f5ecfd3d5ac8b70cd63276b2163ba4ac7bb1c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `rethinkdb:buster-slim` - linux; amd64

```console
$ docker pull rethinkdb@sha256:d352aa03b37b132524a3ccecf22a7d246797dad23011f68b7c0e0b27ad7c4a67
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51762273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1efb5d6e94db37aa27d0591f965c6edc5ad9a922c4c291f82fac000f5bf8c94`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Tue, 09 Jun 2020 01:20:56 GMT
ADD file:4d35f6c8bbbe6801cc5f44989730fb6d349a644ecb36eca481e7df25842d6321 in / 
# Tue, 09 Jun 2020 01:20:56 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 16:55:55 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 16:55:59 GMT
RUN apt-key adv --keyserver keys.gnupg.net --recv-keys "539A 3A8C 6692 E6E3 F69B 3FE8 1D85 E93F 801B B43F"     && echo "deb https://download.rethinkdb.com/repository/debian-buster buster main" > /etc/apt/sources.list.d/rethinkdb.list
# Tue, 09 Jun 2020 16:56:00 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.0~0buster
# Tue, 09 Jun 2020 16:56:13 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 16:56:13 GMT
VOLUME [/data]
# Tue, 09 Jun 2020 16:56:14 GMT
WORKDIR /data
# Tue, 09 Jun 2020 16:56:14 GMT
CMD ["rethinkdb" "--bind" "all"]
# Tue, 09 Jun 2020 16:56:14 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:8559a31e96f442f2c7b6da49d6c84705f98a39d8be10b3f5f14821d0ee8417df`  
		Last Modified: Tue, 09 Jun 2020 01:25:50 GMT  
		Size: 27.1 MB (27098265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd489a3fa35f7c676839eccfd5cb575ab1aa93818f5ff68f5b58743ca782dff0`  
		Last Modified: Tue, 09 Jun 2020 16:56:40 GMT  
		Size: 6.7 MB (6669162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42fd253e9349ad79532244aa7f3f238f5ab1447f20addc9447204f8876be6b79`  
		Last Modified: Tue, 09 Jun 2020 16:56:37 GMT  
		Size: 2.6 KB (2616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:705a8028ffa89e68111acdd7bc999322750a47e9605d9b7b79fc15360b3e0f29`  
		Last Modified: Tue, 09 Jun 2020 16:56:42 GMT  
		Size: 18.0 MB (17992139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d792bf469841c2d38ce8a52aabc00be5e47158776d0b607cd16744fc80b71e30`  
		Last Modified: Tue, 09 Jun 2020 16:56:37 GMT  
		Size: 91.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
