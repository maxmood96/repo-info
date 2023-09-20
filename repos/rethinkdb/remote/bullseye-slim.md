## `rethinkdb:bullseye-slim`

```console
$ docker pull rethinkdb@sha256:93ad8151e34932894c9290cdf233bf297714854ff47ab47942c45284997566f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; s390x

### `rethinkdb:bullseye-slim` - linux; amd64

```console
$ docker pull rethinkdb@sha256:54eb5c5246ca882a27f1b2a92d7e20429cd2f37f3c7dd77e12effb9fe2694bff
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 MB (47985337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d03a09c2d2675e5810ea43ecfa53372900accfe35ab31b88d123c07d4f654a33`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Thu, 07 Sep 2023 00:21:13 GMT
ADD file:cb5fcc80c057b356a31492a20c6e3a75b70ed70a663506c8e97ad730ae32a02d in / 
# Thu, 07 Sep 2023 00:21:13 GMT
CMD ["bash"]
# Thu, 07 Sep 2023 02:31:51 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 02:31:53 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bullseye bullseye main" > /etc/apt/sources.list.d/rethinkdb.list
# Thu, 07 Sep 2023 02:31:53 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.2~0bullseye
# Thu, 07 Sep 2023 02:31:58 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 02:31:58 GMT
VOLUME [/data]
# Thu, 07 Sep 2023 02:31:58 GMT
WORKDIR /data
# Thu, 07 Sep 2023 02:31:58 GMT
CMD ["rethinkdb" "--bind" "all"]
# Thu, 07 Sep 2023 02:31:58 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:7d97e254a0461b0a30b3f443f1daa0d620a3cc6ff4e2714cc1cfd96ace5b7a7e`  
		Last Modified: Thu, 07 Sep 2023 00:26:03 GMT  
		Size: 31.4 MB (31417503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bf000f8ac7892a80108ffdf0b2d24e4527090c906a2c7e1506479503c3c474e`  
		Last Modified: Thu, 07 Sep 2023 02:32:11 GMT  
		Size: 6.3 MB (6328993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be61542e7d0740cb47d75238322981f217b4e92a777668fdab6d53692708335e`  
		Last Modified: Thu, 07 Sep 2023 02:32:10 GMT  
		Size: 2.7 KB (2688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b093088dbb50094ef7e02965727f0e68f32052c38cad998dec98a2ffa67f76d`  
		Last Modified: Thu, 07 Sep 2023 02:32:11 GMT  
		Size: 10.2 MB (10236026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d710f4dd3a42844e5cd13df0f622a3dddedb86e15735d2e5eaa9bc811314a39`  
		Last Modified: Thu, 07 Sep 2023 02:32:10 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rethinkdb:bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull rethinkdb@sha256:05d9f68041752e095370754946343203e285e5ebdc87bfc88ce4114bca4bb70a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.0 MB (45963303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a84e2d621c8396c316079a4658171a332b6324259c1191bf42857e0ed02353c`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Thu, 07 Sep 2023 00:39:53 GMT
ADD file:abd1ad48ae3ebec7a6ecc8ce3016c25be2afcbaedfcb904bc89b1ce59400aef0 in / 
# Thu, 07 Sep 2023 00:39:54 GMT
CMD ["bash"]
# Thu, 07 Sep 2023 01:06:22 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 01:06:24 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bullseye bullseye main" > /etc/apt/sources.list.d/rethinkdb.list
# Thu, 07 Sep 2023 01:06:24 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.2~0bullseye
# Thu, 07 Sep 2023 01:06:28 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 01:06:28 GMT
VOLUME [/data]
# Thu, 07 Sep 2023 01:06:28 GMT
WORKDIR /data
# Thu, 07 Sep 2023 01:06:28 GMT
CMD ["rethinkdb" "--bind" "all"]
# Thu, 07 Sep 2023 01:06:29 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:f96ab15157043879c2ff23e0556e798eba6a6ff3d7fd5d1384de223bb9f66f1d`  
		Last Modified: Thu, 07 Sep 2023 00:43:41 GMT  
		Size: 30.1 MB (30062903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c2024adec37dcd958b017656d0e6ad9069b83a2321556e8192eedf29a8eddd8`  
		Last Modified: Thu, 07 Sep 2023 01:07:16 GMT  
		Size: 6.3 MB (6309686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af7a61cca78ff977a27a6a08763860cefa6bd1c14eb191c8b7b0453a0d64489a`  
		Last Modified: Thu, 07 Sep 2023 01:07:18 GMT  
		Size: 2.7 KB (2685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94910e6203c86f7c71c0dbba369901f0a6c7abc04253e850f1ca43e526c678ac`  
		Last Modified: Thu, 07 Sep 2023 01:06:49 GMT  
		Size: 9.6 MB (9587902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e544a911c6057044c798fb4331353fe367c0ad8391eed52dbecfd290f1f42e2`  
		Last Modified: Thu, 07 Sep 2023 01:06:48 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rethinkdb:bullseye-slim` - linux; s390x

```console
$ docker pull rethinkdb@sha256:b34358fbe9b8a0418977d30a4003c29e916e7df2b0930f89970fb0f25aa559a9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45434194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44f69055732c174b03f9bef05cd88c19adc4a68385db32bc1fc1e2ac541a32d7`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 20 Sep 2023 02:54:54 GMT
ADD file:02a97e0d5f41f84ac0284849646284fa41b5e324d24f4d95bb1e2419899da811 in / 
# Wed, 20 Sep 2023 02:54:57 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 10:21:54 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Wed, 20 Sep 2023 10:21:56 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bullseye bullseye main" > /etc/apt/sources.list.d/rethinkdb.list
# Wed, 20 Sep 2023 10:21:56 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.2~0bullseye
# Wed, 20 Sep 2023 10:22:02 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Wed, 20 Sep 2023 10:22:02 GMT
VOLUME [/data]
# Wed, 20 Sep 2023 10:22:02 GMT
WORKDIR /data
# Wed, 20 Sep 2023 10:22:03 GMT
CMD ["rethinkdb" "--bind" "all"]
# Wed, 20 Sep 2023 10:22:03 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:d2d51167e651784cce0bd658d0c2caa328adef8ccf264d8c09860a95bc2a2fc6`  
		Last Modified: Wed, 20 Sep 2023 03:00:22 GMT  
		Size: 29.7 MB (29653129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dea8e75d506a88101e35a004433cbbb4e0d816df67980894c1dee3b99163866`  
		Last Modified: Wed, 20 Sep 2023 10:22:19 GMT  
		Size: 6.2 MB (6205677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e45ad7c29baadc14fbba254ba452aa26197aa54931d84a5106b2153cf5718bf6`  
		Last Modified: Wed, 20 Sep 2023 10:22:18 GMT  
		Size: 2.7 KB (2689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf466c4d897f20b1e3f2dc68b7dd690a2db55c106023ae3799dab9a5745e2823`  
		Last Modified: Wed, 20 Sep 2023 10:22:19 GMT  
		Size: 9.6 MB (9572572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd8866d2ff420286e20a0a3c316cdd2890071c9a1d078ab5c54150b58545cd03`  
		Last Modified: Wed, 20 Sep 2023 10:22:18 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
