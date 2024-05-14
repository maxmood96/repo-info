## `rethinkdb:latest`

```console
$ docker pull rethinkdb@sha256:5e54e67b9a75df4694569caa39eab96b483bdbf3c85f3713ee280f1e4260491a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; s390x

### `rethinkdb:latest` - linux; amd64

```console
$ docker pull rethinkdb@sha256:ea9b7b0dc7ae26cd29714e7df8a5a537fae0d4537b2611a1357c5ee291bb5e80
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.1 MB (49141590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:830099f65c358d289727dccc97cda8a8a8cb5e75f98d2e476b8812e60ad760f5`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:09 GMT
ADD file:4b1be1de1a1e5aa608c688cad2824587262081866180d7368feb79d33ca05953 in / 
# Wed, 24 Apr 2024 03:28:09 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 08:38:35 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 08:38:37 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list
# Wed, 24 Apr 2024 08:38:37 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Wed, 24 Apr 2024 08:38:42 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 08:38:42 GMT
VOLUME [/data]
# Wed, 24 Apr 2024 08:38:42 GMT
WORKDIR /data
# Wed, 24 Apr 2024 08:38:42 GMT
CMD ["rethinkdb" "--bind" "all"]
# Wed, 24 Apr 2024 08:38:42 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:b0a0cf830b12453b7e15359a804215a7bcccd3788e2bcecff2a03af64bbd4df7`  
		Last Modified: Wed, 24 Apr 2024 03:32:41 GMT  
		Size: 29.2 MB (29150479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:811f1f5f65861187edb2cdfbd26f8bacf9c8751b4c32285cf7832585830884c5`  
		Last Modified: Wed, 24 Apr 2024 08:38:56 GMT  
		Size: 9.8 MB (9789565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23acfb916b8573536a7540b21cb499edfd3e653c2125da515b73ba1edc07a0d9`  
		Last Modified: Wed, 24 Apr 2024 08:38:54 GMT  
		Size: 2.7 KB (2690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b21ee001743eaeaceb402752098c4889d0efe7d04309c123c6ffa0be493e53cb`  
		Last Modified: Wed, 24 Apr 2024 08:38:56 GMT  
		Size: 10.2 MB (10198729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77fee7b493de5b6a2ab7fa8c6c4519776f92948bf3c287a358c7b1c102ed7423`  
		Last Modified: Wed, 24 Apr 2024 08:38:54 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rethinkdb:latest` - linux; arm64 variant v8

```console
$ docker pull rethinkdb@sha256:161e52d1adaddd71bf4a0acfe5189d1848364a6cb00a41484d3b39839440a1e6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.3 MB (48337826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f264f6824063afe6f31545dd8351a851a4ea550aeb4f9aa23b1c54db5257b48b`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:39 GMT
ADD file:ea7004fb788ab5cf1604d6e71153c48d99b75fbd1810e78a8c79faff11fe6771 in / 
# Wed, 24 Apr 2024 04:10:39 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:49:53 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:49:55 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list
# Wed, 24 Apr 2024 04:49:55 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Wed, 24 Apr 2024 04:49:59 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:49:59 GMT
VOLUME [/data]
# Wed, 24 Apr 2024 04:49:59 GMT
WORKDIR /data
# Wed, 24 Apr 2024 04:49:59 GMT
CMD ["rethinkdb" "--bind" "all"]
# Wed, 24 Apr 2024 04:49:59 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:22d97f6a5d13532e867231d23d92620a81874d51a456196be50154eeb32edc08`  
		Last Modified: Wed, 24 Apr 2024 04:14:07 GMT  
		Size: 29.2 MB (29179935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfc0de14d782bc0e476cc0196ae3518fa98f27d11bd27575470ec1038a9d27db`  
		Last Modified: Wed, 24 Apr 2024 04:50:11 GMT  
		Size: 9.6 MB (9586328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38ab8b57f6e349893d2559c48c31675572b8330a600fa83e437461b3abd4d2ea`  
		Last Modified: Wed, 24 Apr 2024 04:50:10 GMT  
		Size: 2.7 KB (2688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad8d35ca603a2301536d6e94d426d002c1338d15aec4f67f0e2019983b832842`  
		Last Modified: Wed, 24 Apr 2024 04:50:11 GMT  
		Size: 9.6 MB (9568748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afbf530bbb9d4a0f020ddaf2c5b2390cd2e2d733a5890a22a534b2f741111fdb`  
		Last Modified: Wed, 24 Apr 2024 04:50:10 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rethinkdb:latest` - linux; s390x

```console
$ docker pull rethinkdb@sha256:bf9f945c9ced8781516fa0bc11e7586392650786159dad6b066a94119165c8f7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.3 MB (46310039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddfdf48dccd40456670078bdc5790874b68296beea53dec903f36dbbc65d48c4`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Tue, 14 May 2024 00:42:38 GMT
ADD file:55fef93bbad6701fe968a070a0c72b3a0bd3df408dd79c9a616a43dea0de11d0 in / 
# Tue, 14 May 2024 00:42:40 GMT
CMD ["bash"]
# Tue, 14 May 2024 01:18:50 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 01:18:51 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list
# Tue, 14 May 2024 01:18:52 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Tue, 14 May 2024 01:18:56 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 01:18:57 GMT
VOLUME [/data]
# Tue, 14 May 2024 01:18:57 GMT
WORKDIR /data
# Tue, 14 May 2024 01:18:57 GMT
CMD ["rethinkdb" "--bind" "all"]
# Tue, 14 May 2024 01:18:57 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:d7365433874e83ccc92aa5d768989641a64e23c3247409161401a09b4895c406`  
		Last Modified: Tue, 14 May 2024 00:47:35 GMT  
		Size: 27.5 MB (27512398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acc5c572afdedeaca6681d3c0dc2cfdb67d002f35150da2633b88e20aa5e5d34`  
		Last Modified: Tue, 14 May 2024 01:19:14 GMT  
		Size: 9.3 MB (9285266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1cc0f996249a1f0bf7794daf63071c31a4cf1d3c875be84a9e708c19024ee96`  
		Last Modified: Tue, 14 May 2024 01:19:13 GMT  
		Size: 2.7 KB (2686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a7b545a983ddf80be29e7748c1b60da945d45cc98acdebea90b62c5ea3026d3`  
		Last Modified: Tue, 14 May 2024 01:19:14 GMT  
		Size: 9.5 MB (9509562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f9a2bde40d7d80f69ef40483f66ae62b1faa4de1c3364d486f487c379f0e6c7`  
		Last Modified: Tue, 14 May 2024 01:19:13 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
