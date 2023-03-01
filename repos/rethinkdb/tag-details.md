<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `rethinkdb`

-	[`rethinkdb:2`](#rethinkdb2)
-	[`rethinkdb:2-bullseye-slim`](#rethinkdb2-bullseye-slim)
-	[`rethinkdb:2.4`](#rethinkdb24)
-	[`rethinkdb:2.4-bullseye-slim`](#rethinkdb24-bullseye-slim)
-	[`rethinkdb:2.4.2`](#rethinkdb242)
-	[`rethinkdb:2.4.2-bullseye-slim`](#rethinkdb242-bullseye-slim)
-	[`rethinkdb:bullseye-slim`](#rethinkdbbullseye-slim)
-	[`rethinkdb:latest`](#rethinkdblatest)

## `rethinkdb:2`

```console
$ docker pull rethinkdb@sha256:1c143042b2ef569a17de88460858d8e31b1995bb5b2037e327c72835c8d71fa7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; s390x

### `rethinkdb:2` - linux; amd64

```console
$ docker pull rethinkdb@sha256:2dbb6ac67687cceba82c0ca5a27bb2fb8f009d4a09e24ef6ec8c70699b7ca055
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 MB (47979147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b2054abe542ebda5186b524cd7c460a6fc8bcdee48983d2381c8a9db8ea2831`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Thu, 09 Feb 2023 03:20:20 GMT
ADD file:3ea7c69e4bfac2ebb6f86baaedab31827c86a594dba8080a49928e211ad3c7a0 in / 
# Thu, 09 Feb 2023 03:20:20 GMT
CMD ["bash"]
# Thu, 09 Feb 2023 15:10:10 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 15:10:12 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bullseye bullseye main" > /etc/apt/sources.list.d/rethinkdb.list
# Thu, 09 Feb 2023 15:10:12 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.2~0bullseye
# Thu, 09 Feb 2023 15:10:17 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 15:10:17 GMT
VOLUME [/data]
# Thu, 09 Feb 2023 15:10:17 GMT
WORKDIR /data
# Thu, 09 Feb 2023 15:10:17 GMT
CMD ["rethinkdb" "--bind" "all"]
# Thu, 09 Feb 2023 15:10:18 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:bb263680fed18eecdc67f885094df6f589bafc19004839d7fdf141df236a61aa`  
		Last Modified: Thu, 09 Feb 2023 03:25:13 GMT  
		Size: 31.4 MB (31411810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57029c11986e6ff974b4c2d8d562f67161b8dc124079e47f1fefaad78bbb0f4b`  
		Last Modified: Thu, 09 Feb 2023 15:10:31 GMT  
		Size: 6.3 MB (6328673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13ea04342952726fd06fc1278ee3b7204a829e8d2ea5169aeb678aa5be537fa9`  
		Last Modified: Thu, 09 Feb 2023 15:10:30 GMT  
		Size: 2.7 KB (2689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b575c5df2f1268e21bb1cb192d47dfc8b6af32b507954e8479573395e942779`  
		Last Modified: Thu, 09 Feb 2023 15:10:32 GMT  
		Size: 10.2 MB (10235848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e54280e41e3b061d6ba6dbe2e2573abda62e8985f955421bcba8271d567b7f47`  
		Last Modified: Thu, 09 Feb 2023 15:10:30 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rethinkdb:2` - linux; arm64 variant v8

```console
$ docker pull rethinkdb@sha256:e9f2b3be7f0f748ba5e02d11845ac73e669724f9c2afae919c86829f654fbe8e
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.0 MB (45962661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2305ad2364ef5889a6b8119f927846f55b51f8c7d04904fd4563ea314f646ca3`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Thu, 09 Feb 2023 03:58:40 GMT
ADD file:3276ac85bb957360f20720da5b37498a6b5f91a017046049f8d2fd791f728a9a in / 
# Thu, 09 Feb 2023 03:58:40 GMT
CMD ["bash"]
# Thu, 09 Feb 2023 13:54:19 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 13:54:21 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bullseye bullseye main" > /etc/apt/sources.list.d/rethinkdb.list
# Thu, 09 Feb 2023 13:54:21 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.2~0bullseye
# Thu, 09 Feb 2023 13:54:25 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 13:54:25 GMT
VOLUME [/data]
# Thu, 09 Feb 2023 13:54:26 GMT
WORKDIR /data
# Thu, 09 Feb 2023 13:54:26 GMT
CMD ["rethinkdb" "--bind" "all"]
# Thu, 09 Feb 2023 13:54:26 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:5731adb3a4abcefe78d75783ea6e5ee87c4604d0c6a4f8c00b50085e162a7f5d`  
		Last Modified: Thu, 09 Feb 2023 04:02:34 GMT  
		Size: 30.1 MB (30062509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a07091757195d6cb16b5b79eb81ea4d316d2b35d181af8ac6d0ef51a2ec04965`  
		Last Modified: Thu, 09 Feb 2023 13:54:42 GMT  
		Size: 6.3 MB (6309539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c41c4ea82b84a2dec2b9e81bd31dd129a6dc85e4e66e3afe88d8aad1ce3b2b41`  
		Last Modified: Thu, 09 Feb 2023 13:54:41 GMT  
		Size: 2.7 KB (2688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6e5d7191566285d1072056d80e3f78d3aa9b74efc80e53b6bef5523525ed650`  
		Last Modified: Thu, 09 Feb 2023 13:54:42 GMT  
		Size: 9.6 MB (9587798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4bedaedc3a0a5823cc13f3d2806df3fb069a1012d9708d5f2b8d9cc7558aea4`  
		Last Modified: Thu, 09 Feb 2023 13:54:41 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rethinkdb:2` - linux; s390x

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

## `rethinkdb:2-bullseye-slim`

```console
$ docker pull rethinkdb@sha256:1c143042b2ef569a17de88460858d8e31b1995bb5b2037e327c72835c8d71fa7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; s390x

### `rethinkdb:2-bullseye-slim` - linux; amd64

```console
$ docker pull rethinkdb@sha256:2dbb6ac67687cceba82c0ca5a27bb2fb8f009d4a09e24ef6ec8c70699b7ca055
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 MB (47979147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b2054abe542ebda5186b524cd7c460a6fc8bcdee48983d2381c8a9db8ea2831`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Thu, 09 Feb 2023 03:20:20 GMT
ADD file:3ea7c69e4bfac2ebb6f86baaedab31827c86a594dba8080a49928e211ad3c7a0 in / 
# Thu, 09 Feb 2023 03:20:20 GMT
CMD ["bash"]
# Thu, 09 Feb 2023 15:10:10 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 15:10:12 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bullseye bullseye main" > /etc/apt/sources.list.d/rethinkdb.list
# Thu, 09 Feb 2023 15:10:12 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.2~0bullseye
# Thu, 09 Feb 2023 15:10:17 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 15:10:17 GMT
VOLUME [/data]
# Thu, 09 Feb 2023 15:10:17 GMT
WORKDIR /data
# Thu, 09 Feb 2023 15:10:17 GMT
CMD ["rethinkdb" "--bind" "all"]
# Thu, 09 Feb 2023 15:10:18 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:bb263680fed18eecdc67f885094df6f589bafc19004839d7fdf141df236a61aa`  
		Last Modified: Thu, 09 Feb 2023 03:25:13 GMT  
		Size: 31.4 MB (31411810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57029c11986e6ff974b4c2d8d562f67161b8dc124079e47f1fefaad78bbb0f4b`  
		Last Modified: Thu, 09 Feb 2023 15:10:31 GMT  
		Size: 6.3 MB (6328673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13ea04342952726fd06fc1278ee3b7204a829e8d2ea5169aeb678aa5be537fa9`  
		Last Modified: Thu, 09 Feb 2023 15:10:30 GMT  
		Size: 2.7 KB (2689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b575c5df2f1268e21bb1cb192d47dfc8b6af32b507954e8479573395e942779`  
		Last Modified: Thu, 09 Feb 2023 15:10:32 GMT  
		Size: 10.2 MB (10235848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e54280e41e3b061d6ba6dbe2e2573abda62e8985f955421bcba8271d567b7f47`  
		Last Modified: Thu, 09 Feb 2023 15:10:30 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rethinkdb:2-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull rethinkdb@sha256:e9f2b3be7f0f748ba5e02d11845ac73e669724f9c2afae919c86829f654fbe8e
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.0 MB (45962661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2305ad2364ef5889a6b8119f927846f55b51f8c7d04904fd4563ea314f646ca3`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Thu, 09 Feb 2023 03:58:40 GMT
ADD file:3276ac85bb957360f20720da5b37498a6b5f91a017046049f8d2fd791f728a9a in / 
# Thu, 09 Feb 2023 03:58:40 GMT
CMD ["bash"]
# Thu, 09 Feb 2023 13:54:19 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 13:54:21 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bullseye bullseye main" > /etc/apt/sources.list.d/rethinkdb.list
# Thu, 09 Feb 2023 13:54:21 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.2~0bullseye
# Thu, 09 Feb 2023 13:54:25 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 13:54:25 GMT
VOLUME [/data]
# Thu, 09 Feb 2023 13:54:26 GMT
WORKDIR /data
# Thu, 09 Feb 2023 13:54:26 GMT
CMD ["rethinkdb" "--bind" "all"]
# Thu, 09 Feb 2023 13:54:26 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:5731adb3a4abcefe78d75783ea6e5ee87c4604d0c6a4f8c00b50085e162a7f5d`  
		Last Modified: Thu, 09 Feb 2023 04:02:34 GMT  
		Size: 30.1 MB (30062509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a07091757195d6cb16b5b79eb81ea4d316d2b35d181af8ac6d0ef51a2ec04965`  
		Last Modified: Thu, 09 Feb 2023 13:54:42 GMT  
		Size: 6.3 MB (6309539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c41c4ea82b84a2dec2b9e81bd31dd129a6dc85e4e66e3afe88d8aad1ce3b2b41`  
		Last Modified: Thu, 09 Feb 2023 13:54:41 GMT  
		Size: 2.7 KB (2688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6e5d7191566285d1072056d80e3f78d3aa9b74efc80e53b6bef5523525ed650`  
		Last Modified: Thu, 09 Feb 2023 13:54:42 GMT  
		Size: 9.6 MB (9587798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4bedaedc3a0a5823cc13f3d2806df3fb069a1012d9708d5f2b8d9cc7558aea4`  
		Last Modified: Thu, 09 Feb 2023 13:54:41 GMT  
		Size: 127.0 B  
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

## `rethinkdb:2.4`

```console
$ docker pull rethinkdb@sha256:1c143042b2ef569a17de88460858d8e31b1995bb5b2037e327c72835c8d71fa7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; s390x

### `rethinkdb:2.4` - linux; amd64

```console
$ docker pull rethinkdb@sha256:2dbb6ac67687cceba82c0ca5a27bb2fb8f009d4a09e24ef6ec8c70699b7ca055
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 MB (47979147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b2054abe542ebda5186b524cd7c460a6fc8bcdee48983d2381c8a9db8ea2831`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Thu, 09 Feb 2023 03:20:20 GMT
ADD file:3ea7c69e4bfac2ebb6f86baaedab31827c86a594dba8080a49928e211ad3c7a0 in / 
# Thu, 09 Feb 2023 03:20:20 GMT
CMD ["bash"]
# Thu, 09 Feb 2023 15:10:10 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 15:10:12 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bullseye bullseye main" > /etc/apt/sources.list.d/rethinkdb.list
# Thu, 09 Feb 2023 15:10:12 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.2~0bullseye
# Thu, 09 Feb 2023 15:10:17 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 15:10:17 GMT
VOLUME [/data]
# Thu, 09 Feb 2023 15:10:17 GMT
WORKDIR /data
# Thu, 09 Feb 2023 15:10:17 GMT
CMD ["rethinkdb" "--bind" "all"]
# Thu, 09 Feb 2023 15:10:18 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:bb263680fed18eecdc67f885094df6f589bafc19004839d7fdf141df236a61aa`  
		Last Modified: Thu, 09 Feb 2023 03:25:13 GMT  
		Size: 31.4 MB (31411810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57029c11986e6ff974b4c2d8d562f67161b8dc124079e47f1fefaad78bbb0f4b`  
		Last Modified: Thu, 09 Feb 2023 15:10:31 GMT  
		Size: 6.3 MB (6328673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13ea04342952726fd06fc1278ee3b7204a829e8d2ea5169aeb678aa5be537fa9`  
		Last Modified: Thu, 09 Feb 2023 15:10:30 GMT  
		Size: 2.7 KB (2689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b575c5df2f1268e21bb1cb192d47dfc8b6af32b507954e8479573395e942779`  
		Last Modified: Thu, 09 Feb 2023 15:10:32 GMT  
		Size: 10.2 MB (10235848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e54280e41e3b061d6ba6dbe2e2573abda62e8985f955421bcba8271d567b7f47`  
		Last Modified: Thu, 09 Feb 2023 15:10:30 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rethinkdb:2.4` - linux; arm64 variant v8

```console
$ docker pull rethinkdb@sha256:e9f2b3be7f0f748ba5e02d11845ac73e669724f9c2afae919c86829f654fbe8e
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.0 MB (45962661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2305ad2364ef5889a6b8119f927846f55b51f8c7d04904fd4563ea314f646ca3`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Thu, 09 Feb 2023 03:58:40 GMT
ADD file:3276ac85bb957360f20720da5b37498a6b5f91a017046049f8d2fd791f728a9a in / 
# Thu, 09 Feb 2023 03:58:40 GMT
CMD ["bash"]
# Thu, 09 Feb 2023 13:54:19 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 13:54:21 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bullseye bullseye main" > /etc/apt/sources.list.d/rethinkdb.list
# Thu, 09 Feb 2023 13:54:21 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.2~0bullseye
# Thu, 09 Feb 2023 13:54:25 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 13:54:25 GMT
VOLUME [/data]
# Thu, 09 Feb 2023 13:54:26 GMT
WORKDIR /data
# Thu, 09 Feb 2023 13:54:26 GMT
CMD ["rethinkdb" "--bind" "all"]
# Thu, 09 Feb 2023 13:54:26 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:5731adb3a4abcefe78d75783ea6e5ee87c4604d0c6a4f8c00b50085e162a7f5d`  
		Last Modified: Thu, 09 Feb 2023 04:02:34 GMT  
		Size: 30.1 MB (30062509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a07091757195d6cb16b5b79eb81ea4d316d2b35d181af8ac6d0ef51a2ec04965`  
		Last Modified: Thu, 09 Feb 2023 13:54:42 GMT  
		Size: 6.3 MB (6309539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c41c4ea82b84a2dec2b9e81bd31dd129a6dc85e4e66e3afe88d8aad1ce3b2b41`  
		Last Modified: Thu, 09 Feb 2023 13:54:41 GMT  
		Size: 2.7 KB (2688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6e5d7191566285d1072056d80e3f78d3aa9b74efc80e53b6bef5523525ed650`  
		Last Modified: Thu, 09 Feb 2023 13:54:42 GMT  
		Size: 9.6 MB (9587798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4bedaedc3a0a5823cc13f3d2806df3fb069a1012d9708d5f2b8d9cc7558aea4`  
		Last Modified: Thu, 09 Feb 2023 13:54:41 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rethinkdb:2.4` - linux; s390x

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

## `rethinkdb:2.4-bullseye-slim`

```console
$ docker pull rethinkdb@sha256:1c143042b2ef569a17de88460858d8e31b1995bb5b2037e327c72835c8d71fa7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; s390x

### `rethinkdb:2.4-bullseye-slim` - linux; amd64

```console
$ docker pull rethinkdb@sha256:2dbb6ac67687cceba82c0ca5a27bb2fb8f009d4a09e24ef6ec8c70699b7ca055
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 MB (47979147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b2054abe542ebda5186b524cd7c460a6fc8bcdee48983d2381c8a9db8ea2831`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Thu, 09 Feb 2023 03:20:20 GMT
ADD file:3ea7c69e4bfac2ebb6f86baaedab31827c86a594dba8080a49928e211ad3c7a0 in / 
# Thu, 09 Feb 2023 03:20:20 GMT
CMD ["bash"]
# Thu, 09 Feb 2023 15:10:10 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 15:10:12 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bullseye bullseye main" > /etc/apt/sources.list.d/rethinkdb.list
# Thu, 09 Feb 2023 15:10:12 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.2~0bullseye
# Thu, 09 Feb 2023 15:10:17 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 15:10:17 GMT
VOLUME [/data]
# Thu, 09 Feb 2023 15:10:17 GMT
WORKDIR /data
# Thu, 09 Feb 2023 15:10:17 GMT
CMD ["rethinkdb" "--bind" "all"]
# Thu, 09 Feb 2023 15:10:18 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:bb263680fed18eecdc67f885094df6f589bafc19004839d7fdf141df236a61aa`  
		Last Modified: Thu, 09 Feb 2023 03:25:13 GMT  
		Size: 31.4 MB (31411810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57029c11986e6ff974b4c2d8d562f67161b8dc124079e47f1fefaad78bbb0f4b`  
		Last Modified: Thu, 09 Feb 2023 15:10:31 GMT  
		Size: 6.3 MB (6328673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13ea04342952726fd06fc1278ee3b7204a829e8d2ea5169aeb678aa5be537fa9`  
		Last Modified: Thu, 09 Feb 2023 15:10:30 GMT  
		Size: 2.7 KB (2689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b575c5df2f1268e21bb1cb192d47dfc8b6af32b507954e8479573395e942779`  
		Last Modified: Thu, 09 Feb 2023 15:10:32 GMT  
		Size: 10.2 MB (10235848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e54280e41e3b061d6ba6dbe2e2573abda62e8985f955421bcba8271d567b7f47`  
		Last Modified: Thu, 09 Feb 2023 15:10:30 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rethinkdb:2.4-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull rethinkdb@sha256:e9f2b3be7f0f748ba5e02d11845ac73e669724f9c2afae919c86829f654fbe8e
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.0 MB (45962661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2305ad2364ef5889a6b8119f927846f55b51f8c7d04904fd4563ea314f646ca3`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Thu, 09 Feb 2023 03:58:40 GMT
ADD file:3276ac85bb957360f20720da5b37498a6b5f91a017046049f8d2fd791f728a9a in / 
# Thu, 09 Feb 2023 03:58:40 GMT
CMD ["bash"]
# Thu, 09 Feb 2023 13:54:19 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 13:54:21 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bullseye bullseye main" > /etc/apt/sources.list.d/rethinkdb.list
# Thu, 09 Feb 2023 13:54:21 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.2~0bullseye
# Thu, 09 Feb 2023 13:54:25 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 13:54:25 GMT
VOLUME [/data]
# Thu, 09 Feb 2023 13:54:26 GMT
WORKDIR /data
# Thu, 09 Feb 2023 13:54:26 GMT
CMD ["rethinkdb" "--bind" "all"]
# Thu, 09 Feb 2023 13:54:26 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:5731adb3a4abcefe78d75783ea6e5ee87c4604d0c6a4f8c00b50085e162a7f5d`  
		Last Modified: Thu, 09 Feb 2023 04:02:34 GMT  
		Size: 30.1 MB (30062509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a07091757195d6cb16b5b79eb81ea4d316d2b35d181af8ac6d0ef51a2ec04965`  
		Last Modified: Thu, 09 Feb 2023 13:54:42 GMT  
		Size: 6.3 MB (6309539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c41c4ea82b84a2dec2b9e81bd31dd129a6dc85e4e66e3afe88d8aad1ce3b2b41`  
		Last Modified: Thu, 09 Feb 2023 13:54:41 GMT  
		Size: 2.7 KB (2688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6e5d7191566285d1072056d80e3f78d3aa9b74efc80e53b6bef5523525ed650`  
		Last Modified: Thu, 09 Feb 2023 13:54:42 GMT  
		Size: 9.6 MB (9587798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4bedaedc3a0a5823cc13f3d2806df3fb069a1012d9708d5f2b8d9cc7558aea4`  
		Last Modified: Thu, 09 Feb 2023 13:54:41 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rethinkdb:2.4-bullseye-slim` - linux; s390x

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

## `rethinkdb:2.4.2`

```console
$ docker pull rethinkdb@sha256:1c143042b2ef569a17de88460858d8e31b1995bb5b2037e327c72835c8d71fa7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; s390x

### `rethinkdb:2.4.2` - linux; amd64

```console
$ docker pull rethinkdb@sha256:2dbb6ac67687cceba82c0ca5a27bb2fb8f009d4a09e24ef6ec8c70699b7ca055
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 MB (47979147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b2054abe542ebda5186b524cd7c460a6fc8bcdee48983d2381c8a9db8ea2831`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Thu, 09 Feb 2023 03:20:20 GMT
ADD file:3ea7c69e4bfac2ebb6f86baaedab31827c86a594dba8080a49928e211ad3c7a0 in / 
# Thu, 09 Feb 2023 03:20:20 GMT
CMD ["bash"]
# Thu, 09 Feb 2023 15:10:10 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 15:10:12 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bullseye bullseye main" > /etc/apt/sources.list.d/rethinkdb.list
# Thu, 09 Feb 2023 15:10:12 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.2~0bullseye
# Thu, 09 Feb 2023 15:10:17 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 15:10:17 GMT
VOLUME [/data]
# Thu, 09 Feb 2023 15:10:17 GMT
WORKDIR /data
# Thu, 09 Feb 2023 15:10:17 GMT
CMD ["rethinkdb" "--bind" "all"]
# Thu, 09 Feb 2023 15:10:18 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:bb263680fed18eecdc67f885094df6f589bafc19004839d7fdf141df236a61aa`  
		Last Modified: Thu, 09 Feb 2023 03:25:13 GMT  
		Size: 31.4 MB (31411810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57029c11986e6ff974b4c2d8d562f67161b8dc124079e47f1fefaad78bbb0f4b`  
		Last Modified: Thu, 09 Feb 2023 15:10:31 GMT  
		Size: 6.3 MB (6328673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13ea04342952726fd06fc1278ee3b7204a829e8d2ea5169aeb678aa5be537fa9`  
		Last Modified: Thu, 09 Feb 2023 15:10:30 GMT  
		Size: 2.7 KB (2689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b575c5df2f1268e21bb1cb192d47dfc8b6af32b507954e8479573395e942779`  
		Last Modified: Thu, 09 Feb 2023 15:10:32 GMT  
		Size: 10.2 MB (10235848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e54280e41e3b061d6ba6dbe2e2573abda62e8985f955421bcba8271d567b7f47`  
		Last Modified: Thu, 09 Feb 2023 15:10:30 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rethinkdb:2.4.2` - linux; arm64 variant v8

```console
$ docker pull rethinkdb@sha256:e9f2b3be7f0f748ba5e02d11845ac73e669724f9c2afae919c86829f654fbe8e
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.0 MB (45962661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2305ad2364ef5889a6b8119f927846f55b51f8c7d04904fd4563ea314f646ca3`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Thu, 09 Feb 2023 03:58:40 GMT
ADD file:3276ac85bb957360f20720da5b37498a6b5f91a017046049f8d2fd791f728a9a in / 
# Thu, 09 Feb 2023 03:58:40 GMT
CMD ["bash"]
# Thu, 09 Feb 2023 13:54:19 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 13:54:21 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bullseye bullseye main" > /etc/apt/sources.list.d/rethinkdb.list
# Thu, 09 Feb 2023 13:54:21 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.2~0bullseye
# Thu, 09 Feb 2023 13:54:25 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 13:54:25 GMT
VOLUME [/data]
# Thu, 09 Feb 2023 13:54:26 GMT
WORKDIR /data
# Thu, 09 Feb 2023 13:54:26 GMT
CMD ["rethinkdb" "--bind" "all"]
# Thu, 09 Feb 2023 13:54:26 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:5731adb3a4abcefe78d75783ea6e5ee87c4604d0c6a4f8c00b50085e162a7f5d`  
		Last Modified: Thu, 09 Feb 2023 04:02:34 GMT  
		Size: 30.1 MB (30062509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a07091757195d6cb16b5b79eb81ea4d316d2b35d181af8ac6d0ef51a2ec04965`  
		Last Modified: Thu, 09 Feb 2023 13:54:42 GMT  
		Size: 6.3 MB (6309539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c41c4ea82b84a2dec2b9e81bd31dd129a6dc85e4e66e3afe88d8aad1ce3b2b41`  
		Last Modified: Thu, 09 Feb 2023 13:54:41 GMT  
		Size: 2.7 KB (2688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6e5d7191566285d1072056d80e3f78d3aa9b74efc80e53b6bef5523525ed650`  
		Last Modified: Thu, 09 Feb 2023 13:54:42 GMT  
		Size: 9.6 MB (9587798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4bedaedc3a0a5823cc13f3d2806df3fb069a1012d9708d5f2b8d9cc7558aea4`  
		Last Modified: Thu, 09 Feb 2023 13:54:41 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rethinkdb:2.4.2` - linux; s390x

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

## `rethinkdb:2.4.2-bullseye-slim`

```console
$ docker pull rethinkdb@sha256:1c143042b2ef569a17de88460858d8e31b1995bb5b2037e327c72835c8d71fa7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; s390x

### `rethinkdb:2.4.2-bullseye-slim` - linux; amd64

```console
$ docker pull rethinkdb@sha256:2dbb6ac67687cceba82c0ca5a27bb2fb8f009d4a09e24ef6ec8c70699b7ca055
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 MB (47979147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b2054abe542ebda5186b524cd7c460a6fc8bcdee48983d2381c8a9db8ea2831`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Thu, 09 Feb 2023 03:20:20 GMT
ADD file:3ea7c69e4bfac2ebb6f86baaedab31827c86a594dba8080a49928e211ad3c7a0 in / 
# Thu, 09 Feb 2023 03:20:20 GMT
CMD ["bash"]
# Thu, 09 Feb 2023 15:10:10 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 15:10:12 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bullseye bullseye main" > /etc/apt/sources.list.d/rethinkdb.list
# Thu, 09 Feb 2023 15:10:12 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.2~0bullseye
# Thu, 09 Feb 2023 15:10:17 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 15:10:17 GMT
VOLUME [/data]
# Thu, 09 Feb 2023 15:10:17 GMT
WORKDIR /data
# Thu, 09 Feb 2023 15:10:17 GMT
CMD ["rethinkdb" "--bind" "all"]
# Thu, 09 Feb 2023 15:10:18 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:bb263680fed18eecdc67f885094df6f589bafc19004839d7fdf141df236a61aa`  
		Last Modified: Thu, 09 Feb 2023 03:25:13 GMT  
		Size: 31.4 MB (31411810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57029c11986e6ff974b4c2d8d562f67161b8dc124079e47f1fefaad78bbb0f4b`  
		Last Modified: Thu, 09 Feb 2023 15:10:31 GMT  
		Size: 6.3 MB (6328673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13ea04342952726fd06fc1278ee3b7204a829e8d2ea5169aeb678aa5be537fa9`  
		Last Modified: Thu, 09 Feb 2023 15:10:30 GMT  
		Size: 2.7 KB (2689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b575c5df2f1268e21bb1cb192d47dfc8b6af32b507954e8479573395e942779`  
		Last Modified: Thu, 09 Feb 2023 15:10:32 GMT  
		Size: 10.2 MB (10235848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e54280e41e3b061d6ba6dbe2e2573abda62e8985f955421bcba8271d567b7f47`  
		Last Modified: Thu, 09 Feb 2023 15:10:30 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rethinkdb:2.4.2-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull rethinkdb@sha256:e9f2b3be7f0f748ba5e02d11845ac73e669724f9c2afae919c86829f654fbe8e
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.0 MB (45962661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2305ad2364ef5889a6b8119f927846f55b51f8c7d04904fd4563ea314f646ca3`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Thu, 09 Feb 2023 03:58:40 GMT
ADD file:3276ac85bb957360f20720da5b37498a6b5f91a017046049f8d2fd791f728a9a in / 
# Thu, 09 Feb 2023 03:58:40 GMT
CMD ["bash"]
# Thu, 09 Feb 2023 13:54:19 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 13:54:21 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bullseye bullseye main" > /etc/apt/sources.list.d/rethinkdb.list
# Thu, 09 Feb 2023 13:54:21 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.2~0bullseye
# Thu, 09 Feb 2023 13:54:25 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 13:54:25 GMT
VOLUME [/data]
# Thu, 09 Feb 2023 13:54:26 GMT
WORKDIR /data
# Thu, 09 Feb 2023 13:54:26 GMT
CMD ["rethinkdb" "--bind" "all"]
# Thu, 09 Feb 2023 13:54:26 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:5731adb3a4abcefe78d75783ea6e5ee87c4604d0c6a4f8c00b50085e162a7f5d`  
		Last Modified: Thu, 09 Feb 2023 04:02:34 GMT  
		Size: 30.1 MB (30062509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a07091757195d6cb16b5b79eb81ea4d316d2b35d181af8ac6d0ef51a2ec04965`  
		Last Modified: Thu, 09 Feb 2023 13:54:42 GMT  
		Size: 6.3 MB (6309539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c41c4ea82b84a2dec2b9e81bd31dd129a6dc85e4e66e3afe88d8aad1ce3b2b41`  
		Last Modified: Thu, 09 Feb 2023 13:54:41 GMT  
		Size: 2.7 KB (2688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6e5d7191566285d1072056d80e3f78d3aa9b74efc80e53b6bef5523525ed650`  
		Last Modified: Thu, 09 Feb 2023 13:54:42 GMT  
		Size: 9.6 MB (9587798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4bedaedc3a0a5823cc13f3d2806df3fb069a1012d9708d5f2b8d9cc7558aea4`  
		Last Modified: Thu, 09 Feb 2023 13:54:41 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rethinkdb:2.4.2-bullseye-slim` - linux; s390x

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

## `rethinkdb:bullseye-slim`

```console
$ docker pull rethinkdb@sha256:1c143042b2ef569a17de88460858d8e31b1995bb5b2037e327c72835c8d71fa7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; s390x

### `rethinkdb:bullseye-slim` - linux; amd64

```console
$ docker pull rethinkdb@sha256:2dbb6ac67687cceba82c0ca5a27bb2fb8f009d4a09e24ef6ec8c70699b7ca055
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 MB (47979147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b2054abe542ebda5186b524cd7c460a6fc8bcdee48983d2381c8a9db8ea2831`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Thu, 09 Feb 2023 03:20:20 GMT
ADD file:3ea7c69e4bfac2ebb6f86baaedab31827c86a594dba8080a49928e211ad3c7a0 in / 
# Thu, 09 Feb 2023 03:20:20 GMT
CMD ["bash"]
# Thu, 09 Feb 2023 15:10:10 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 15:10:12 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bullseye bullseye main" > /etc/apt/sources.list.d/rethinkdb.list
# Thu, 09 Feb 2023 15:10:12 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.2~0bullseye
# Thu, 09 Feb 2023 15:10:17 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 15:10:17 GMT
VOLUME [/data]
# Thu, 09 Feb 2023 15:10:17 GMT
WORKDIR /data
# Thu, 09 Feb 2023 15:10:17 GMT
CMD ["rethinkdb" "--bind" "all"]
# Thu, 09 Feb 2023 15:10:18 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:bb263680fed18eecdc67f885094df6f589bafc19004839d7fdf141df236a61aa`  
		Last Modified: Thu, 09 Feb 2023 03:25:13 GMT  
		Size: 31.4 MB (31411810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57029c11986e6ff974b4c2d8d562f67161b8dc124079e47f1fefaad78bbb0f4b`  
		Last Modified: Thu, 09 Feb 2023 15:10:31 GMT  
		Size: 6.3 MB (6328673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13ea04342952726fd06fc1278ee3b7204a829e8d2ea5169aeb678aa5be537fa9`  
		Last Modified: Thu, 09 Feb 2023 15:10:30 GMT  
		Size: 2.7 KB (2689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b575c5df2f1268e21bb1cb192d47dfc8b6af32b507954e8479573395e942779`  
		Last Modified: Thu, 09 Feb 2023 15:10:32 GMT  
		Size: 10.2 MB (10235848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e54280e41e3b061d6ba6dbe2e2573abda62e8985f955421bcba8271d567b7f47`  
		Last Modified: Thu, 09 Feb 2023 15:10:30 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rethinkdb:bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull rethinkdb@sha256:e9f2b3be7f0f748ba5e02d11845ac73e669724f9c2afae919c86829f654fbe8e
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.0 MB (45962661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2305ad2364ef5889a6b8119f927846f55b51f8c7d04904fd4563ea314f646ca3`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Thu, 09 Feb 2023 03:58:40 GMT
ADD file:3276ac85bb957360f20720da5b37498a6b5f91a017046049f8d2fd791f728a9a in / 
# Thu, 09 Feb 2023 03:58:40 GMT
CMD ["bash"]
# Thu, 09 Feb 2023 13:54:19 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 13:54:21 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bullseye bullseye main" > /etc/apt/sources.list.d/rethinkdb.list
# Thu, 09 Feb 2023 13:54:21 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.2~0bullseye
# Thu, 09 Feb 2023 13:54:25 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 13:54:25 GMT
VOLUME [/data]
# Thu, 09 Feb 2023 13:54:26 GMT
WORKDIR /data
# Thu, 09 Feb 2023 13:54:26 GMT
CMD ["rethinkdb" "--bind" "all"]
# Thu, 09 Feb 2023 13:54:26 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:5731adb3a4abcefe78d75783ea6e5ee87c4604d0c6a4f8c00b50085e162a7f5d`  
		Last Modified: Thu, 09 Feb 2023 04:02:34 GMT  
		Size: 30.1 MB (30062509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a07091757195d6cb16b5b79eb81ea4d316d2b35d181af8ac6d0ef51a2ec04965`  
		Last Modified: Thu, 09 Feb 2023 13:54:42 GMT  
		Size: 6.3 MB (6309539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c41c4ea82b84a2dec2b9e81bd31dd129a6dc85e4e66e3afe88d8aad1ce3b2b41`  
		Last Modified: Thu, 09 Feb 2023 13:54:41 GMT  
		Size: 2.7 KB (2688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6e5d7191566285d1072056d80e3f78d3aa9b74efc80e53b6bef5523525ed650`  
		Last Modified: Thu, 09 Feb 2023 13:54:42 GMT  
		Size: 9.6 MB (9587798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4bedaedc3a0a5823cc13f3d2806df3fb069a1012d9708d5f2b8d9cc7558aea4`  
		Last Modified: Thu, 09 Feb 2023 13:54:41 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rethinkdb:bullseye-slim` - linux; s390x

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

## `rethinkdb:latest`

```console
$ docker pull rethinkdb@sha256:1c143042b2ef569a17de88460858d8e31b1995bb5b2037e327c72835c8d71fa7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; s390x

### `rethinkdb:latest` - linux; amd64

```console
$ docker pull rethinkdb@sha256:2dbb6ac67687cceba82c0ca5a27bb2fb8f009d4a09e24ef6ec8c70699b7ca055
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 MB (47979147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b2054abe542ebda5186b524cd7c460a6fc8bcdee48983d2381c8a9db8ea2831`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Thu, 09 Feb 2023 03:20:20 GMT
ADD file:3ea7c69e4bfac2ebb6f86baaedab31827c86a594dba8080a49928e211ad3c7a0 in / 
# Thu, 09 Feb 2023 03:20:20 GMT
CMD ["bash"]
# Thu, 09 Feb 2023 15:10:10 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 15:10:12 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bullseye bullseye main" > /etc/apt/sources.list.d/rethinkdb.list
# Thu, 09 Feb 2023 15:10:12 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.2~0bullseye
# Thu, 09 Feb 2023 15:10:17 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 15:10:17 GMT
VOLUME [/data]
# Thu, 09 Feb 2023 15:10:17 GMT
WORKDIR /data
# Thu, 09 Feb 2023 15:10:17 GMT
CMD ["rethinkdb" "--bind" "all"]
# Thu, 09 Feb 2023 15:10:18 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:bb263680fed18eecdc67f885094df6f589bafc19004839d7fdf141df236a61aa`  
		Last Modified: Thu, 09 Feb 2023 03:25:13 GMT  
		Size: 31.4 MB (31411810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57029c11986e6ff974b4c2d8d562f67161b8dc124079e47f1fefaad78bbb0f4b`  
		Last Modified: Thu, 09 Feb 2023 15:10:31 GMT  
		Size: 6.3 MB (6328673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13ea04342952726fd06fc1278ee3b7204a829e8d2ea5169aeb678aa5be537fa9`  
		Last Modified: Thu, 09 Feb 2023 15:10:30 GMT  
		Size: 2.7 KB (2689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b575c5df2f1268e21bb1cb192d47dfc8b6af32b507954e8479573395e942779`  
		Last Modified: Thu, 09 Feb 2023 15:10:32 GMT  
		Size: 10.2 MB (10235848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e54280e41e3b061d6ba6dbe2e2573abda62e8985f955421bcba8271d567b7f47`  
		Last Modified: Thu, 09 Feb 2023 15:10:30 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rethinkdb:latest` - linux; arm64 variant v8

```console
$ docker pull rethinkdb@sha256:e9f2b3be7f0f748ba5e02d11845ac73e669724f9c2afae919c86829f654fbe8e
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.0 MB (45962661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2305ad2364ef5889a6b8119f927846f55b51f8c7d04904fd4563ea314f646ca3`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Thu, 09 Feb 2023 03:58:40 GMT
ADD file:3276ac85bb957360f20720da5b37498a6b5f91a017046049f8d2fd791f728a9a in / 
# Thu, 09 Feb 2023 03:58:40 GMT
CMD ["bash"]
# Thu, 09 Feb 2023 13:54:19 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 13:54:21 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bullseye bullseye main" > /etc/apt/sources.list.d/rethinkdb.list
# Thu, 09 Feb 2023 13:54:21 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.2~0bullseye
# Thu, 09 Feb 2023 13:54:25 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 13:54:25 GMT
VOLUME [/data]
# Thu, 09 Feb 2023 13:54:26 GMT
WORKDIR /data
# Thu, 09 Feb 2023 13:54:26 GMT
CMD ["rethinkdb" "--bind" "all"]
# Thu, 09 Feb 2023 13:54:26 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:5731adb3a4abcefe78d75783ea6e5ee87c4604d0c6a4f8c00b50085e162a7f5d`  
		Last Modified: Thu, 09 Feb 2023 04:02:34 GMT  
		Size: 30.1 MB (30062509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a07091757195d6cb16b5b79eb81ea4d316d2b35d181af8ac6d0ef51a2ec04965`  
		Last Modified: Thu, 09 Feb 2023 13:54:42 GMT  
		Size: 6.3 MB (6309539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c41c4ea82b84a2dec2b9e81bd31dd129a6dc85e4e66e3afe88d8aad1ce3b2b41`  
		Last Modified: Thu, 09 Feb 2023 13:54:41 GMT  
		Size: 2.7 KB (2688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6e5d7191566285d1072056d80e3f78d3aa9b74efc80e53b6bef5523525ed650`  
		Last Modified: Thu, 09 Feb 2023 13:54:42 GMT  
		Size: 9.6 MB (9587798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4bedaedc3a0a5823cc13f3d2806df3fb069a1012d9708d5f2b8d9cc7558aea4`  
		Last Modified: Thu, 09 Feb 2023 13:54:41 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rethinkdb:latest` - linux; s390x

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
