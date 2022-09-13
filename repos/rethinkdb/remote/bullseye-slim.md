## `rethinkdb:bullseye-slim`

```console
$ docker pull rethinkdb@sha256:3fb8bd8c1895632a26ca5522a4d8402067bf52817993adc50fe2d476e6d616d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; s390x

### `rethinkdb:bullseye-slim` - linux; amd64

```console
$ docker pull rethinkdb@sha256:38567f8b58adee4afef34f3da1e8977620beae8f438543dc5852fe141bab17b3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 MB (47971233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c88841f94073e4a4de709748296bcbb3b2d0fa49594c8eb021194078655ab5ec`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Tue, 13 Sep 2022 00:56:29 GMT
ADD file:5bd53bff884e470b3c12425132975ab9c6f99002c62c43bca1ff5cde9d863b92 in / 
# Tue, 13 Sep 2022 00:56:29 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 12:19:53 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 12:19:55 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bullseye bullseye main" > /etc/apt/sources.list.d/rethinkdb.list
# Tue, 13 Sep 2022 12:19:55 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.2~0bullseye
# Tue, 13 Sep 2022 12:20:00 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 12:20:00 GMT
VOLUME [/data]
# Tue, 13 Sep 2022 12:20:00 GMT
WORKDIR /data
# Tue, 13 Sep 2022 12:20:00 GMT
CMD ["rethinkdb" "--bind" "all"]
# Tue, 13 Sep 2022 12:20:00 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:31b3f1ad4ce1f369084d0f959813c51df0ca17d9877d5ee88c2db6ff88341430`  
		Last Modified: Tue, 13 Sep 2022 01:00:29 GMT  
		Size: 31.4 MB (31404121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45f57028eb1835632ed6cb05e8fb6e595a099691695fe70fc4d0b538d508c779`  
		Last Modified: Tue, 13 Sep 2022 12:20:17 GMT  
		Size: 6.3 MB (6328527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c190e787845007b74dd0acff2755df53f36f1320e30af694da5ff7242d220b3d`  
		Last Modified: Tue, 13 Sep 2022 12:20:17 GMT  
		Size: 2.7 KB (2690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fff8094f62d4eefbecddd28a679666997b932797d0adb19d2f6bcccea4fca53`  
		Last Modified: Tue, 13 Sep 2022 12:20:18 GMT  
		Size: 10.2 MB (10235768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d65cd60e9d3915400c98d67708edc01e1f2fa570a51d3391b0177f58b3621df5`  
		Last Modified: Tue, 13 Sep 2022 12:20:16 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rethinkdb:bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull rethinkdb@sha256:f5b96489210618ed825621d9f01f8f0f0a59e1ecaaf0f92af54794a58c3f0bbb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.5 MB (45542059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:993e852e4f6f9b06b18beebf599dd549a6fb1df90caac8208f1c3dbb55f02918`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Tue, 23 Aug 2022 01:52:32 GMT
ADD file:90344130400909b0ad12bb54d439b0e4868fc5863f538f676e6fdfeaeb4dad51 in / 
# Tue, 23 Aug 2022 01:52:33 GMT
CMD ["bash"]
# Tue, 23 Aug 2022 17:33:50 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 17:33:52 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bullseye bullseye main" > /etc/apt/sources.list.d/rethinkdb.list
# Tue, 23 Aug 2022 17:33:53 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.2~0bullseye
# Tue, 23 Aug 2022 17:33:58 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 17:33:59 GMT
VOLUME [/data]
# Tue, 23 Aug 2022 17:34:00 GMT
WORKDIR /data
# Tue, 23 Aug 2022 17:34:01 GMT
CMD ["rethinkdb" "--bind" "all"]
# Tue, 23 Aug 2022 17:34:02 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:5b142346550416c75ea412d21741de5eaf3e76857affc12fab789277f81f53b3`  
		Last Modified: Tue, 23 Aug 2022 01:58:00 GMT  
		Size: 30.1 MB (30063788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8df3b4e10490fe18d4cefcfd0ac879109eb8f61fa40ccf2feb966491eb8d6071`  
		Last Modified: Tue, 23 Aug 2022 17:34:28 GMT  
		Size: 6.1 MB (6103355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fed0200c2fa6764d4ea192e8eae6a4fdc68b21f3c32ee7c0709d0f82c862e92c`  
		Last Modified: Tue, 23 Aug 2022 17:34:27 GMT  
		Size: 2.7 KB (2670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24d66e99d4413325381a48b676addb6a154edb71813b3cc53d721b6a464a492d`  
		Last Modified: Tue, 23 Aug 2022 17:34:28 GMT  
		Size: 9.4 MB (9372153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ed012e5dff886545941674b755fa01f56eac483d0c2df92153abdd91b711645`  
		Last Modified: Tue, 23 Aug 2022 17:34:27 GMT  
		Size: 93.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rethinkdb:bullseye-slim` - linux; s390x

```console
$ docker pull rethinkdb@sha256:78d2f2b9ef9c7b5acb9d1f0c067c1f20eb126512caf9583122cd207083711b2b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45416018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82757c2a85810b65f1a192806a47b28b3a382f84cbd099ef75b730a341459221`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Tue, 13 Sep 2022 00:48:07 GMT
ADD file:e8a6c2e8be5d9d1f83c1e280419014489438391a9feb7c77b6c21adbf0ec062b in / 
# Tue, 13 Sep 2022 00:48:08 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 06:52:33 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 06:52:36 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bullseye bullseye main" > /etc/apt/sources.list.d/rethinkdb.list
# Tue, 13 Sep 2022 06:52:36 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.2~0bullseye
# Tue, 13 Sep 2022 06:52:42 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 06:52:42 GMT
VOLUME [/data]
# Tue, 13 Sep 2022 06:52:42 GMT
WORKDIR /data
# Tue, 13 Sep 2022 06:52:43 GMT
CMD ["rethinkdb" "--bind" "all"]
# Tue, 13 Sep 2022 06:52:43 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:c64715e5ebd39975a39b5cf2535772544c27713cbed678b0a21e73680fffaf72`  
		Last Modified: Tue, 13 Sep 2022 00:52:39 GMT  
		Size: 29.6 MB (29635080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3d90ae81aa48a6524de47405ccda60aa21c6019a0e5ce06910111a253b10947`  
		Last Modified: Tue, 13 Sep 2022 06:53:10 GMT  
		Size: 6.2 MB (6205669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e9f0b2c76f6722904687acef1569fd85c4ed9fdbcd3c1f2a641379141fe0274`  
		Last Modified: Tue, 13 Sep 2022 06:53:10 GMT  
		Size: 2.7 KB (2689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6ad2716a6c3e2534cf18ef82bf9b1adf79d3060548e805457f70f55b96b1c98`  
		Last Modified: Tue, 13 Sep 2022 06:53:10 GMT  
		Size: 9.6 MB (9572453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d6fd9d26d856864d33ffb44a1773a1c20ee8209228bcdff1186241bbabf10a6`  
		Last Modified: Tue, 13 Sep 2022 06:53:09 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
