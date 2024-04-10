## `rethinkdb:latest`

```console
$ docker pull rethinkdb@sha256:368934c3059be39d54301edd75d3eb48b685ebfffe54af5a925517e2e000007f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; s390x

### `rethinkdb:latest` - linux; amd64

```console
$ docker pull rethinkdb@sha256:f2709d2fd6bd1c2baedcccdd579db42e01e998a412267f1b373cc4211a6091d3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.1 MB (49110367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f897ad975be9ab0be45a0d44d87a8e8a111b28dcfa084e5d2fd5495d77a4867`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Tue, 12 Mar 2024 01:21:01 GMT
ADD file:b86ae1c7ca3586d8feedcd9ff1b2b1e8ab872caf6587618f1da689045a5d7ae4 in / 
# Tue, 12 Mar 2024 01:21:01 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 10:11:41 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 10:11:43 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list
# Tue, 12 Mar 2024 10:11:43 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Tue, 12 Mar 2024 10:11:48 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 10:11:48 GMT
VOLUME [/data]
# Tue, 12 Mar 2024 10:11:48 GMT
WORKDIR /data
# Tue, 12 Mar 2024 10:11:48 GMT
CMD ["rethinkdb" "--bind" "all"]
# Tue, 12 Mar 2024 10:11:48 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:8a1e25ce7c4f75e372e9884f8f7b1bedcfe4a7a7d452eb4b0a1c7477c9a90345`  
		Last Modified: Tue, 12 Mar 2024 01:25:41 GMT  
		Size: 29.1 MB (29124181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12dd38add8be1f1d0af76956c5bfc708168f82bbd2c6c00c353c7dcf1257a7ec`  
		Last Modified: Tue, 12 Mar 2024 10:12:01 GMT  
		Size: 9.8 MB (9785983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5016670844f5da0591fc28871919854ed174ac1bbc6b4a9c46ba2411764dfe64`  
		Last Modified: Tue, 12 Mar 2024 10:11:59 GMT  
		Size: 2.7 KB (2688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c5ee511ebf807f79de4eb4e6b83a0f9462ca10443f50e844e128d6a348ec38d`  
		Last Modified: Tue, 12 Mar 2024 10:12:01 GMT  
		Size: 10.2 MB (10197388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f062e939ed24383cfee1414d1b88c09f068734d20ab2fc55a52ff89ba5b7191e`  
		Last Modified: Tue, 12 Mar 2024 10:11:59 GMT  
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
