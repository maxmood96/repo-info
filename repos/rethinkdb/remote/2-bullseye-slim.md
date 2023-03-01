## `rethinkdb:2-bullseye-slim`

```console
$ docker pull rethinkdb@sha256:c673e8baf3172705268909efe00fb236d455b44ca6360df4e3e2a884c190b68d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; s390x

### `rethinkdb:2-bullseye-slim` - linux; amd64

```console
$ docker pull rethinkdb@sha256:f2bab4f667cf39ee9577ca292bd85aa200bc58c102f0d6d599d8daf1a994f4b2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 MB (47978749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a91f3e5a27e9a583b667e75827f9277713fbd67a8147dd1a22eb5f1fa6680384`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 01 Mar 2023 04:09:58 GMT
ADD file:493a5b0c8d2d63a1343258b3f9aa5fcd59a93f44fe26ad9e56b094c3a08fd3be in / 
# Wed, 01 Mar 2023 04:09:59 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 16:47:29 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 16:47:31 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bullseye bullseye main" > /etc/apt/sources.list.d/rethinkdb.list
# Wed, 01 Mar 2023 16:47:31 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.2~0bullseye
# Wed, 01 Mar 2023 16:47:36 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 16:47:37 GMT
VOLUME [/data]
# Wed, 01 Mar 2023 16:47:37 GMT
WORKDIR /data
# Wed, 01 Mar 2023 16:47:37 GMT
CMD ["rethinkdb" "--bind" "all"]
# Wed, 01 Mar 2023 16:47:37 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:3f9582a2cbe7197f39185419c0ced2c986389f8fc6aa805e1f5c090eea6511e0`  
		Last Modified: Wed, 01 Mar 2023 04:14:23 GMT  
		Size: 31.4 MB (31411403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcdb5586b0fe92f1ed8dbddcd64dc35b4d59695d5d70acf9efd562e93521f05c`  
		Last Modified: Wed, 01 Mar 2023 16:47:52 GMT  
		Size: 6.3 MB (6328659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:387899c9513e847717d1f3889e5f52eb106e5a607c9a0036dad051855b0d36ab`  
		Last Modified: Wed, 01 Mar 2023 16:47:51 GMT  
		Size: 2.7 KB (2689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76fd507bf127647bf96226177270c6158d50514db5f458d363b39fc9c3e953f3`  
		Last Modified: Wed, 01 Mar 2023 16:47:53 GMT  
		Size: 10.2 MB (10235871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f01eab8e58b9a37fe9704ba3d5cfc2f2c6413e63f2addcadc9e459ffe94d3a18`  
		Last Modified: Wed, 01 Mar 2023 16:47:51 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rethinkdb:2-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull rethinkdb@sha256:8cbef36d2505be4106e20329e5bf9ebf829619506543d12ead68e85bd986a934
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.0 MB (45963048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b45a24685707ce24d3e722730cdd321645240f099a43e619fe11ecae905f943b`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 01 Mar 2023 02:20:39 GMT
ADD file:9dc5c6fb6431df80107eddb76fb18256d6f4a06b4b22f9a7c4bcd58476068186 in / 
# Wed, 01 Mar 2023 02:20:39 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 12:28:04 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 12:28:07 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bullseye bullseye main" > /etc/apt/sources.list.d/rethinkdb.list
# Wed, 01 Mar 2023 12:28:07 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.2~0bullseye
# Wed, 01 Mar 2023 12:28:11 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 12:28:11 GMT
VOLUME [/data]
# Wed, 01 Mar 2023 12:28:11 GMT
WORKDIR /data
# Wed, 01 Mar 2023 12:28:11 GMT
CMD ["rethinkdb" "--bind" "all"]
# Wed, 01 Mar 2023 12:28:11 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:66dbba0fb1b568cc3ffd53409ba2f9f82995ab7f80e379338f3f36e4dcd223be`  
		Last Modified: Wed, 01 Mar 2023 02:24:17 GMT  
		Size: 30.1 MB (30062814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c8c0948f4d1ba003c67fc23b18860d9c770c272a1abc5561d175ddba12ee8c1`  
		Last Modified: Wed, 01 Mar 2023 12:28:25 GMT  
		Size: 6.3 MB (6309611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dda6b95fba3131558bd564a9b2a6e66392342d5de660cfd409f1c8390f578d9`  
		Last Modified: Wed, 01 Mar 2023 12:28:24 GMT  
		Size: 2.7 KB (2689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a19e7198f729dad152bbd1dbbd3ad2f705de2dda4829e93f286ef9155519666`  
		Last Modified: Wed, 01 Mar 2023 12:28:25 GMT  
		Size: 9.6 MB (9587809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:482fe7eb5bd94a33f9a1367ede1f6cb01f6d391065b864bff04b36aa17eda383`  
		Last Modified: Wed, 01 Mar 2023 12:28:24 GMT  
		Size: 125.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rethinkdb:2-bullseye-slim` - linux; s390x

```console
$ docker pull rethinkdb@sha256:7e0c96a6771531746c17cb3dcd0d8d342d33b79934f29a12fd37eb3d289e582e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45427550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d369e305496614dfa1ffd8086896d2617c131bee05d1df9acc1068dea7972130`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 01 Mar 2023 02:50:30 GMT
ADD file:01aa3de7444f0716938e0d85522be065193be4ffb6788b3190a0f4fefdbb8d65 in / 
# Wed, 01 Mar 2023 02:50:31 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 06:37:03 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 06:37:05 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bullseye bullseye main" > /etc/apt/sources.list.d/rethinkdb.list
# Wed, 01 Mar 2023 06:37:05 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.2~0bullseye
# Wed, 01 Mar 2023 06:37:10 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 06:37:11 GMT
VOLUME [/data]
# Wed, 01 Mar 2023 06:37:11 GMT
WORKDIR /data
# Wed, 01 Mar 2023 06:37:11 GMT
CMD ["rethinkdb" "--bind" "all"]
# Wed, 01 Mar 2023 06:37:11 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:7b8d78f42e32e7fa234bcf890ae6603acab2881bca68a9d8c429981c7f42b1d6`  
		Last Modified: Wed, 01 Mar 2023 02:54:48 GMT  
		Size: 29.6 MB (29646854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9406695806fa1d92b5baf40391490c4e06168ff3d79ddc4b6648e3506908464a`  
		Last Modified: Wed, 01 Mar 2023 06:37:35 GMT  
		Size: 6.2 MB (6205439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c96bd7e99e7fd101c8bec2989ff09cd32ab2a07c2c664a92b8f03c04b3fd04d1`  
		Last Modified: Wed, 01 Mar 2023 06:37:34 GMT  
		Size: 2.7 KB (2688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45e004c6cfa9121e3a6fa242b4bef8457b812b58fef5ca23cb26596d852b67bb`  
		Last Modified: Wed, 01 Mar 2023 06:37:36 GMT  
		Size: 9.6 MB (9572442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6806471eb8da2f42231e85ac0279acd808a7b9c1fbe5a02e8d28269f9b0130a6`  
		Last Modified: Wed, 01 Mar 2023 06:37:34 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
