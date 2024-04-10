## `rethinkdb:latest`

```console
$ docker pull rethinkdb@sha256:e6e6e339f82e7d05848a9e2c05c2124527de157c9c12688a029884c91bca982b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; s390x

### `rethinkdb:latest` - linux; amd64

```console
$ docker pull rethinkdb@sha256:b6be0f84acf4874044054c34f303028d34c08b6e3fe60716cef323cc33dd2367
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.1 MB (49117652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:500977bd1ddcf525547277af1ffe2e88d71f945bfb479a3356b9d84e05754c0c`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 10 Apr 2024 01:50:48 GMT
ADD file:d4bb05cb4d403a78b4ab5cd8d620330659d5aeb25f847d104ebc02c3a0f32624 in / 
# Wed, 10 Apr 2024 01:50:48 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 13:16:50 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 13:16:52 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list
# Wed, 10 Apr 2024 13:16:52 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Wed, 10 Apr 2024 13:16:57 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 13:16:57 GMT
VOLUME [/data]
# Wed, 10 Apr 2024 13:16:58 GMT
WORKDIR /data
# Wed, 10 Apr 2024 13:16:58 GMT
CMD ["rethinkdb" "--bind" "all"]
# Wed, 10 Apr 2024 13:16:58 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:13808c22b207b066ef43572e57e4fb8c6172e887dd9a918c089a174a19371b7a`  
		Last Modified: Wed, 10 Apr 2024 01:55:34 GMT  
		Size: 29.1 MB (29131358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a28cb05aed215bfea37c062c57c6af6e0db55081dd901784537ec43ec3f930ee`  
		Last Modified: Wed, 10 Apr 2024 13:17:10 GMT  
		Size: 9.8 MB (9786082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6725a6b062d7d686cf47cb52f45dfe25c1ec196c0dd2542cf9995c4fc6a4c26`  
		Last Modified: Wed, 10 Apr 2024 13:17:09 GMT  
		Size: 2.7 KB (2691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89350d47a12bfac59162ea0f7ebd2922862f37cbda97c932776d3f62e0a8ebca`  
		Last Modified: Wed, 10 Apr 2024 13:17:10 GMT  
		Size: 10.2 MB (10197394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bbee74a2d07cc27382e81e18cc744b8a340991d54a485db2eea8c6e92b24cc6`  
		Last Modified: Wed, 10 Apr 2024 13:17:09 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rethinkdb:latest` - linux; arm64 variant v8

```console
$ docker pull rethinkdb@sha256:0b045d96d1956f0fb12c3dcc820d4343d15dceba9837edf1bce508aa2150db04
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.3 MB (48315107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:280acfdee00794215219e64aaa34e2fd76772106296c2b571313f76118fbfcbb`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 10 Apr 2024 00:40:23 GMT
ADD file:c7462f37a5f52b19cd37c5f448dd8959421f489eccea6afa5483d10692994ff6 in / 
# Wed, 10 Apr 2024 00:40:23 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 10:18:30 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 10:18:33 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list
# Wed, 10 Apr 2024 10:18:33 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Wed, 10 Apr 2024 10:18:37 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 10:18:37 GMT
VOLUME [/data]
# Wed, 10 Apr 2024 10:18:37 GMT
WORKDIR /data
# Wed, 10 Apr 2024 10:18:37 GMT
CMD ["rethinkdb" "--bind" "all"]
# Wed, 10 Apr 2024 10:18:37 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:26070551e657534bdf420d43107e85b972b2e8c212413bbbe5d192bd2692c0a7`  
		Last Modified: Wed, 10 Apr 2024 00:44:06 GMT  
		Size: 29.2 MB (29162157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b50712ba3dcfac0e6a0e4f0299c3221e1d99f965ea83addbb0cd11db32152b23`  
		Last Modified: Wed, 10 Apr 2024 10:18:51 GMT  
		Size: 9.6 MB (9582999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce13e769cb18e0043e7b623828b956440a8ddb7534ef65492847690c5be72eb4`  
		Last Modified: Wed, 10 Apr 2024 10:18:50 GMT  
		Size: 2.7 KB (2689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f7da0b65aa281f81b1d352c3452d55f951cd0b8bcbf162a1ee6546e7225d08e`  
		Last Modified: Wed, 10 Apr 2024 10:18:51 GMT  
		Size: 9.6 MB (9567135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad20115b5747cb91f0264b8f1c2fdd32409a17c08f34aa85becea2af94840cf1`  
		Last Modified: Wed, 10 Apr 2024 10:18:50 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rethinkdb:latest` - linux; s390x

```console
$ docker pull rethinkdb@sha256:b30ef1b07d36546a1eeda3d94c0c7b6c5848d718a8759b9e5e2a36eb7e0b5c3f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.3 MB (46281499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eeec7e85f54f19292e796b0468b32616c0a1aa1c6fb7769e0fb9aff4d5ad04f6`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Tue, 12 Mar 2024 00:54:02 GMT
ADD file:80ab985d4871ca6a72156bedfe1038e6b1a89591fc2fd86c4ef778d293223aff in / 
# Tue, 12 Mar 2024 00:54:03 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 04:26:19 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 04:26:21 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list
# Tue, 12 Mar 2024 04:26:21 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Tue, 12 Mar 2024 04:26:27 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 04:26:27 GMT
VOLUME [/data]
# Tue, 12 Mar 2024 04:26:27 GMT
WORKDIR /data
# Tue, 12 Mar 2024 04:26:27 GMT
CMD ["rethinkdb" "--bind" "all"]
# Tue, 12 Mar 2024 04:26:27 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:9cada496cd2b8a88571bf23d513e7fce34888d13321fcf23c6613bffe4c37297`  
		Last Modified: Tue, 12 Mar 2024 01:21:14 GMT  
		Size: 27.5 MB (27488684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ca3c756f7efa867c2fa90dcc45c2c75b1ace64aaf616294becdf5c0b6349e0e`  
		Last Modified: Tue, 12 Mar 2024 04:27:35 GMT  
		Size: 9.3 MB (9282131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abe3aa82e64e54c83eb8b048054b4b86a1a4b466e30d5a6eb86f831d4bbe9afb`  
		Last Modified: Tue, 12 Mar 2024 04:27:34 GMT  
		Size: 2.7 KB (2684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5bc71716bc0b3bf58b80fda87b73e792e529e1136047fb2aba9763e9ef03908`  
		Last Modified: Tue, 12 Mar 2024 04:27:35 GMT  
		Size: 9.5 MB (9507873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d0fe23b6dc49468f5432982434c8862924e8994b84c93b8af157bedca152c3a`  
		Last Modified: Tue, 12 Mar 2024 04:27:34 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
