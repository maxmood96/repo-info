## `rethinkdb:bookworm-slim`

```console
$ docker pull rethinkdb@sha256:03a6f9e2e9004244d66f20059fe8007f82407ce8f8f8362f95e0078117df6239
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; s390x

### `rethinkdb:bookworm-slim` - linux; amd64

```console
$ docker pull rethinkdb@sha256:dd007cd446acf2878d0a37fe0574ce7425b33374df7f30d1c5f9fd99e03a3d18
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.1 MB (49110388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c31c95ff96e1207cde2d566d5913ff5d2101f5a9cd98eb27df500a82a39296c`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:22 GMT
ADD file:eb6a3def1f69e76655620640e610015f285bc23c97e89855feb1f0548309d518 in / 
# Tue, 13 Feb 2024 00:37:22 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 07:46:36 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 07:46:37 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list
# Tue, 13 Feb 2024 07:46:38 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Tue, 13 Feb 2024 07:46:43 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 07:46:43 GMT
VOLUME [/data]
# Tue, 13 Feb 2024 07:46:43 GMT
WORKDIR /data
# Tue, 13 Feb 2024 07:46:43 GMT
CMD ["rethinkdb" "--bind" "all"]
# Tue, 13 Feb 2024 07:46:43 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:e1caac4eb9d2ec24aa3618e5992208321a92492aef5fef5eb9e470895f771c56`  
		Last Modified: Tue, 13 Feb 2024 00:42:02 GMT  
		Size: 29.1 MB (29124091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18a44559cf6da4b22a0bdc3be2f91b4d02d500d3f2cfc0660fc97c9fc3e535db`  
		Last Modified: Tue, 13 Feb 2024 07:46:55 GMT  
		Size: 9.8 MB (9786050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc8525f73bea1db5209d6742581ae1be2b9822a0b025bcfa7e86dc8f8454c38e`  
		Last Modified: Tue, 13 Feb 2024 07:46:53 GMT  
		Size: 2.7 KB (2687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3238e0a1904d9778e912ccdccd38fd54201cb844c8cfeb73b016963842765c7`  
		Last Modified: Tue, 13 Feb 2024 07:46:54 GMT  
		Size: 10.2 MB (10197433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ea6d2ec54c157b140cbad47a0bafe8801ba2e5d70dd92d4e6ae6080be644e00`  
		Last Modified: Tue, 13 Feb 2024 07:46:53 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rethinkdb:bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull rethinkdb@sha256:1ab8ee90b2f5ea44cb6053c2f11e672557b2ae17d6f394b58f8134ca2f24217f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.3 MB (48309246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afe5ce06836ab0dc847cddf3f99f9f5a50626829f319087a0ad07145bd592b08`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:20 GMT
ADD file:a3e4f94158c3515dc70de5aa81c136a9f7daf5adcac636a15c237097cb454140 in / 
# Tue, 13 Feb 2024 00:41:20 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 07:23:31 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 07:23:33 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list
# Tue, 13 Feb 2024 07:23:33 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Tue, 13 Feb 2024 07:23:37 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 07:23:37 GMT
VOLUME [/data]
# Tue, 13 Feb 2024 07:23:37 GMT
WORKDIR /data
# Tue, 13 Feb 2024 07:23:37 GMT
CMD ["rethinkdb" "--bind" "all"]
# Tue, 13 Feb 2024 07:23:37 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:f546e941f15b76df3d982d56985432b05bc065e3923fb35be25a4d33d5c0f911`  
		Last Modified: Tue, 13 Feb 2024 00:44:54 GMT  
		Size: 29.2 MB (29156363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23adf2df0c1e863ab5fdfb489a7723ba69263c310f9d3df0b54ae9b5923fb7cd`  
		Last Modified: Tue, 13 Feb 2024 07:23:49 GMT  
		Size: 9.6 MB (9582920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca3f243cf8d00d0cc8d84d3243655215482ff1cb6f41b24b8f9547093b7ab074`  
		Last Modified: Tue, 13 Feb 2024 07:23:48 GMT  
		Size: 2.7 KB (2685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:828f8a8efe7e8178f1cd335981009db52076a0f220c5e54e14545121f62da74c`  
		Last Modified: Tue, 13 Feb 2024 07:23:49 GMT  
		Size: 9.6 MB (9567151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1166ac7e9d4081ca134aabb4fc5c9be89ce6fd95fd604d84287d2a1369bf91f7`  
		Last Modified: Tue, 13 Feb 2024 07:23:48 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rethinkdb:bookworm-slim` - linux; s390x

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
