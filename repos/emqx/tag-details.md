<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `emqx`

-	[`emqx:5`](#emqx5)
-	[`emqx:5.1`](#emqx51)
-	[`emqx:5.1.6`](#emqx516)
-	[`emqx:5.2`](#emqx52)
-	[`emqx:5.2.1`](#emqx521)
-	[`emqx:5.3`](#emqx53)
-	[`emqx:5.3.2`](#emqx532)
-	[`emqx:5.4`](#emqx54)
-	[`emqx:5.4.1`](#emqx541)
-	[`emqx:5.5`](#emqx55)
-	[`emqx:5.5.1`](#emqx551)
-	[`emqx:5.6`](#emqx56)
-	[`emqx:5.6.1`](#emqx561)
-	[`emqx:5.7`](#emqx57)
-	[`emqx:5.7.1`](#emqx571)
-	[`emqx:latest`](#emqxlatest)

## `emqx:5`

```console
$ docker pull emqx@sha256:309c87aeb41c7da427f44925e91df25d2db88187639579030e224eb03c1187d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5` - linux; amd64

```console
$ docker pull emqx@sha256:23e00db6e6be310c552badbbfef8cad44b8045960b37b2e1169e4aaaefd85121
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.3 MB (126268671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c261fa69f19b02951b5f77db322c55c9dc76d58d6d0be69340a0f6c842665ad`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Thu, 13 Jun 2024 01:20:56 GMT
ADD file:5f9954090af042b377ea0d1d184faa64d2e9d4c946b6c3898d52aff47e764056 in / 
# Thu, 13 Jun 2024 01:20:56 GMT
CMD ["bash"]
# Thu, 27 Jun 2024 18:19:48 GMT
ENV EMQX_VERSION=5.7.1
# Thu, 27 Jun 2024 18:19:48 GMT
ENV AMD64_SHA256=6896263e24c1211fea0e15464afb39931e9b4c7139804e0a6fb5f143826efaf8
# Thu, 27 Jun 2024 18:19:48 GMT
ENV ARM64_SHA256=c321477bab28e381a472761c2d62f9e5acf6290f298f5aaf9404ab70feb6d587
# Thu, 27 Jun 2024 18:19:48 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Thu, 27 Jun 2024 18:20:07 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 27 Jun 2024 18:20:08 GMT
WORKDIR /opt/emqx
# Thu, 27 Jun 2024 18:20:08 GMT
USER emqx
# Thu, 27 Jun 2024 18:20:08 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Thu, 27 Jun 2024 18:20:08 GMT
EXPOSE 18083 1883 4370 5369 8083 8084 8883
# Thu, 27 Jun 2024 18:20:08 GMT
COPY file:f0e3faa715cc7e845bbdf3b121a4a8bad40d65e5cef1fac9f1285fec250cedf2 in /usr/bin/ 
# Thu, 27 Jun 2024 18:20:08 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Thu, 27 Jun 2024 18:20:09 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:2cc3ae149d28a36d28d4eefbae70aaa14a0c9eab588c3790f7979f310b893c44`  
		Last Modified: Thu, 13 Jun 2024 01:25:30 GMT  
		Size: 29.2 MB (29150430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21ada3da96cf914860b0103cd485748be41d637b09bc8853d126f0d98d845ff8`  
		Last Modified: Thu, 27 Jun 2024 18:20:39 GMT  
		Size: 97.1 MB (97117207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87b3cc76375fdf61e1a6705fe7f358029a6939ceb7a97e8f6255bf7a037696d6`  
		Last Modified: Thu, 27 Jun 2024 18:20:30 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:5` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:43649a68514edd13ed29eaf28634e3c6cb668c6ef74cc43acc91c44e01bf706b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.8 MB (122818365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffc506dce6f9e4989d8a088171e08078e39628702aff7e4d2ccd33279fda1287`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 02 Jul 2024 00:39:37 GMT
ADD file:cbda549b25cd4337cd3ce345e3b66c0d3b43c247d7315906a028f98a56c41f1d in / 
# Tue, 02 Jul 2024 00:39:37 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 04:07:44 GMT
ENV EMQX_VERSION=5.7.1
# Tue, 02 Jul 2024 04:07:44 GMT
ENV AMD64_SHA256=6896263e24c1211fea0e15464afb39931e9b4c7139804e0a6fb5f143826efaf8
# Tue, 02 Jul 2024 04:07:44 GMT
ENV ARM64_SHA256=c321477bab28e381a472761c2d62f9e5acf6290f298f5aaf9404ab70feb6d587
# Tue, 02 Jul 2024 04:07:44 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 02 Jul 2024 04:07:58 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Tue, 02 Jul 2024 04:07:59 GMT
WORKDIR /opt/emqx
# Tue, 02 Jul 2024 04:07:59 GMT
USER emqx
# Tue, 02 Jul 2024 04:07:59 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 02 Jul 2024 04:07:59 GMT
EXPOSE 18083 1883 4370 5369 8083 8084 8883
# Tue, 02 Jul 2024 04:07:59 GMT
COPY file:f0e3faa715cc7e845bbdf3b121a4a8bad40d65e5cef1fac9f1285fec250cedf2 in /usr/bin/ 
# Tue, 02 Jul 2024 04:08:00 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 02 Jul 2024 04:08:00 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:ea235d1ccf77ca07a545b448996766dc3eca4b971b04ba39d50af69660b25751`  
		Last Modified: Tue, 02 Jul 2024 00:42:25 GMT  
		Size: 29.2 MB (29156563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51c44934ae8ca03950296a4539a08b216eef45c351b694b9232d93161d83368e`  
		Last Modified: Tue, 02 Jul 2024 04:09:48 GMT  
		Size: 93.7 MB (93660768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa2ba6b94a2eb3de1a86a522cc9e627fe013fcaff6ff730bb4f6828ab2b51dba`  
		Last Modified: Tue, 02 Jul 2024 04:09:40 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:5.1`

```console
$ docker pull emqx@sha256:cc320a0bf02ecae102da9d543a515ffe1246154f3120c7faef1de5b84350d471
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5.1` - linux; amd64

```console
$ docker pull emqx@sha256:0ac4a63a824d5a26a7236849625ede3963d5ace578ba4d777b2b0b476cfb8475
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.4 MB (102409713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34059ceb56f8b35b0b4030b18ecd7347497378b7527dd8a5ef0ea0a4411114a9`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Thu, 13 Jun 2024 01:21:18 GMT
ADD file:574b112227f85a83f5d80d2523398640537475d2a56fa4c622397c466c0b552b in / 
# Thu, 13 Jun 2024 01:21:18 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 03:54:57 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 03:54:57 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Thu, 13 Jun 2024 03:54:57 GMT
ENV EMQX_VERSION=5.1.6
# Thu, 13 Jun 2024 03:54:57 GMT
ENV AMD64_SHA256=5c65f7538141e93d71d1dd7d088589339ef6a091b90f901604a2e0e004f5f4aa
# Thu, 13 Jun 2024 03:54:58 GMT
ENV ARM64_SHA256=ae832d29d6b4e7fa43f3bf04c8c9fad4c9047f079d1587d3ed2a3564d5ea8147
# Thu, 13 Jun 2024 03:54:58 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Thu, 13 Jun 2024 03:55:04 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg
# Thu, 13 Jun 2024 03:55:05 GMT
WORKDIR /opt/emqx
# Thu, 13 Jun 2024 03:55:05 GMT
USER emqx
# Thu, 13 Jun 2024 03:55:05 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Thu, 13 Jun 2024 03:55:05 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Thu, 13 Jun 2024 03:55:05 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Thu, 13 Jun 2024 03:55:05 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Thu, 13 Jun 2024 03:55:06 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:f7b75fe1f735933f47315080637abf01f87962d47f8636a07ff4535ed7a4a133`  
		Last Modified: Thu, 13 Jun 2024 01:26:15 GMT  
		Size: 31.4 MB (31434040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0d97c40610f645bb9b7ce3c4d91e09363548276037a4e32cec57edf951b79ff`  
		Last Modified: Thu, 13 Jun 2024 03:57:29 GMT  
		Size: 3.0 MB (2989397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a74c2117dfa04f910ded7dff6bc29f1a2fede6411a728f5884b659a1a3e4de05`  
		Last Modified: Thu, 13 Jun 2024 03:57:28 GMT  
		Size: 4.1 KB (4082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1615680af1641fe3fafb198a90d6db1b4beac23db01cee1a8e949b804d4ec0e7`  
		Last Modified: Thu, 13 Jun 2024 03:57:36 GMT  
		Size: 68.0 MB (67981292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f7471981042bc9e59d4560557ae2800fbcc56e140bcb38260273163127ac935`  
		Last Modified: Thu, 13 Jun 2024 03:57:28 GMT  
		Size: 902.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:5.1` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:9faf82efec5c3d29bcdb3865da55f2ec3700b32d843c7bf7820050bb0a1d58cb
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.7 MB (92703799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1fb305f5fa0e596849e693493318c5c935a1cc19b44564acd83ecd316e000b8`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 02 Jul 2024 00:39:52 GMT
ADD file:17d80cdc7d7b37786a32ac4e261c7d17cd4d80248ae39f9574ab5a6bf6a2707c in / 
# Tue, 02 Jul 2024 00:39:52 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 04:06:13 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 04:06:13 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Tue, 02 Jul 2024 04:06:13 GMT
ENV EMQX_VERSION=5.1.6
# Tue, 02 Jul 2024 04:06:13 GMT
ENV AMD64_SHA256=5c65f7538141e93d71d1dd7d088589339ef6a091b90f901604a2e0e004f5f4aa
# Tue, 02 Jul 2024 04:06:13 GMT
ENV ARM64_SHA256=ae832d29d6b4e7fa43f3bf04c8c9fad4c9047f079d1587d3ed2a3564d5ea8147
# Tue, 02 Jul 2024 04:06:14 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 02 Jul 2024 04:06:20 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg
# Tue, 02 Jul 2024 04:06:20 GMT
WORKDIR /opt/emqx
# Tue, 02 Jul 2024 04:06:21 GMT
USER emqx
# Tue, 02 Jul 2024 04:06:21 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 02 Jul 2024 04:06:21 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Tue, 02 Jul 2024 04:06:21 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Tue, 02 Jul 2024 04:06:21 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 02 Jul 2024 04:06:21 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:d13ad33c16eef01d20d5563bfb2ec4f25c0d12699b40cdab418e47b88d2f02e2`  
		Last Modified: Tue, 02 Jul 2024 00:43:04 GMT  
		Size: 30.1 MB (30069615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50ed1ead68b106555b7702cd67bfea91393035db82f1d2956e66bea5aa76d884`  
		Last Modified: Tue, 02 Jul 2024 04:08:18 GMT  
		Size: 3.0 MB (3004478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a092beb378b5f70dd4caa7f309fa4fd36df42994aab6816acbe43742814405cb`  
		Last Modified: Tue, 02 Jul 2024 04:08:17 GMT  
		Size: 4.1 KB (4081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f4f8062829dc895f30b38782ce3cd38d0658e5e89e23a6621ebd9843deaa754`  
		Last Modified: Tue, 02 Jul 2024 04:08:22 GMT  
		Size: 59.6 MB (59624724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daa4e633320795188232ffc346fe8f099a282fb31879e5a9c1a1b428e9d727a1`  
		Last Modified: Tue, 02 Jul 2024 04:08:17 GMT  
		Size: 901.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:5.1.6`

```console
$ docker pull emqx@sha256:cc320a0bf02ecae102da9d543a515ffe1246154f3120c7faef1de5b84350d471
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5.1.6` - linux; amd64

```console
$ docker pull emqx@sha256:0ac4a63a824d5a26a7236849625ede3963d5ace578ba4d777b2b0b476cfb8475
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.4 MB (102409713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34059ceb56f8b35b0b4030b18ecd7347497378b7527dd8a5ef0ea0a4411114a9`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Thu, 13 Jun 2024 01:21:18 GMT
ADD file:574b112227f85a83f5d80d2523398640537475d2a56fa4c622397c466c0b552b in / 
# Thu, 13 Jun 2024 01:21:18 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 03:54:57 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 03:54:57 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Thu, 13 Jun 2024 03:54:57 GMT
ENV EMQX_VERSION=5.1.6
# Thu, 13 Jun 2024 03:54:57 GMT
ENV AMD64_SHA256=5c65f7538141e93d71d1dd7d088589339ef6a091b90f901604a2e0e004f5f4aa
# Thu, 13 Jun 2024 03:54:58 GMT
ENV ARM64_SHA256=ae832d29d6b4e7fa43f3bf04c8c9fad4c9047f079d1587d3ed2a3564d5ea8147
# Thu, 13 Jun 2024 03:54:58 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Thu, 13 Jun 2024 03:55:04 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg
# Thu, 13 Jun 2024 03:55:05 GMT
WORKDIR /opt/emqx
# Thu, 13 Jun 2024 03:55:05 GMT
USER emqx
# Thu, 13 Jun 2024 03:55:05 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Thu, 13 Jun 2024 03:55:05 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Thu, 13 Jun 2024 03:55:05 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Thu, 13 Jun 2024 03:55:05 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Thu, 13 Jun 2024 03:55:06 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:f7b75fe1f735933f47315080637abf01f87962d47f8636a07ff4535ed7a4a133`  
		Last Modified: Thu, 13 Jun 2024 01:26:15 GMT  
		Size: 31.4 MB (31434040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0d97c40610f645bb9b7ce3c4d91e09363548276037a4e32cec57edf951b79ff`  
		Last Modified: Thu, 13 Jun 2024 03:57:29 GMT  
		Size: 3.0 MB (2989397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a74c2117dfa04f910ded7dff6bc29f1a2fede6411a728f5884b659a1a3e4de05`  
		Last Modified: Thu, 13 Jun 2024 03:57:28 GMT  
		Size: 4.1 KB (4082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1615680af1641fe3fafb198a90d6db1b4beac23db01cee1a8e949b804d4ec0e7`  
		Last Modified: Thu, 13 Jun 2024 03:57:36 GMT  
		Size: 68.0 MB (67981292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f7471981042bc9e59d4560557ae2800fbcc56e140bcb38260273163127ac935`  
		Last Modified: Thu, 13 Jun 2024 03:57:28 GMT  
		Size: 902.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:5.1.6` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:9faf82efec5c3d29bcdb3865da55f2ec3700b32d843c7bf7820050bb0a1d58cb
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.7 MB (92703799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1fb305f5fa0e596849e693493318c5c935a1cc19b44564acd83ecd316e000b8`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 02 Jul 2024 00:39:52 GMT
ADD file:17d80cdc7d7b37786a32ac4e261c7d17cd4d80248ae39f9574ab5a6bf6a2707c in / 
# Tue, 02 Jul 2024 00:39:52 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 04:06:13 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 04:06:13 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Tue, 02 Jul 2024 04:06:13 GMT
ENV EMQX_VERSION=5.1.6
# Tue, 02 Jul 2024 04:06:13 GMT
ENV AMD64_SHA256=5c65f7538141e93d71d1dd7d088589339ef6a091b90f901604a2e0e004f5f4aa
# Tue, 02 Jul 2024 04:06:13 GMT
ENV ARM64_SHA256=ae832d29d6b4e7fa43f3bf04c8c9fad4c9047f079d1587d3ed2a3564d5ea8147
# Tue, 02 Jul 2024 04:06:14 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 02 Jul 2024 04:06:20 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg
# Tue, 02 Jul 2024 04:06:20 GMT
WORKDIR /opt/emqx
# Tue, 02 Jul 2024 04:06:21 GMT
USER emqx
# Tue, 02 Jul 2024 04:06:21 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 02 Jul 2024 04:06:21 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Tue, 02 Jul 2024 04:06:21 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Tue, 02 Jul 2024 04:06:21 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 02 Jul 2024 04:06:21 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:d13ad33c16eef01d20d5563bfb2ec4f25c0d12699b40cdab418e47b88d2f02e2`  
		Last Modified: Tue, 02 Jul 2024 00:43:04 GMT  
		Size: 30.1 MB (30069615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50ed1ead68b106555b7702cd67bfea91393035db82f1d2956e66bea5aa76d884`  
		Last Modified: Tue, 02 Jul 2024 04:08:18 GMT  
		Size: 3.0 MB (3004478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a092beb378b5f70dd4caa7f309fa4fd36df42994aab6816acbe43742814405cb`  
		Last Modified: Tue, 02 Jul 2024 04:08:17 GMT  
		Size: 4.1 KB (4081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f4f8062829dc895f30b38782ce3cd38d0658e5e89e23a6621ebd9843deaa754`  
		Last Modified: Tue, 02 Jul 2024 04:08:22 GMT  
		Size: 59.6 MB (59624724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daa4e633320795188232ffc346fe8f099a282fb31879e5a9c1a1b428e9d727a1`  
		Last Modified: Tue, 02 Jul 2024 04:08:17 GMT  
		Size: 901.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:5.2`

```console
$ docker pull emqx@sha256:18f7337bd6864ec212a43782dca8b36a6cdfc7129f84c3198a15bb61e199f91e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5.2` - linux; amd64

```console
$ docker pull emqx@sha256:c7244e10a477f8f0aa5f03487f283c1d2c3ad56d75e3e84dd114198a216bf5e2
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.2 MB (101181437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01c44330a8ef3022eb94568e7e48642303fc962c55adcfe3ec67cc3eb6471e10`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Thu, 13 Jun 2024 01:21:18 GMT
ADD file:574b112227f85a83f5d80d2523398640537475d2a56fa4c622397c466c0b552b in / 
# Thu, 13 Jun 2024 01:21:18 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 03:55:16 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 03:55:17 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Thu, 13 Jun 2024 03:55:17 GMT
ENV EMQX_VERSION=5.2.1
# Thu, 13 Jun 2024 03:55:17 GMT
ENV AMD64_SHA256=359a12811e5e6725e4269d9484abd348effdde35c0f2af1f5b63cae790c73020
# Thu, 13 Jun 2024 03:55:17 GMT
ENV ARM64_SHA256=2e0a3e0b33669c9b6da488970a2f92d08d7bd0824295822b205b83461ba4728d
# Thu, 13 Jun 2024 03:55:17 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Thu, 13 Jun 2024 03:55:28 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl;     rm -rf /var/lib/apt/lists/*;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl
# Thu, 13 Jun 2024 03:55:28 GMT
WORKDIR /opt/emqx
# Thu, 13 Jun 2024 03:55:28 GMT
USER emqx
# Thu, 13 Jun 2024 03:55:29 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Thu, 13 Jun 2024 03:55:29 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Thu, 13 Jun 2024 03:55:29 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Thu, 13 Jun 2024 03:55:29 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Thu, 13 Jun 2024 03:55:29 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:f7b75fe1f735933f47315080637abf01f87962d47f8636a07ff4535ed7a4a133`  
		Last Modified: Thu, 13 Jun 2024 01:26:15 GMT  
		Size: 31.4 MB (31434040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0208d68f9c6279f0590d8e995a110487769ce608abbe3615beaa26429c65d468`  
		Last Modified: Thu, 13 Jun 2024 03:57:45 GMT  
		Size: 1.6 MB (1631336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5fffa01708702c731fe6ee1573f442274dec6ac3d7f10f1752e9ce8a0433c5d`  
		Last Modified: Thu, 13 Jun 2024 03:57:44 GMT  
		Size: 4.1 KB (4080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:527ff68d43cb16d52ff0dc48c786703d9646c2f86e4e31b305a6bb87ead26b29`  
		Last Modified: Thu, 13 Jun 2024 03:57:51 GMT  
		Size: 68.1 MB (68111079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dafa7ad93fc20ecc970e5b2d11dda9baab7896ff3ac18d3e54822d3615a4b111`  
		Last Modified: Thu, 13 Jun 2024 03:57:44 GMT  
		Size: 902.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:5.2` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:1431ed6b7351f63df989aa47418be5324047c6d6803e498c5e77bee325579d42
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.5 MB (91469566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e15e47f4554d90452fe4f542778c9fab2108d58082219cb5a0adfa96f129ee1`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 02 Jul 2024 00:39:52 GMT
ADD file:17d80cdc7d7b37786a32ac4e261c7d17cd4d80248ae39f9574ab5a6bf6a2707c in / 
# Tue, 02 Jul 2024 00:39:52 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 04:06:28 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 04:06:29 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Tue, 02 Jul 2024 04:06:29 GMT
ENV EMQX_VERSION=5.2.1
# Tue, 02 Jul 2024 04:06:29 GMT
ENV AMD64_SHA256=359a12811e5e6725e4269d9484abd348effdde35c0f2af1f5b63cae790c73020
# Tue, 02 Jul 2024 04:06:29 GMT
ENV ARM64_SHA256=2e0a3e0b33669c9b6da488970a2f92d08d7bd0824295822b205b83461ba4728d
# Tue, 02 Jul 2024 04:06:29 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 02 Jul 2024 04:06:38 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl;     rm -rf /var/lib/apt/lists/*;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl
# Tue, 02 Jul 2024 04:06:38 GMT
WORKDIR /opt/emqx
# Tue, 02 Jul 2024 04:06:39 GMT
USER emqx
# Tue, 02 Jul 2024 04:06:39 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 02 Jul 2024 04:06:39 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Tue, 02 Jul 2024 04:06:39 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Tue, 02 Jul 2024 04:06:39 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 02 Jul 2024 04:06:39 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:d13ad33c16eef01d20d5563bfb2ec4f25c0d12699b40cdab418e47b88d2f02e2`  
		Last Modified: Tue, 02 Jul 2024 00:43:04 GMT  
		Size: 30.1 MB (30069615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0734229117a45b54f93d8b9148f30efdf5f1d8d3a888094ca865fa9082471c96`  
		Last Modified: Tue, 02 Jul 2024 04:08:29 GMT  
		Size: 1.6 MB (1644122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a54fa8ec19887eb930c8de2daa11920313b544b4318847197f8ff5d58b9445f8`  
		Last Modified: Tue, 02 Jul 2024 04:08:29 GMT  
		Size: 4.1 KB (4081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df1b985ef3b5ac7d971cdfd716dba542c6709c2023cc374aa64318f7b2cc77ce`  
		Last Modified: Tue, 02 Jul 2024 04:08:35 GMT  
		Size: 59.8 MB (59750848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8f7ded5fb40d378c24f4ebca44c2c87dd899a11cab38685674eb49d374f6c17`  
		Last Modified: Tue, 02 Jul 2024 04:08:29 GMT  
		Size: 900.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:5.2.1`

```console
$ docker pull emqx@sha256:18f7337bd6864ec212a43782dca8b36a6cdfc7129f84c3198a15bb61e199f91e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5.2.1` - linux; amd64

```console
$ docker pull emqx@sha256:c7244e10a477f8f0aa5f03487f283c1d2c3ad56d75e3e84dd114198a216bf5e2
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.2 MB (101181437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01c44330a8ef3022eb94568e7e48642303fc962c55adcfe3ec67cc3eb6471e10`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Thu, 13 Jun 2024 01:21:18 GMT
ADD file:574b112227f85a83f5d80d2523398640537475d2a56fa4c622397c466c0b552b in / 
# Thu, 13 Jun 2024 01:21:18 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 03:55:16 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 03:55:17 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Thu, 13 Jun 2024 03:55:17 GMT
ENV EMQX_VERSION=5.2.1
# Thu, 13 Jun 2024 03:55:17 GMT
ENV AMD64_SHA256=359a12811e5e6725e4269d9484abd348effdde35c0f2af1f5b63cae790c73020
# Thu, 13 Jun 2024 03:55:17 GMT
ENV ARM64_SHA256=2e0a3e0b33669c9b6da488970a2f92d08d7bd0824295822b205b83461ba4728d
# Thu, 13 Jun 2024 03:55:17 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Thu, 13 Jun 2024 03:55:28 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl;     rm -rf /var/lib/apt/lists/*;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl
# Thu, 13 Jun 2024 03:55:28 GMT
WORKDIR /opt/emqx
# Thu, 13 Jun 2024 03:55:28 GMT
USER emqx
# Thu, 13 Jun 2024 03:55:29 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Thu, 13 Jun 2024 03:55:29 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Thu, 13 Jun 2024 03:55:29 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Thu, 13 Jun 2024 03:55:29 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Thu, 13 Jun 2024 03:55:29 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:f7b75fe1f735933f47315080637abf01f87962d47f8636a07ff4535ed7a4a133`  
		Last Modified: Thu, 13 Jun 2024 01:26:15 GMT  
		Size: 31.4 MB (31434040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0208d68f9c6279f0590d8e995a110487769ce608abbe3615beaa26429c65d468`  
		Last Modified: Thu, 13 Jun 2024 03:57:45 GMT  
		Size: 1.6 MB (1631336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5fffa01708702c731fe6ee1573f442274dec6ac3d7f10f1752e9ce8a0433c5d`  
		Last Modified: Thu, 13 Jun 2024 03:57:44 GMT  
		Size: 4.1 KB (4080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:527ff68d43cb16d52ff0dc48c786703d9646c2f86e4e31b305a6bb87ead26b29`  
		Last Modified: Thu, 13 Jun 2024 03:57:51 GMT  
		Size: 68.1 MB (68111079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dafa7ad93fc20ecc970e5b2d11dda9baab7896ff3ac18d3e54822d3615a4b111`  
		Last Modified: Thu, 13 Jun 2024 03:57:44 GMT  
		Size: 902.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:5.2.1` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:1431ed6b7351f63df989aa47418be5324047c6d6803e498c5e77bee325579d42
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.5 MB (91469566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e15e47f4554d90452fe4f542778c9fab2108d58082219cb5a0adfa96f129ee1`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 02 Jul 2024 00:39:52 GMT
ADD file:17d80cdc7d7b37786a32ac4e261c7d17cd4d80248ae39f9574ab5a6bf6a2707c in / 
# Tue, 02 Jul 2024 00:39:52 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 04:06:28 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 04:06:29 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Tue, 02 Jul 2024 04:06:29 GMT
ENV EMQX_VERSION=5.2.1
# Tue, 02 Jul 2024 04:06:29 GMT
ENV AMD64_SHA256=359a12811e5e6725e4269d9484abd348effdde35c0f2af1f5b63cae790c73020
# Tue, 02 Jul 2024 04:06:29 GMT
ENV ARM64_SHA256=2e0a3e0b33669c9b6da488970a2f92d08d7bd0824295822b205b83461ba4728d
# Tue, 02 Jul 2024 04:06:29 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 02 Jul 2024 04:06:38 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl;     rm -rf /var/lib/apt/lists/*;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl
# Tue, 02 Jul 2024 04:06:38 GMT
WORKDIR /opt/emqx
# Tue, 02 Jul 2024 04:06:39 GMT
USER emqx
# Tue, 02 Jul 2024 04:06:39 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 02 Jul 2024 04:06:39 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Tue, 02 Jul 2024 04:06:39 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Tue, 02 Jul 2024 04:06:39 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 02 Jul 2024 04:06:39 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:d13ad33c16eef01d20d5563bfb2ec4f25c0d12699b40cdab418e47b88d2f02e2`  
		Last Modified: Tue, 02 Jul 2024 00:43:04 GMT  
		Size: 30.1 MB (30069615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0734229117a45b54f93d8b9148f30efdf5f1d8d3a888094ca865fa9082471c96`  
		Last Modified: Tue, 02 Jul 2024 04:08:29 GMT  
		Size: 1.6 MB (1644122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a54fa8ec19887eb930c8de2daa11920313b544b4318847197f8ff5d58b9445f8`  
		Last Modified: Tue, 02 Jul 2024 04:08:29 GMT  
		Size: 4.1 KB (4081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df1b985ef3b5ac7d971cdfd716dba542c6709c2023cc374aa64318f7b2cc77ce`  
		Last Modified: Tue, 02 Jul 2024 04:08:35 GMT  
		Size: 59.8 MB (59750848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8f7ded5fb40d378c24f4ebca44c2c87dd899a11cab38685674eb49d374f6c17`  
		Last Modified: Tue, 02 Jul 2024 04:08:29 GMT  
		Size: 900.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:5.3`

```console
$ docker pull emqx@sha256:c9eda6bd0b4ab31288e9729f803bb3bead3ab0713925e1322c32dabace389038
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5.3` - linux; amd64

```console
$ docker pull emqx@sha256:bf78eed6ebdb278e3b89658c8cee37f03c1f732a62157958930db62c19fc3115
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.8 MB (101796665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9540354cceb08ddfdae331715c0c09e2a8bb8dc44ab8db4a750e088cbfb4b4c1`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Thu, 13 Jun 2024 01:21:18 GMT
ADD file:574b112227f85a83f5d80d2523398640537475d2a56fa4c622397c466c0b552b in / 
# Thu, 13 Jun 2024 01:21:18 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 03:55:32 GMT
ENV EMQX_VERSION=5.3.2
# Thu, 13 Jun 2024 03:55:32 GMT
ENV AMD64_SHA256=d5948d4171f57e77756dd6c9eeb745c39e391e75aad3798fce445f44f5690be0
# Thu, 13 Jun 2024 03:55:32 GMT
ENV ARM64_SHA256=82b056bb1c1cd1f16e9d0719150fa8ac19c499d29563738bcd6984b3c395c6ac
# Thu, 13 Jun 2024 03:55:32 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Thu, 13 Jun 2024 03:55:45 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 03:55:46 GMT
WORKDIR /opt/emqx
# Thu, 13 Jun 2024 03:55:46 GMT
USER emqx
# Thu, 13 Jun 2024 03:55:46 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Thu, 13 Jun 2024 03:55:46 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Thu, 13 Jun 2024 03:55:46 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Thu, 13 Jun 2024 03:55:47 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Thu, 13 Jun 2024 03:55:47 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:f7b75fe1f735933f47315080637abf01f87962d47f8636a07ff4535ed7a4a133`  
		Last Modified: Thu, 13 Jun 2024 01:26:15 GMT  
		Size: 31.4 MB (31434040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1e1fa0bc2570114366d9603ac3ae5e8546e8d4c26c08c3dd5786c1382338f89`  
		Last Modified: Thu, 13 Jun 2024 03:58:06 GMT  
		Size: 70.4 MB (70361722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a813741233fe12aba40528ca51c81b61c20b3bebb93f846fdf610dc0975610f`  
		Last Modified: Thu, 13 Jun 2024 03:57:59 GMT  
		Size: 903.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:5.3` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:ca60b7ecd7cbe0a01b457e9e20183a163e7ef1aac21dc4e2a9dcf4734069fe5f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.1 MB (92083981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11dab6443e86458206d7cd8285f9274f01101fb79362f07166f15cb9ccfa850c`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 02 Jul 2024 00:39:52 GMT
ADD file:17d80cdc7d7b37786a32ac4e261c7d17cd4d80248ae39f9574ab5a6bf6a2707c in / 
# Tue, 02 Jul 2024 00:39:52 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 04:06:44 GMT
ENV EMQX_VERSION=5.3.2
# Tue, 02 Jul 2024 04:06:44 GMT
ENV AMD64_SHA256=d5948d4171f57e77756dd6c9eeb745c39e391e75aad3798fce445f44f5690be0
# Tue, 02 Jul 2024 04:06:44 GMT
ENV ARM64_SHA256=82b056bb1c1cd1f16e9d0719150fa8ac19c499d29563738bcd6984b3c395c6ac
# Tue, 02 Jul 2024 04:06:44 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 02 Jul 2024 04:06:55 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 04:06:55 GMT
WORKDIR /opt/emqx
# Tue, 02 Jul 2024 04:06:55 GMT
USER emqx
# Tue, 02 Jul 2024 04:06:55 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 02 Jul 2024 04:06:55 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Tue, 02 Jul 2024 04:06:56 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Tue, 02 Jul 2024 04:06:56 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 02 Jul 2024 04:06:56 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:d13ad33c16eef01d20d5563bfb2ec4f25c0d12699b40cdab418e47b88d2f02e2`  
		Last Modified: Tue, 02 Jul 2024 00:43:04 GMT  
		Size: 30.1 MB (30069615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6d2994db3481c10f85a482c9724c180febfb5804b4b67eb742507538c2cd9ca`  
		Last Modified: Tue, 02 Jul 2024 04:08:48 GMT  
		Size: 62.0 MB (62013465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6094ac2475cd17aa76f3ad223b0f29e15d9b8e44ac0683139487183d20a0b7c`  
		Last Modified: Tue, 02 Jul 2024 04:08:43 GMT  
		Size: 901.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:5.3.2`

```console
$ docker pull emqx@sha256:c9eda6bd0b4ab31288e9729f803bb3bead3ab0713925e1322c32dabace389038
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5.3.2` - linux; amd64

```console
$ docker pull emqx@sha256:bf78eed6ebdb278e3b89658c8cee37f03c1f732a62157958930db62c19fc3115
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.8 MB (101796665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9540354cceb08ddfdae331715c0c09e2a8bb8dc44ab8db4a750e088cbfb4b4c1`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Thu, 13 Jun 2024 01:21:18 GMT
ADD file:574b112227f85a83f5d80d2523398640537475d2a56fa4c622397c466c0b552b in / 
# Thu, 13 Jun 2024 01:21:18 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 03:55:32 GMT
ENV EMQX_VERSION=5.3.2
# Thu, 13 Jun 2024 03:55:32 GMT
ENV AMD64_SHA256=d5948d4171f57e77756dd6c9eeb745c39e391e75aad3798fce445f44f5690be0
# Thu, 13 Jun 2024 03:55:32 GMT
ENV ARM64_SHA256=82b056bb1c1cd1f16e9d0719150fa8ac19c499d29563738bcd6984b3c395c6ac
# Thu, 13 Jun 2024 03:55:32 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Thu, 13 Jun 2024 03:55:45 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 03:55:46 GMT
WORKDIR /opt/emqx
# Thu, 13 Jun 2024 03:55:46 GMT
USER emqx
# Thu, 13 Jun 2024 03:55:46 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Thu, 13 Jun 2024 03:55:46 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Thu, 13 Jun 2024 03:55:46 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Thu, 13 Jun 2024 03:55:47 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Thu, 13 Jun 2024 03:55:47 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:f7b75fe1f735933f47315080637abf01f87962d47f8636a07ff4535ed7a4a133`  
		Last Modified: Thu, 13 Jun 2024 01:26:15 GMT  
		Size: 31.4 MB (31434040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1e1fa0bc2570114366d9603ac3ae5e8546e8d4c26c08c3dd5786c1382338f89`  
		Last Modified: Thu, 13 Jun 2024 03:58:06 GMT  
		Size: 70.4 MB (70361722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a813741233fe12aba40528ca51c81b61c20b3bebb93f846fdf610dc0975610f`  
		Last Modified: Thu, 13 Jun 2024 03:57:59 GMT  
		Size: 903.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:5.3.2` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:ca60b7ecd7cbe0a01b457e9e20183a163e7ef1aac21dc4e2a9dcf4734069fe5f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.1 MB (92083981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11dab6443e86458206d7cd8285f9274f01101fb79362f07166f15cb9ccfa850c`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 02 Jul 2024 00:39:52 GMT
ADD file:17d80cdc7d7b37786a32ac4e261c7d17cd4d80248ae39f9574ab5a6bf6a2707c in / 
# Tue, 02 Jul 2024 00:39:52 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 04:06:44 GMT
ENV EMQX_VERSION=5.3.2
# Tue, 02 Jul 2024 04:06:44 GMT
ENV AMD64_SHA256=d5948d4171f57e77756dd6c9eeb745c39e391e75aad3798fce445f44f5690be0
# Tue, 02 Jul 2024 04:06:44 GMT
ENV ARM64_SHA256=82b056bb1c1cd1f16e9d0719150fa8ac19c499d29563738bcd6984b3c395c6ac
# Tue, 02 Jul 2024 04:06:44 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 02 Jul 2024 04:06:55 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 04:06:55 GMT
WORKDIR /opt/emqx
# Tue, 02 Jul 2024 04:06:55 GMT
USER emqx
# Tue, 02 Jul 2024 04:06:55 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 02 Jul 2024 04:06:55 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Tue, 02 Jul 2024 04:06:56 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Tue, 02 Jul 2024 04:06:56 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 02 Jul 2024 04:06:56 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:d13ad33c16eef01d20d5563bfb2ec4f25c0d12699b40cdab418e47b88d2f02e2`  
		Last Modified: Tue, 02 Jul 2024 00:43:04 GMT  
		Size: 30.1 MB (30069615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6d2994db3481c10f85a482c9724c180febfb5804b4b67eb742507538c2cd9ca`  
		Last Modified: Tue, 02 Jul 2024 04:08:48 GMT  
		Size: 62.0 MB (62013465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6094ac2475cd17aa76f3ad223b0f29e15d9b8e44ac0683139487183d20a0b7c`  
		Last Modified: Tue, 02 Jul 2024 04:08:43 GMT  
		Size: 901.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:5.4`

```console
$ docker pull emqx@sha256:d45221b80f00ef9f7b527c52acb829b8d24bbb0a8abc39a149c985e2dc847079
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5.4` - linux; amd64

```console
$ docker pull emqx@sha256:54d4671e2c5426af42c01fe34f2c6e462f665a9857caed5a2a40a191f093c95c
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.7 MB (118710755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebf3e1221a774469cf335874de0bd0633bc8ea667f531b690579072e0534a6a1`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Thu, 13 Jun 2024 01:21:18 GMT
ADD file:574b112227f85a83f5d80d2523398640537475d2a56fa4c622397c466c0b552b in / 
# Thu, 13 Jun 2024 01:21:18 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 03:55:53 GMT
ENV EMQX_VERSION=5.4.1
# Thu, 13 Jun 2024 03:55:53 GMT
ENV AMD64_SHA256=c2087651d72f17999f52d73ff22cd8f23dc5fa5db8b5a90a8bc4a1410b03affb
# Thu, 13 Jun 2024 03:55:53 GMT
ENV ARM64_SHA256=6c53a68ae907f7b4a3cdcd4dbee4f839b07853695ac1c039b51fd97d993073bc
# Thu, 13 Jun 2024 03:55:53 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Thu, 13 Jun 2024 03:56:08 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 03:56:08 GMT
WORKDIR /opt/emqx
# Thu, 13 Jun 2024 03:56:08 GMT
USER emqx
# Thu, 13 Jun 2024 03:56:08 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Thu, 13 Jun 2024 03:56:08 GMT
EXPOSE 18083 1883 4370 5369 8083 8084 8883
# Thu, 13 Jun 2024 03:56:09 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Thu, 13 Jun 2024 03:56:09 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Thu, 13 Jun 2024 03:56:09 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:f7b75fe1f735933f47315080637abf01f87962d47f8636a07ff4535ed7a4a133`  
		Last Modified: Thu, 13 Jun 2024 01:26:15 GMT  
		Size: 31.4 MB (31434040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eb85fafa02e1eedc4769b99c3faa87cb042f61ac33293b7b22c353cf01b81c8`  
		Last Modified: Thu, 13 Jun 2024 03:58:23 GMT  
		Size: 87.3 MB (87275816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d3148676b6f7eef01235be27c5473ee49aa60b59da002af97e7b3f91830d09e`  
		Last Modified: Thu, 13 Jun 2024 03:58:14 GMT  
		Size: 899.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:5.4` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:8d62feb5a41d1c3d7c950bb3ff312a09ff93e4aeff2c4d0acaba1c992e79ee2f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.5 MB (108480012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6aedfad2d3a625be78fc67a5f78aa536c74ced4339e6ade02857d13e36ab248b`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 02 Jul 2024 00:39:52 GMT
ADD file:17d80cdc7d7b37786a32ac4e261c7d17cd4d80248ae39f9574ab5a6bf6a2707c in / 
# Tue, 02 Jul 2024 00:39:52 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 04:06:57 GMT
ENV EMQX_VERSION=5.4.1
# Tue, 02 Jul 2024 04:06:57 GMT
ENV AMD64_SHA256=c2087651d72f17999f52d73ff22cd8f23dc5fa5db8b5a90a8bc4a1410b03affb
# Tue, 02 Jul 2024 04:06:58 GMT
ENV ARM64_SHA256=6c53a68ae907f7b4a3cdcd4dbee4f839b07853695ac1c039b51fd97d993073bc
# Tue, 02 Jul 2024 04:06:58 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 02 Jul 2024 04:07:10 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 04:07:11 GMT
WORKDIR /opt/emqx
# Tue, 02 Jul 2024 04:07:11 GMT
USER emqx
# Tue, 02 Jul 2024 04:07:11 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 02 Jul 2024 04:07:11 GMT
EXPOSE 18083 1883 4370 5369 8083 8084 8883
# Tue, 02 Jul 2024 04:07:12 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Tue, 02 Jul 2024 04:07:12 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 02 Jul 2024 04:07:12 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:d13ad33c16eef01d20d5563bfb2ec4f25c0d12699b40cdab418e47b88d2f02e2`  
		Last Modified: Tue, 02 Jul 2024 00:43:04 GMT  
		Size: 30.1 MB (30069615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:274503190cd1f1345397c5ce9773e366ea81cfbd4ccf1029e787efc29fd2e0b9`  
		Last Modified: Tue, 02 Jul 2024 04:09:02 GMT  
		Size: 78.4 MB (78409495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8e341ede7f5a9ec98520829ce55e180b545c9cd499e375d2cd36fabef4140ef`  
		Last Modified: Tue, 02 Jul 2024 04:08:55 GMT  
		Size: 902.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:5.4.1`

```console
$ docker pull emqx@sha256:d45221b80f00ef9f7b527c52acb829b8d24bbb0a8abc39a149c985e2dc847079
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5.4.1` - linux; amd64

```console
$ docker pull emqx@sha256:54d4671e2c5426af42c01fe34f2c6e462f665a9857caed5a2a40a191f093c95c
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.7 MB (118710755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebf3e1221a774469cf335874de0bd0633bc8ea667f531b690579072e0534a6a1`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Thu, 13 Jun 2024 01:21:18 GMT
ADD file:574b112227f85a83f5d80d2523398640537475d2a56fa4c622397c466c0b552b in / 
# Thu, 13 Jun 2024 01:21:18 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 03:55:53 GMT
ENV EMQX_VERSION=5.4.1
# Thu, 13 Jun 2024 03:55:53 GMT
ENV AMD64_SHA256=c2087651d72f17999f52d73ff22cd8f23dc5fa5db8b5a90a8bc4a1410b03affb
# Thu, 13 Jun 2024 03:55:53 GMT
ENV ARM64_SHA256=6c53a68ae907f7b4a3cdcd4dbee4f839b07853695ac1c039b51fd97d993073bc
# Thu, 13 Jun 2024 03:55:53 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Thu, 13 Jun 2024 03:56:08 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 03:56:08 GMT
WORKDIR /opt/emqx
# Thu, 13 Jun 2024 03:56:08 GMT
USER emqx
# Thu, 13 Jun 2024 03:56:08 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Thu, 13 Jun 2024 03:56:08 GMT
EXPOSE 18083 1883 4370 5369 8083 8084 8883
# Thu, 13 Jun 2024 03:56:09 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Thu, 13 Jun 2024 03:56:09 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Thu, 13 Jun 2024 03:56:09 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:f7b75fe1f735933f47315080637abf01f87962d47f8636a07ff4535ed7a4a133`  
		Last Modified: Thu, 13 Jun 2024 01:26:15 GMT  
		Size: 31.4 MB (31434040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eb85fafa02e1eedc4769b99c3faa87cb042f61ac33293b7b22c353cf01b81c8`  
		Last Modified: Thu, 13 Jun 2024 03:58:23 GMT  
		Size: 87.3 MB (87275816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d3148676b6f7eef01235be27c5473ee49aa60b59da002af97e7b3f91830d09e`  
		Last Modified: Thu, 13 Jun 2024 03:58:14 GMT  
		Size: 899.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:5.4.1` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:8d62feb5a41d1c3d7c950bb3ff312a09ff93e4aeff2c4d0acaba1c992e79ee2f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.5 MB (108480012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6aedfad2d3a625be78fc67a5f78aa536c74ced4339e6ade02857d13e36ab248b`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 02 Jul 2024 00:39:52 GMT
ADD file:17d80cdc7d7b37786a32ac4e261c7d17cd4d80248ae39f9574ab5a6bf6a2707c in / 
# Tue, 02 Jul 2024 00:39:52 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 04:06:57 GMT
ENV EMQX_VERSION=5.4.1
# Tue, 02 Jul 2024 04:06:57 GMT
ENV AMD64_SHA256=c2087651d72f17999f52d73ff22cd8f23dc5fa5db8b5a90a8bc4a1410b03affb
# Tue, 02 Jul 2024 04:06:58 GMT
ENV ARM64_SHA256=6c53a68ae907f7b4a3cdcd4dbee4f839b07853695ac1c039b51fd97d993073bc
# Tue, 02 Jul 2024 04:06:58 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 02 Jul 2024 04:07:10 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 04:07:11 GMT
WORKDIR /opt/emqx
# Tue, 02 Jul 2024 04:07:11 GMT
USER emqx
# Tue, 02 Jul 2024 04:07:11 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 02 Jul 2024 04:07:11 GMT
EXPOSE 18083 1883 4370 5369 8083 8084 8883
# Tue, 02 Jul 2024 04:07:12 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Tue, 02 Jul 2024 04:07:12 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 02 Jul 2024 04:07:12 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:d13ad33c16eef01d20d5563bfb2ec4f25c0d12699b40cdab418e47b88d2f02e2`  
		Last Modified: Tue, 02 Jul 2024 00:43:04 GMT  
		Size: 30.1 MB (30069615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:274503190cd1f1345397c5ce9773e366ea81cfbd4ccf1029e787efc29fd2e0b9`  
		Last Modified: Tue, 02 Jul 2024 04:09:02 GMT  
		Size: 78.4 MB (78409495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8e341ede7f5a9ec98520829ce55e180b545c9cd499e375d2cd36fabef4140ef`  
		Last Modified: Tue, 02 Jul 2024 04:08:55 GMT  
		Size: 902.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:5.5`

```console
$ docker pull emqx@sha256:1bde798156412f721b60be3d952ecb6d947e0e9eb36226810f4898f3cac82cbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5.5` - linux; amd64

```console
$ docker pull emqx@sha256:2422653050058c9db18fc5dcdc8a4d8d572d1598a638670a92b4c803be5dbafa
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.3 MB (121275849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:deb9e3e7f5ec4b11f90f9ac7335c4f6204fcfdbbe11a9aad6b064fb9f995fef7`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Thu, 13 Jun 2024 01:21:18 GMT
ADD file:574b112227f85a83f5d80d2523398640537475d2a56fa4c622397c466c0b552b in / 
# Thu, 13 Jun 2024 01:21:18 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 03:56:13 GMT
ENV EMQX_VERSION=5.5.1
# Thu, 13 Jun 2024 03:56:13 GMT
ENV AMD64_SHA256=8bac2886987a632aab1c738aa3de28684b415d3b1e1f9489b458c819254673a6
# Thu, 13 Jun 2024 03:56:13 GMT
ENV ARM64_SHA256=8b962ad8beea50fb92dc0b93d2ab8a5064752147b70bbf46fd221bc4cc29c32d
# Thu, 13 Jun 2024 03:56:13 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Thu, 13 Jun 2024 03:56:28 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     mkdir -p /opt/emqx/log /opt/emqx/data /opt/emqx/plugins;     chown -R emqx:emqx /opt/emqx/log /opt/emqx/data /opt/emqx/plugins;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 13 Jun 2024 03:56:29 GMT
WORKDIR /opt/emqx
# Thu, 13 Jun 2024 03:56:29 GMT
USER emqx
# Thu, 13 Jun 2024 03:56:29 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Thu, 13 Jun 2024 03:56:29 GMT
EXPOSE 18083 1883 4370 5369 8083 8084 8883
# Thu, 13 Jun 2024 03:56:29 GMT
COPY file:f0e3faa715cc7e845bbdf3b121a4a8bad40d65e5cef1fac9f1285fec250cedf2 in /usr/bin/ 
# Thu, 13 Jun 2024 03:56:29 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Thu, 13 Jun 2024 03:56:29 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:f7b75fe1f735933f47315080637abf01f87962d47f8636a07ff4535ed7a4a133`  
		Last Modified: Thu, 13 Jun 2024 01:26:15 GMT  
		Size: 31.4 MB (31434040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11b081183319c2b1650d1e4a00a4c692b1e81f182a0dc161c69523639a3bd344`  
		Last Modified: Thu, 13 Jun 2024 03:58:41 GMT  
		Size: 89.8 MB (89840776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:212fc3caa74149af6b7ba07a5610b47a48aee393908615685d1992e56108afd6`  
		Last Modified: Thu, 13 Jun 2024 03:58:31 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:5.5` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:7d3350ef27cf6dea63f6aa1e46b3196e5b811626589bf554683afe58999096e5
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.8 MB (116777912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ab2d1259d5777f35bc005d610df3d1269b527ed1a3988384d0a933aeb0ebf4d`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 02 Jul 2024 00:39:52 GMT
ADD file:17d80cdc7d7b37786a32ac4e261c7d17cd4d80248ae39f9574ab5a6bf6a2707c in / 
# Tue, 02 Jul 2024 00:39:52 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 04:07:14 GMT
ENV EMQX_VERSION=5.5.1
# Tue, 02 Jul 2024 04:07:14 GMT
ENV AMD64_SHA256=8bac2886987a632aab1c738aa3de28684b415d3b1e1f9489b458c819254673a6
# Tue, 02 Jul 2024 04:07:14 GMT
ENV ARM64_SHA256=8b962ad8beea50fb92dc0b93d2ab8a5064752147b70bbf46fd221bc4cc29c32d
# Tue, 02 Jul 2024 04:07:14 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 02 Jul 2024 04:07:27 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     mkdir -p /opt/emqx/log /opt/emqx/data /opt/emqx/plugins;     chown -R emqx:emqx /opt/emqx/log /opt/emqx/data /opt/emqx/plugins;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Tue, 02 Jul 2024 04:07:28 GMT
WORKDIR /opt/emqx
# Tue, 02 Jul 2024 04:07:28 GMT
USER emqx
# Tue, 02 Jul 2024 04:07:28 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 02 Jul 2024 04:07:28 GMT
EXPOSE 18083 1883 4370 5369 8083 8084 8883
# Tue, 02 Jul 2024 04:07:28 GMT
COPY file:f0e3faa715cc7e845bbdf3b121a4a8bad40d65e5cef1fac9f1285fec250cedf2 in /usr/bin/ 
# Tue, 02 Jul 2024 04:07:28 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 02 Jul 2024 04:07:28 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:d13ad33c16eef01d20d5563bfb2ec4f25c0d12699b40cdab418e47b88d2f02e2`  
		Last Modified: Tue, 02 Jul 2024 00:43:04 GMT  
		Size: 30.1 MB (30069615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b49adc43bb9dd8a05be9573ab3bdedc024dc08283849eb69150eab98ae7653ad`  
		Last Modified: Tue, 02 Jul 2024 04:09:17 GMT  
		Size: 86.7 MB (86707264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f9e298a39960f307a14eaeb2ad56cd39c4771ec408f92f6f1e2e3bdfd4de986`  
		Last Modified: Tue, 02 Jul 2024 04:09:10 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:5.5.1`

```console
$ docker pull emqx@sha256:1bde798156412f721b60be3d952ecb6d947e0e9eb36226810f4898f3cac82cbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5.5.1` - linux; amd64

```console
$ docker pull emqx@sha256:2422653050058c9db18fc5dcdc8a4d8d572d1598a638670a92b4c803be5dbafa
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.3 MB (121275849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:deb9e3e7f5ec4b11f90f9ac7335c4f6204fcfdbbe11a9aad6b064fb9f995fef7`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Thu, 13 Jun 2024 01:21:18 GMT
ADD file:574b112227f85a83f5d80d2523398640537475d2a56fa4c622397c466c0b552b in / 
# Thu, 13 Jun 2024 01:21:18 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 03:56:13 GMT
ENV EMQX_VERSION=5.5.1
# Thu, 13 Jun 2024 03:56:13 GMT
ENV AMD64_SHA256=8bac2886987a632aab1c738aa3de28684b415d3b1e1f9489b458c819254673a6
# Thu, 13 Jun 2024 03:56:13 GMT
ENV ARM64_SHA256=8b962ad8beea50fb92dc0b93d2ab8a5064752147b70bbf46fd221bc4cc29c32d
# Thu, 13 Jun 2024 03:56:13 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Thu, 13 Jun 2024 03:56:28 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     mkdir -p /opt/emqx/log /opt/emqx/data /opt/emqx/plugins;     chown -R emqx:emqx /opt/emqx/log /opt/emqx/data /opt/emqx/plugins;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 13 Jun 2024 03:56:29 GMT
WORKDIR /opt/emqx
# Thu, 13 Jun 2024 03:56:29 GMT
USER emqx
# Thu, 13 Jun 2024 03:56:29 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Thu, 13 Jun 2024 03:56:29 GMT
EXPOSE 18083 1883 4370 5369 8083 8084 8883
# Thu, 13 Jun 2024 03:56:29 GMT
COPY file:f0e3faa715cc7e845bbdf3b121a4a8bad40d65e5cef1fac9f1285fec250cedf2 in /usr/bin/ 
# Thu, 13 Jun 2024 03:56:29 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Thu, 13 Jun 2024 03:56:29 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:f7b75fe1f735933f47315080637abf01f87962d47f8636a07ff4535ed7a4a133`  
		Last Modified: Thu, 13 Jun 2024 01:26:15 GMT  
		Size: 31.4 MB (31434040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11b081183319c2b1650d1e4a00a4c692b1e81f182a0dc161c69523639a3bd344`  
		Last Modified: Thu, 13 Jun 2024 03:58:41 GMT  
		Size: 89.8 MB (89840776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:212fc3caa74149af6b7ba07a5610b47a48aee393908615685d1992e56108afd6`  
		Last Modified: Thu, 13 Jun 2024 03:58:31 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:5.5.1` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:7d3350ef27cf6dea63f6aa1e46b3196e5b811626589bf554683afe58999096e5
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.8 MB (116777912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ab2d1259d5777f35bc005d610df3d1269b527ed1a3988384d0a933aeb0ebf4d`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 02 Jul 2024 00:39:52 GMT
ADD file:17d80cdc7d7b37786a32ac4e261c7d17cd4d80248ae39f9574ab5a6bf6a2707c in / 
# Tue, 02 Jul 2024 00:39:52 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 04:07:14 GMT
ENV EMQX_VERSION=5.5.1
# Tue, 02 Jul 2024 04:07:14 GMT
ENV AMD64_SHA256=8bac2886987a632aab1c738aa3de28684b415d3b1e1f9489b458c819254673a6
# Tue, 02 Jul 2024 04:07:14 GMT
ENV ARM64_SHA256=8b962ad8beea50fb92dc0b93d2ab8a5064752147b70bbf46fd221bc4cc29c32d
# Tue, 02 Jul 2024 04:07:14 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 02 Jul 2024 04:07:27 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     mkdir -p /opt/emqx/log /opt/emqx/data /opt/emqx/plugins;     chown -R emqx:emqx /opt/emqx/log /opt/emqx/data /opt/emqx/plugins;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Tue, 02 Jul 2024 04:07:28 GMT
WORKDIR /opt/emqx
# Tue, 02 Jul 2024 04:07:28 GMT
USER emqx
# Tue, 02 Jul 2024 04:07:28 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 02 Jul 2024 04:07:28 GMT
EXPOSE 18083 1883 4370 5369 8083 8084 8883
# Tue, 02 Jul 2024 04:07:28 GMT
COPY file:f0e3faa715cc7e845bbdf3b121a4a8bad40d65e5cef1fac9f1285fec250cedf2 in /usr/bin/ 
# Tue, 02 Jul 2024 04:07:28 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 02 Jul 2024 04:07:28 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:d13ad33c16eef01d20d5563bfb2ec4f25c0d12699b40cdab418e47b88d2f02e2`  
		Last Modified: Tue, 02 Jul 2024 00:43:04 GMT  
		Size: 30.1 MB (30069615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b49adc43bb9dd8a05be9573ab3bdedc024dc08283849eb69150eab98ae7653ad`  
		Last Modified: Tue, 02 Jul 2024 04:09:17 GMT  
		Size: 86.7 MB (86707264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f9e298a39960f307a14eaeb2ad56cd39c4771ec408f92f6f1e2e3bdfd4de986`  
		Last Modified: Tue, 02 Jul 2024 04:09:10 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:5.6`

```console
$ docker pull emqx@sha256:9c7451b3229cfcf4821e2db1aaaf2871f7d8777eeac77bfc8e41112e7ff01742
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5.6` - linux; amd64

```console
$ docker pull emqx@sha256:ce324951a0da5e1e07d735b86017aa6efc2a19eb52bdf23a9fdfac9d2958cdcd
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.2 MB (124206724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9afdee6aa3dcebdc533a4f7f4be9a9f3b95a92e531370f1b4949a9dc805f04c1`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Thu, 13 Jun 2024 01:20:56 GMT
ADD file:5f9954090af042b377ea0d1d184faa64d2e9d4c946b6c3898d52aff47e764056 in / 
# Thu, 13 Jun 2024 01:20:56 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 03:56:34 GMT
ENV EMQX_VERSION=5.6.1
# Thu, 13 Jun 2024 03:56:34 GMT
ENV AMD64_SHA256=a5be37660bfe6130bc159b934ed98ffcb9bef5519765491b4ed38d08ba304538
# Thu, 13 Jun 2024 03:56:34 GMT
ENV ARM64_SHA256=3f7f9b10d313f760af43e0a54cba2af4eb23ad3864b439196cb8b2903baf5651
# Thu, 13 Jun 2024 03:56:34 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Thu, 13 Jun 2024 03:56:49 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 13 Jun 2024 03:56:49 GMT
WORKDIR /opt/emqx
# Thu, 13 Jun 2024 03:56:50 GMT
USER emqx
# Thu, 13 Jun 2024 03:56:50 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Thu, 13 Jun 2024 03:56:50 GMT
EXPOSE 18083 1883 4370 5369 8083 8084 8883
# Thu, 13 Jun 2024 03:56:50 GMT
COPY file:f0e3faa715cc7e845bbdf3b121a4a8bad40d65e5cef1fac9f1285fec250cedf2 in /usr/bin/ 
# Thu, 13 Jun 2024 03:56:50 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Thu, 13 Jun 2024 03:56:50 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:2cc3ae149d28a36d28d4eefbae70aaa14a0c9eab588c3790f7979f310b893c44`  
		Last Modified: Thu, 13 Jun 2024 01:25:30 GMT  
		Size: 29.2 MB (29150430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f74bef663063657d8e64192364293bc9f97a90a309715bbcfdeff3f3811876bf`  
		Last Modified: Thu, 13 Jun 2024 03:58:59 GMT  
		Size: 95.1 MB (95055258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:685cbb5e68d866cef9403f6388f9ed545b3e0149228f2d8ea55954e1559c6a7e`  
		Last Modified: Thu, 13 Jun 2024 03:58:49 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:5.6` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:846ec32edd65a7805d6e9406fd3401f4b2c0d5c2d0e3d70eadbaaa5d5ef489a6
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.8 MB (120774221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0533c3667e306d8260f83777f839ab4173b350708333268c87b96fdb8ad18b6`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 02 Jul 2024 00:39:37 GMT
ADD file:cbda549b25cd4337cd3ce345e3b66c0d3b43c247d7315906a028f98a56c41f1d in / 
# Tue, 02 Jul 2024 00:39:37 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 04:07:30 GMT
ENV EMQX_VERSION=5.6.1
# Tue, 02 Jul 2024 04:07:30 GMT
ENV AMD64_SHA256=a5be37660bfe6130bc159b934ed98ffcb9bef5519765491b4ed38d08ba304538
# Tue, 02 Jul 2024 04:07:31 GMT
ENV ARM64_SHA256=3f7f9b10d313f760af43e0a54cba2af4eb23ad3864b439196cb8b2903baf5651
# Tue, 02 Jul 2024 04:07:31 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 02 Jul 2024 04:07:40 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Tue, 02 Jul 2024 04:07:41 GMT
WORKDIR /opt/emqx
# Tue, 02 Jul 2024 04:07:42 GMT
USER emqx
# Tue, 02 Jul 2024 04:07:42 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 02 Jul 2024 04:07:42 GMT
EXPOSE 18083 1883 4370 5369 8083 8084 8883
# Tue, 02 Jul 2024 04:07:42 GMT
COPY file:f0e3faa715cc7e845bbdf3b121a4a8bad40d65e5cef1fac9f1285fec250cedf2 in /usr/bin/ 
# Tue, 02 Jul 2024 04:07:42 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 02 Jul 2024 04:07:42 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:ea235d1ccf77ca07a545b448996766dc3eca4b971b04ba39d50af69660b25751`  
		Last Modified: Tue, 02 Jul 2024 00:42:25 GMT  
		Size: 29.2 MB (29156563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0543b8bdb67f5a9c171569106b113225f1aa26f7b251189504a8166929554df5`  
		Last Modified: Tue, 02 Jul 2024 04:09:33 GMT  
		Size: 91.6 MB (91616624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cb5a0d9024990215a2191000fa708cff7ed1af5bd8e43e29cc8e3b296658009`  
		Last Modified: Tue, 02 Jul 2024 04:09:25 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:5.6.1`

```console
$ docker pull emqx@sha256:9c7451b3229cfcf4821e2db1aaaf2871f7d8777eeac77bfc8e41112e7ff01742
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5.6.1` - linux; amd64

```console
$ docker pull emqx@sha256:ce324951a0da5e1e07d735b86017aa6efc2a19eb52bdf23a9fdfac9d2958cdcd
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.2 MB (124206724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9afdee6aa3dcebdc533a4f7f4be9a9f3b95a92e531370f1b4949a9dc805f04c1`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Thu, 13 Jun 2024 01:20:56 GMT
ADD file:5f9954090af042b377ea0d1d184faa64d2e9d4c946b6c3898d52aff47e764056 in / 
# Thu, 13 Jun 2024 01:20:56 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 03:56:34 GMT
ENV EMQX_VERSION=5.6.1
# Thu, 13 Jun 2024 03:56:34 GMT
ENV AMD64_SHA256=a5be37660bfe6130bc159b934ed98ffcb9bef5519765491b4ed38d08ba304538
# Thu, 13 Jun 2024 03:56:34 GMT
ENV ARM64_SHA256=3f7f9b10d313f760af43e0a54cba2af4eb23ad3864b439196cb8b2903baf5651
# Thu, 13 Jun 2024 03:56:34 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Thu, 13 Jun 2024 03:56:49 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 13 Jun 2024 03:56:49 GMT
WORKDIR /opt/emqx
# Thu, 13 Jun 2024 03:56:50 GMT
USER emqx
# Thu, 13 Jun 2024 03:56:50 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Thu, 13 Jun 2024 03:56:50 GMT
EXPOSE 18083 1883 4370 5369 8083 8084 8883
# Thu, 13 Jun 2024 03:56:50 GMT
COPY file:f0e3faa715cc7e845bbdf3b121a4a8bad40d65e5cef1fac9f1285fec250cedf2 in /usr/bin/ 
# Thu, 13 Jun 2024 03:56:50 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Thu, 13 Jun 2024 03:56:50 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:2cc3ae149d28a36d28d4eefbae70aaa14a0c9eab588c3790f7979f310b893c44`  
		Last Modified: Thu, 13 Jun 2024 01:25:30 GMT  
		Size: 29.2 MB (29150430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f74bef663063657d8e64192364293bc9f97a90a309715bbcfdeff3f3811876bf`  
		Last Modified: Thu, 13 Jun 2024 03:58:59 GMT  
		Size: 95.1 MB (95055258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:685cbb5e68d866cef9403f6388f9ed545b3e0149228f2d8ea55954e1559c6a7e`  
		Last Modified: Thu, 13 Jun 2024 03:58:49 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:5.6.1` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:846ec32edd65a7805d6e9406fd3401f4b2c0d5c2d0e3d70eadbaaa5d5ef489a6
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.8 MB (120774221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0533c3667e306d8260f83777f839ab4173b350708333268c87b96fdb8ad18b6`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 02 Jul 2024 00:39:37 GMT
ADD file:cbda549b25cd4337cd3ce345e3b66c0d3b43c247d7315906a028f98a56c41f1d in / 
# Tue, 02 Jul 2024 00:39:37 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 04:07:30 GMT
ENV EMQX_VERSION=5.6.1
# Tue, 02 Jul 2024 04:07:30 GMT
ENV AMD64_SHA256=a5be37660bfe6130bc159b934ed98ffcb9bef5519765491b4ed38d08ba304538
# Tue, 02 Jul 2024 04:07:31 GMT
ENV ARM64_SHA256=3f7f9b10d313f760af43e0a54cba2af4eb23ad3864b439196cb8b2903baf5651
# Tue, 02 Jul 2024 04:07:31 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 02 Jul 2024 04:07:40 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Tue, 02 Jul 2024 04:07:41 GMT
WORKDIR /opt/emqx
# Tue, 02 Jul 2024 04:07:42 GMT
USER emqx
# Tue, 02 Jul 2024 04:07:42 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 02 Jul 2024 04:07:42 GMT
EXPOSE 18083 1883 4370 5369 8083 8084 8883
# Tue, 02 Jul 2024 04:07:42 GMT
COPY file:f0e3faa715cc7e845bbdf3b121a4a8bad40d65e5cef1fac9f1285fec250cedf2 in /usr/bin/ 
# Tue, 02 Jul 2024 04:07:42 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 02 Jul 2024 04:07:42 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:ea235d1ccf77ca07a545b448996766dc3eca4b971b04ba39d50af69660b25751`  
		Last Modified: Tue, 02 Jul 2024 00:42:25 GMT  
		Size: 29.2 MB (29156563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0543b8bdb67f5a9c171569106b113225f1aa26f7b251189504a8166929554df5`  
		Last Modified: Tue, 02 Jul 2024 04:09:33 GMT  
		Size: 91.6 MB (91616624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cb5a0d9024990215a2191000fa708cff7ed1af5bd8e43e29cc8e3b296658009`  
		Last Modified: Tue, 02 Jul 2024 04:09:25 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:5.7`

```console
$ docker pull emqx@sha256:309c87aeb41c7da427f44925e91df25d2db88187639579030e224eb03c1187d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5.7` - linux; amd64

```console
$ docker pull emqx@sha256:23e00db6e6be310c552badbbfef8cad44b8045960b37b2e1169e4aaaefd85121
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.3 MB (126268671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c261fa69f19b02951b5f77db322c55c9dc76d58d6d0be69340a0f6c842665ad`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Thu, 13 Jun 2024 01:20:56 GMT
ADD file:5f9954090af042b377ea0d1d184faa64d2e9d4c946b6c3898d52aff47e764056 in / 
# Thu, 13 Jun 2024 01:20:56 GMT
CMD ["bash"]
# Thu, 27 Jun 2024 18:19:48 GMT
ENV EMQX_VERSION=5.7.1
# Thu, 27 Jun 2024 18:19:48 GMT
ENV AMD64_SHA256=6896263e24c1211fea0e15464afb39931e9b4c7139804e0a6fb5f143826efaf8
# Thu, 27 Jun 2024 18:19:48 GMT
ENV ARM64_SHA256=c321477bab28e381a472761c2d62f9e5acf6290f298f5aaf9404ab70feb6d587
# Thu, 27 Jun 2024 18:19:48 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Thu, 27 Jun 2024 18:20:07 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 27 Jun 2024 18:20:08 GMT
WORKDIR /opt/emqx
# Thu, 27 Jun 2024 18:20:08 GMT
USER emqx
# Thu, 27 Jun 2024 18:20:08 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Thu, 27 Jun 2024 18:20:08 GMT
EXPOSE 18083 1883 4370 5369 8083 8084 8883
# Thu, 27 Jun 2024 18:20:08 GMT
COPY file:f0e3faa715cc7e845bbdf3b121a4a8bad40d65e5cef1fac9f1285fec250cedf2 in /usr/bin/ 
# Thu, 27 Jun 2024 18:20:08 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Thu, 27 Jun 2024 18:20:09 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:2cc3ae149d28a36d28d4eefbae70aaa14a0c9eab588c3790f7979f310b893c44`  
		Last Modified: Thu, 13 Jun 2024 01:25:30 GMT  
		Size: 29.2 MB (29150430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21ada3da96cf914860b0103cd485748be41d637b09bc8853d126f0d98d845ff8`  
		Last Modified: Thu, 27 Jun 2024 18:20:39 GMT  
		Size: 97.1 MB (97117207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87b3cc76375fdf61e1a6705fe7f358029a6939ceb7a97e8f6255bf7a037696d6`  
		Last Modified: Thu, 27 Jun 2024 18:20:30 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:5.7` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:43649a68514edd13ed29eaf28634e3c6cb668c6ef74cc43acc91c44e01bf706b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.8 MB (122818365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffc506dce6f9e4989d8a088171e08078e39628702aff7e4d2ccd33279fda1287`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 02 Jul 2024 00:39:37 GMT
ADD file:cbda549b25cd4337cd3ce345e3b66c0d3b43c247d7315906a028f98a56c41f1d in / 
# Tue, 02 Jul 2024 00:39:37 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 04:07:44 GMT
ENV EMQX_VERSION=5.7.1
# Tue, 02 Jul 2024 04:07:44 GMT
ENV AMD64_SHA256=6896263e24c1211fea0e15464afb39931e9b4c7139804e0a6fb5f143826efaf8
# Tue, 02 Jul 2024 04:07:44 GMT
ENV ARM64_SHA256=c321477bab28e381a472761c2d62f9e5acf6290f298f5aaf9404ab70feb6d587
# Tue, 02 Jul 2024 04:07:44 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 02 Jul 2024 04:07:58 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Tue, 02 Jul 2024 04:07:59 GMT
WORKDIR /opt/emqx
# Tue, 02 Jul 2024 04:07:59 GMT
USER emqx
# Tue, 02 Jul 2024 04:07:59 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 02 Jul 2024 04:07:59 GMT
EXPOSE 18083 1883 4370 5369 8083 8084 8883
# Tue, 02 Jul 2024 04:07:59 GMT
COPY file:f0e3faa715cc7e845bbdf3b121a4a8bad40d65e5cef1fac9f1285fec250cedf2 in /usr/bin/ 
# Tue, 02 Jul 2024 04:08:00 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 02 Jul 2024 04:08:00 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:ea235d1ccf77ca07a545b448996766dc3eca4b971b04ba39d50af69660b25751`  
		Last Modified: Tue, 02 Jul 2024 00:42:25 GMT  
		Size: 29.2 MB (29156563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51c44934ae8ca03950296a4539a08b216eef45c351b694b9232d93161d83368e`  
		Last Modified: Tue, 02 Jul 2024 04:09:48 GMT  
		Size: 93.7 MB (93660768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa2ba6b94a2eb3de1a86a522cc9e627fe013fcaff6ff730bb4f6828ab2b51dba`  
		Last Modified: Tue, 02 Jul 2024 04:09:40 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:5.7.1`

```console
$ docker pull emqx@sha256:309c87aeb41c7da427f44925e91df25d2db88187639579030e224eb03c1187d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5.7.1` - linux; amd64

```console
$ docker pull emqx@sha256:23e00db6e6be310c552badbbfef8cad44b8045960b37b2e1169e4aaaefd85121
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.3 MB (126268671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c261fa69f19b02951b5f77db322c55c9dc76d58d6d0be69340a0f6c842665ad`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Thu, 13 Jun 2024 01:20:56 GMT
ADD file:5f9954090af042b377ea0d1d184faa64d2e9d4c946b6c3898d52aff47e764056 in / 
# Thu, 13 Jun 2024 01:20:56 GMT
CMD ["bash"]
# Thu, 27 Jun 2024 18:19:48 GMT
ENV EMQX_VERSION=5.7.1
# Thu, 27 Jun 2024 18:19:48 GMT
ENV AMD64_SHA256=6896263e24c1211fea0e15464afb39931e9b4c7139804e0a6fb5f143826efaf8
# Thu, 27 Jun 2024 18:19:48 GMT
ENV ARM64_SHA256=c321477bab28e381a472761c2d62f9e5acf6290f298f5aaf9404ab70feb6d587
# Thu, 27 Jun 2024 18:19:48 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Thu, 27 Jun 2024 18:20:07 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 27 Jun 2024 18:20:08 GMT
WORKDIR /opt/emqx
# Thu, 27 Jun 2024 18:20:08 GMT
USER emqx
# Thu, 27 Jun 2024 18:20:08 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Thu, 27 Jun 2024 18:20:08 GMT
EXPOSE 18083 1883 4370 5369 8083 8084 8883
# Thu, 27 Jun 2024 18:20:08 GMT
COPY file:f0e3faa715cc7e845bbdf3b121a4a8bad40d65e5cef1fac9f1285fec250cedf2 in /usr/bin/ 
# Thu, 27 Jun 2024 18:20:08 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Thu, 27 Jun 2024 18:20:09 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:2cc3ae149d28a36d28d4eefbae70aaa14a0c9eab588c3790f7979f310b893c44`  
		Last Modified: Thu, 13 Jun 2024 01:25:30 GMT  
		Size: 29.2 MB (29150430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21ada3da96cf914860b0103cd485748be41d637b09bc8853d126f0d98d845ff8`  
		Last Modified: Thu, 27 Jun 2024 18:20:39 GMT  
		Size: 97.1 MB (97117207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87b3cc76375fdf61e1a6705fe7f358029a6939ceb7a97e8f6255bf7a037696d6`  
		Last Modified: Thu, 27 Jun 2024 18:20:30 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:5.7.1` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:43649a68514edd13ed29eaf28634e3c6cb668c6ef74cc43acc91c44e01bf706b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.8 MB (122818365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffc506dce6f9e4989d8a088171e08078e39628702aff7e4d2ccd33279fda1287`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 02 Jul 2024 00:39:37 GMT
ADD file:cbda549b25cd4337cd3ce345e3b66c0d3b43c247d7315906a028f98a56c41f1d in / 
# Tue, 02 Jul 2024 00:39:37 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 04:07:44 GMT
ENV EMQX_VERSION=5.7.1
# Tue, 02 Jul 2024 04:07:44 GMT
ENV AMD64_SHA256=6896263e24c1211fea0e15464afb39931e9b4c7139804e0a6fb5f143826efaf8
# Tue, 02 Jul 2024 04:07:44 GMT
ENV ARM64_SHA256=c321477bab28e381a472761c2d62f9e5acf6290f298f5aaf9404ab70feb6d587
# Tue, 02 Jul 2024 04:07:44 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 02 Jul 2024 04:07:58 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Tue, 02 Jul 2024 04:07:59 GMT
WORKDIR /opt/emqx
# Tue, 02 Jul 2024 04:07:59 GMT
USER emqx
# Tue, 02 Jul 2024 04:07:59 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 02 Jul 2024 04:07:59 GMT
EXPOSE 18083 1883 4370 5369 8083 8084 8883
# Tue, 02 Jul 2024 04:07:59 GMT
COPY file:f0e3faa715cc7e845bbdf3b121a4a8bad40d65e5cef1fac9f1285fec250cedf2 in /usr/bin/ 
# Tue, 02 Jul 2024 04:08:00 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 02 Jul 2024 04:08:00 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:ea235d1ccf77ca07a545b448996766dc3eca4b971b04ba39d50af69660b25751`  
		Last Modified: Tue, 02 Jul 2024 00:42:25 GMT  
		Size: 29.2 MB (29156563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51c44934ae8ca03950296a4539a08b216eef45c351b694b9232d93161d83368e`  
		Last Modified: Tue, 02 Jul 2024 04:09:48 GMT  
		Size: 93.7 MB (93660768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa2ba6b94a2eb3de1a86a522cc9e627fe013fcaff6ff730bb4f6828ab2b51dba`  
		Last Modified: Tue, 02 Jul 2024 04:09:40 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:latest`

```console
$ docker pull emqx@sha256:309c87aeb41c7da427f44925e91df25d2db88187639579030e224eb03c1187d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:latest` - linux; amd64

```console
$ docker pull emqx@sha256:23e00db6e6be310c552badbbfef8cad44b8045960b37b2e1169e4aaaefd85121
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.3 MB (126268671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c261fa69f19b02951b5f77db322c55c9dc76d58d6d0be69340a0f6c842665ad`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Thu, 13 Jun 2024 01:20:56 GMT
ADD file:5f9954090af042b377ea0d1d184faa64d2e9d4c946b6c3898d52aff47e764056 in / 
# Thu, 13 Jun 2024 01:20:56 GMT
CMD ["bash"]
# Thu, 27 Jun 2024 18:19:48 GMT
ENV EMQX_VERSION=5.7.1
# Thu, 27 Jun 2024 18:19:48 GMT
ENV AMD64_SHA256=6896263e24c1211fea0e15464afb39931e9b4c7139804e0a6fb5f143826efaf8
# Thu, 27 Jun 2024 18:19:48 GMT
ENV ARM64_SHA256=c321477bab28e381a472761c2d62f9e5acf6290f298f5aaf9404ab70feb6d587
# Thu, 27 Jun 2024 18:19:48 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Thu, 27 Jun 2024 18:20:07 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 27 Jun 2024 18:20:08 GMT
WORKDIR /opt/emqx
# Thu, 27 Jun 2024 18:20:08 GMT
USER emqx
# Thu, 27 Jun 2024 18:20:08 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Thu, 27 Jun 2024 18:20:08 GMT
EXPOSE 18083 1883 4370 5369 8083 8084 8883
# Thu, 27 Jun 2024 18:20:08 GMT
COPY file:f0e3faa715cc7e845bbdf3b121a4a8bad40d65e5cef1fac9f1285fec250cedf2 in /usr/bin/ 
# Thu, 27 Jun 2024 18:20:08 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Thu, 27 Jun 2024 18:20:09 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:2cc3ae149d28a36d28d4eefbae70aaa14a0c9eab588c3790f7979f310b893c44`  
		Last Modified: Thu, 13 Jun 2024 01:25:30 GMT  
		Size: 29.2 MB (29150430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21ada3da96cf914860b0103cd485748be41d637b09bc8853d126f0d98d845ff8`  
		Last Modified: Thu, 27 Jun 2024 18:20:39 GMT  
		Size: 97.1 MB (97117207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87b3cc76375fdf61e1a6705fe7f358029a6939ceb7a97e8f6255bf7a037696d6`  
		Last Modified: Thu, 27 Jun 2024 18:20:30 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:latest` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:43649a68514edd13ed29eaf28634e3c6cb668c6ef74cc43acc91c44e01bf706b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.8 MB (122818365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffc506dce6f9e4989d8a088171e08078e39628702aff7e4d2ccd33279fda1287`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 02 Jul 2024 00:39:37 GMT
ADD file:cbda549b25cd4337cd3ce345e3b66c0d3b43c247d7315906a028f98a56c41f1d in / 
# Tue, 02 Jul 2024 00:39:37 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 04:07:44 GMT
ENV EMQX_VERSION=5.7.1
# Tue, 02 Jul 2024 04:07:44 GMT
ENV AMD64_SHA256=6896263e24c1211fea0e15464afb39931e9b4c7139804e0a6fb5f143826efaf8
# Tue, 02 Jul 2024 04:07:44 GMT
ENV ARM64_SHA256=c321477bab28e381a472761c2d62f9e5acf6290f298f5aaf9404ab70feb6d587
# Tue, 02 Jul 2024 04:07:44 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 02 Jul 2024 04:07:58 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Tue, 02 Jul 2024 04:07:59 GMT
WORKDIR /opt/emqx
# Tue, 02 Jul 2024 04:07:59 GMT
USER emqx
# Tue, 02 Jul 2024 04:07:59 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 02 Jul 2024 04:07:59 GMT
EXPOSE 18083 1883 4370 5369 8083 8084 8883
# Tue, 02 Jul 2024 04:07:59 GMT
COPY file:f0e3faa715cc7e845bbdf3b121a4a8bad40d65e5cef1fac9f1285fec250cedf2 in /usr/bin/ 
# Tue, 02 Jul 2024 04:08:00 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 02 Jul 2024 04:08:00 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:ea235d1ccf77ca07a545b448996766dc3eca4b971b04ba39d50af69660b25751`  
		Last Modified: Tue, 02 Jul 2024 00:42:25 GMT  
		Size: 29.2 MB (29156563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51c44934ae8ca03950296a4539a08b216eef45c351b694b9232d93161d83368e`  
		Last Modified: Tue, 02 Jul 2024 04:09:48 GMT  
		Size: 93.7 MB (93660768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa2ba6b94a2eb3de1a86a522cc9e627fe013fcaff6ff730bb4f6828ab2b51dba`  
		Last Modified: Tue, 02 Jul 2024 04:09:40 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
