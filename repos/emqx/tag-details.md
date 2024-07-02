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
$ docker pull emqx@sha256:9b3f31a262ccb09ca2286f6458672cc42f006bd1a97a97315c6e08111074ae78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5` - linux; amd64

```console
$ docker pull emqx@sha256:15456b72c9d1cb61b56a7a1ce0857909ee9fc9ebad8419378a81add3adb6ed15
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.2 MB (126241662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00e77fc8b626c1b9f206306128246eb5dfacc19cbdbf5fc1d9f63e8e87bd1d06`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 02 Jul 2024 01:25:02 GMT
ADD file:b24689567a7c604de93e4ef1dc87c372514f692556744da43925c575b4f80df6 in / 
# Tue, 02 Jul 2024 01:25:02 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 05:12:43 GMT
ENV EMQX_VERSION=5.7.1
# Tue, 02 Jul 2024 05:12:43 GMT
ENV AMD64_SHA256=6896263e24c1211fea0e15464afb39931e9b4c7139804e0a6fb5f143826efaf8
# Tue, 02 Jul 2024 05:12:43 GMT
ENV ARM64_SHA256=c321477bab28e381a472761c2d62f9e5acf6290f298f5aaf9404ab70feb6d587
# Tue, 02 Jul 2024 05:12:43 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 02 Jul 2024 05:12:58 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Tue, 02 Jul 2024 05:12:59 GMT
WORKDIR /opt/emqx
# Tue, 02 Jul 2024 05:12:59 GMT
USER emqx
# Tue, 02 Jul 2024 05:12:59 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 02 Jul 2024 05:12:59 GMT
EXPOSE 18083 1883 4370 5369 8083 8084 8883
# Tue, 02 Jul 2024 05:13:00 GMT
COPY file:f0e3faa715cc7e845bbdf3b121a4a8bad40d65e5cef1fac9f1285fec250cedf2 in /usr/bin/ 
# Tue, 02 Jul 2024 05:13:00 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 02 Jul 2024 05:13:00 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:f11c1adaa26e078479ccdd45312ea3b88476441b91be0ec898a7e07bfd05badc`  
		Last Modified: Tue, 02 Jul 2024 01:28:49 GMT  
		Size: 29.1 MB (29126278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1196d7aba6f1e9c7c461f95948e03afe739ab4078c2ace0d2d2985fc7be16227`  
		Last Modified: Tue, 02 Jul 2024 05:14:57 GMT  
		Size: 97.1 MB (97114351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66dd426bb64ae176d26b1300ae5ec1d4474edbf7f6c5938fc127b680feb3c35c`  
		Last Modified: Tue, 02 Jul 2024 05:14:48 GMT  
		Size: 1.0 KB (1033 bytes)  
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
$ docker pull emqx@sha256:33e5458ba851a2cef0b655418e18d380f2c342aca2cb029878262db8fc23cf28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5.1` - linux; amd64

```console
$ docker pull emqx@sha256:14565ae1f88be9e77554b1ab9a337a96ab8aeb135051fb657b80fbdefa4e92ad
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.4 MB (102396908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83ebfb2a7cc99b4da1d4486f3fb9a5b6d59506413427b9744242646827fc44ba`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 02 Jul 2024 01:25:24 GMT
ADD file:49759b7a74bac875e3619e20ed5a9521101c7729f601d90976d0755d30e97499 in / 
# Tue, 02 Jul 2024 01:25:24 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 05:10:52 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 05:10:52 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Tue, 02 Jul 2024 05:10:52 GMT
ENV EMQX_VERSION=5.1.6
# Tue, 02 Jul 2024 05:10:52 GMT
ENV AMD64_SHA256=5c65f7538141e93d71d1dd7d088589339ef6a091b90f901604a2e0e004f5f4aa
# Tue, 02 Jul 2024 05:10:52 GMT
ENV ARM64_SHA256=ae832d29d6b4e7fa43f3bf04c8c9fad4c9047f079d1587d3ed2a3564d5ea8147
# Tue, 02 Jul 2024 05:10:53 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 02 Jul 2024 05:10:59 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg
# Tue, 02 Jul 2024 05:11:00 GMT
WORKDIR /opt/emqx
# Tue, 02 Jul 2024 05:11:00 GMT
USER emqx
# Tue, 02 Jul 2024 05:11:00 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 02 Jul 2024 05:11:00 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Tue, 02 Jul 2024 05:11:00 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Tue, 02 Jul 2024 05:11:00 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 02 Jul 2024 05:11:00 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:76956b537f14770ffd78afbe4f17016b2794c4b9b568325e8079089ea5c4e8cd`  
		Last Modified: Tue, 02 Jul 2024 01:29:27 GMT  
		Size: 31.4 MB (31422284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe777f634d47d0903fb0bf6fb13967bc465e8487da0311750511f774c2900549`  
		Last Modified: Tue, 02 Jul 2024 05:13:14 GMT  
		Size: 3.0 MB (2988349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:655fb377bdf7395b0d3335bc8d7e9f00280b311eb6eb513bb38baca1b4918936`  
		Last Modified: Tue, 02 Jul 2024 05:13:14 GMT  
		Size: 4.1 KB (4077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da63eb6968b725e589692ae895218d8a309ada5f312a51cbbdeb34f7afc5079b`  
		Last Modified: Tue, 02 Jul 2024 05:13:21 GMT  
		Size: 68.0 MB (67981296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67b41babc1c67658c529c0b85427fd3aa28758866844243d941f013adb840fa2`  
		Last Modified: Tue, 02 Jul 2024 05:13:14 GMT  
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
$ docker pull emqx@sha256:33e5458ba851a2cef0b655418e18d380f2c342aca2cb029878262db8fc23cf28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5.1.6` - linux; amd64

```console
$ docker pull emqx@sha256:14565ae1f88be9e77554b1ab9a337a96ab8aeb135051fb657b80fbdefa4e92ad
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.4 MB (102396908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83ebfb2a7cc99b4da1d4486f3fb9a5b6d59506413427b9744242646827fc44ba`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 02 Jul 2024 01:25:24 GMT
ADD file:49759b7a74bac875e3619e20ed5a9521101c7729f601d90976d0755d30e97499 in / 
# Tue, 02 Jul 2024 01:25:24 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 05:10:52 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 05:10:52 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Tue, 02 Jul 2024 05:10:52 GMT
ENV EMQX_VERSION=5.1.6
# Tue, 02 Jul 2024 05:10:52 GMT
ENV AMD64_SHA256=5c65f7538141e93d71d1dd7d088589339ef6a091b90f901604a2e0e004f5f4aa
# Tue, 02 Jul 2024 05:10:52 GMT
ENV ARM64_SHA256=ae832d29d6b4e7fa43f3bf04c8c9fad4c9047f079d1587d3ed2a3564d5ea8147
# Tue, 02 Jul 2024 05:10:53 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 02 Jul 2024 05:10:59 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg
# Tue, 02 Jul 2024 05:11:00 GMT
WORKDIR /opt/emqx
# Tue, 02 Jul 2024 05:11:00 GMT
USER emqx
# Tue, 02 Jul 2024 05:11:00 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 02 Jul 2024 05:11:00 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Tue, 02 Jul 2024 05:11:00 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Tue, 02 Jul 2024 05:11:00 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 02 Jul 2024 05:11:00 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:76956b537f14770ffd78afbe4f17016b2794c4b9b568325e8079089ea5c4e8cd`  
		Last Modified: Tue, 02 Jul 2024 01:29:27 GMT  
		Size: 31.4 MB (31422284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe777f634d47d0903fb0bf6fb13967bc465e8487da0311750511f774c2900549`  
		Last Modified: Tue, 02 Jul 2024 05:13:14 GMT  
		Size: 3.0 MB (2988349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:655fb377bdf7395b0d3335bc8d7e9f00280b311eb6eb513bb38baca1b4918936`  
		Last Modified: Tue, 02 Jul 2024 05:13:14 GMT  
		Size: 4.1 KB (4077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da63eb6968b725e589692ae895218d8a309ada5f312a51cbbdeb34f7afc5079b`  
		Last Modified: Tue, 02 Jul 2024 05:13:21 GMT  
		Size: 68.0 MB (67981296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67b41babc1c67658c529c0b85427fd3aa28758866844243d941f013adb840fa2`  
		Last Modified: Tue, 02 Jul 2024 05:13:14 GMT  
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
$ docker pull emqx@sha256:872bce6d44d531ded1beb5bc88d03b819549c2af12a7eaf325963fb89b8ee19e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5.2` - linux; amd64

```console
$ docker pull emqx@sha256:0bd000657286c1cf57a3e051ea246fe540449c46d1ae301cb5e7a21da9efe6ee
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.2 MB (101167115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96c9dbd6bd528cc41d138067b09f20a3098e6fafe5890f88df450f19b8707b54`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 02 Jul 2024 01:25:24 GMT
ADD file:49759b7a74bac875e3619e20ed5a9521101c7729f601d90976d0755d30e97499 in / 
# Tue, 02 Jul 2024 01:25:24 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 05:11:08 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 05:11:09 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Tue, 02 Jul 2024 05:11:09 GMT
ENV EMQX_VERSION=5.2.1
# Tue, 02 Jul 2024 05:11:09 GMT
ENV AMD64_SHA256=359a12811e5e6725e4269d9484abd348effdde35c0f2af1f5b63cae790c73020
# Tue, 02 Jul 2024 05:11:09 GMT
ENV ARM64_SHA256=2e0a3e0b33669c9b6da488970a2f92d08d7bd0824295822b205b83461ba4728d
# Tue, 02 Jul 2024 05:11:09 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 02 Jul 2024 05:11:19 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl;     rm -rf /var/lib/apt/lists/*;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl
# Tue, 02 Jul 2024 05:11:20 GMT
WORKDIR /opt/emqx
# Tue, 02 Jul 2024 05:11:20 GMT
USER emqx
# Tue, 02 Jul 2024 05:11:20 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 02 Jul 2024 05:11:20 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Tue, 02 Jul 2024 05:11:20 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Tue, 02 Jul 2024 05:11:20 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 02 Jul 2024 05:11:20 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:76956b537f14770ffd78afbe4f17016b2794c4b9b568325e8079089ea5c4e8cd`  
		Last Modified: Tue, 02 Jul 2024 01:29:27 GMT  
		Size: 31.4 MB (31422284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3710d15ae0b621974802f3f4bc77fffbf7322e678682b0e13981cce124050046`  
		Last Modified: Tue, 02 Jul 2024 05:13:30 GMT  
		Size: 1.6 MB (1629584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a4e596f16c808306590723849e1bedc519d3a0738f004dcffb924643b10b39f`  
		Last Modified: Tue, 02 Jul 2024 05:13:30 GMT  
		Size: 4.1 KB (4071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7b15b97e095605dc2bc33844ed1f307436982cf79e3f714b0f3a27edf7bff80`  
		Last Modified: Tue, 02 Jul 2024 05:13:37 GMT  
		Size: 68.1 MB (68110274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:991d44276344a59732562607ae13b7ec7307d78aaf76d55383e404c82094959d`  
		Last Modified: Tue, 02 Jul 2024 05:13:30 GMT  
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
$ docker pull emqx@sha256:872bce6d44d531ded1beb5bc88d03b819549c2af12a7eaf325963fb89b8ee19e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5.2.1` - linux; amd64

```console
$ docker pull emqx@sha256:0bd000657286c1cf57a3e051ea246fe540449c46d1ae301cb5e7a21da9efe6ee
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.2 MB (101167115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96c9dbd6bd528cc41d138067b09f20a3098e6fafe5890f88df450f19b8707b54`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 02 Jul 2024 01:25:24 GMT
ADD file:49759b7a74bac875e3619e20ed5a9521101c7729f601d90976d0755d30e97499 in / 
# Tue, 02 Jul 2024 01:25:24 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 05:11:08 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 05:11:09 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Tue, 02 Jul 2024 05:11:09 GMT
ENV EMQX_VERSION=5.2.1
# Tue, 02 Jul 2024 05:11:09 GMT
ENV AMD64_SHA256=359a12811e5e6725e4269d9484abd348effdde35c0f2af1f5b63cae790c73020
# Tue, 02 Jul 2024 05:11:09 GMT
ENV ARM64_SHA256=2e0a3e0b33669c9b6da488970a2f92d08d7bd0824295822b205b83461ba4728d
# Tue, 02 Jul 2024 05:11:09 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 02 Jul 2024 05:11:19 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl;     rm -rf /var/lib/apt/lists/*;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl
# Tue, 02 Jul 2024 05:11:20 GMT
WORKDIR /opt/emqx
# Tue, 02 Jul 2024 05:11:20 GMT
USER emqx
# Tue, 02 Jul 2024 05:11:20 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 02 Jul 2024 05:11:20 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Tue, 02 Jul 2024 05:11:20 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Tue, 02 Jul 2024 05:11:20 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 02 Jul 2024 05:11:20 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:76956b537f14770ffd78afbe4f17016b2794c4b9b568325e8079089ea5c4e8cd`  
		Last Modified: Tue, 02 Jul 2024 01:29:27 GMT  
		Size: 31.4 MB (31422284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3710d15ae0b621974802f3f4bc77fffbf7322e678682b0e13981cce124050046`  
		Last Modified: Tue, 02 Jul 2024 05:13:30 GMT  
		Size: 1.6 MB (1629584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a4e596f16c808306590723849e1bedc519d3a0738f004dcffb924643b10b39f`  
		Last Modified: Tue, 02 Jul 2024 05:13:30 GMT  
		Size: 4.1 KB (4071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7b15b97e095605dc2bc33844ed1f307436982cf79e3f714b0f3a27edf7bff80`  
		Last Modified: Tue, 02 Jul 2024 05:13:37 GMT  
		Size: 68.1 MB (68110274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:991d44276344a59732562607ae13b7ec7307d78aaf76d55383e404c82094959d`  
		Last Modified: Tue, 02 Jul 2024 05:13:30 GMT  
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
$ docker pull emqx@sha256:cbcc158ba979290dfa30aec08d1489659cc9fafc597aa383c6a2ca0d742384a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5.3` - linux; amd64

```console
$ docker pull emqx@sha256:4b9301217a0efddfe2b07cdb53a9e6774c9a7865afe813d4062928adfc042e90
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.8 MB (101783054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b55d1b5d3c5e4aa687f047c3bb1852ce2fc6b6b32d792955b39d037bca1e36b`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 02 Jul 2024 01:25:24 GMT
ADD file:49759b7a74bac875e3619e20ed5a9521101c7729f601d90976d0755d30e97499 in / 
# Tue, 02 Jul 2024 01:25:24 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 05:11:24 GMT
ENV EMQX_VERSION=5.3.2
# Tue, 02 Jul 2024 05:11:24 GMT
ENV AMD64_SHA256=d5948d4171f57e77756dd6c9eeb745c39e391e75aad3798fce445f44f5690be0
# Tue, 02 Jul 2024 05:11:24 GMT
ENV ARM64_SHA256=82b056bb1c1cd1f16e9d0719150fa8ac19c499d29563738bcd6984b3c395c6ac
# Tue, 02 Jul 2024 05:11:24 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 02 Jul 2024 05:11:38 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 05:11:39 GMT
WORKDIR /opt/emqx
# Tue, 02 Jul 2024 05:11:39 GMT
USER emqx
# Tue, 02 Jul 2024 05:11:39 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 02 Jul 2024 05:11:39 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Tue, 02 Jul 2024 05:11:39 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Tue, 02 Jul 2024 05:11:39 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 02 Jul 2024 05:11:40 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:76956b537f14770ffd78afbe4f17016b2794c4b9b568325e8079089ea5c4e8cd`  
		Last Modified: Tue, 02 Jul 2024 01:29:27 GMT  
		Size: 31.4 MB (31422284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1261c945a62f7ef559c06042f3d5986b4b33e2103952c70e3095e9b6ef8ee282`  
		Last Modified: Tue, 02 Jul 2024 05:13:51 GMT  
		Size: 70.4 MB (70359868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3e9456d2b5c0df8a82df46022b442e86f5a6a98cf112e083fb3e8684a6e1d35`  
		Last Modified: Tue, 02 Jul 2024 05:13:44 GMT  
		Size: 902.0 B  
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
$ docker pull emqx@sha256:cbcc158ba979290dfa30aec08d1489659cc9fafc597aa383c6a2ca0d742384a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5.3.2` - linux; amd64

```console
$ docker pull emqx@sha256:4b9301217a0efddfe2b07cdb53a9e6774c9a7865afe813d4062928adfc042e90
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.8 MB (101783054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b55d1b5d3c5e4aa687f047c3bb1852ce2fc6b6b32d792955b39d037bca1e36b`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 02 Jul 2024 01:25:24 GMT
ADD file:49759b7a74bac875e3619e20ed5a9521101c7729f601d90976d0755d30e97499 in / 
# Tue, 02 Jul 2024 01:25:24 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 05:11:24 GMT
ENV EMQX_VERSION=5.3.2
# Tue, 02 Jul 2024 05:11:24 GMT
ENV AMD64_SHA256=d5948d4171f57e77756dd6c9eeb745c39e391e75aad3798fce445f44f5690be0
# Tue, 02 Jul 2024 05:11:24 GMT
ENV ARM64_SHA256=82b056bb1c1cd1f16e9d0719150fa8ac19c499d29563738bcd6984b3c395c6ac
# Tue, 02 Jul 2024 05:11:24 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 02 Jul 2024 05:11:38 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 05:11:39 GMT
WORKDIR /opt/emqx
# Tue, 02 Jul 2024 05:11:39 GMT
USER emqx
# Tue, 02 Jul 2024 05:11:39 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 02 Jul 2024 05:11:39 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Tue, 02 Jul 2024 05:11:39 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Tue, 02 Jul 2024 05:11:39 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 02 Jul 2024 05:11:40 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:76956b537f14770ffd78afbe4f17016b2794c4b9b568325e8079089ea5c4e8cd`  
		Last Modified: Tue, 02 Jul 2024 01:29:27 GMT  
		Size: 31.4 MB (31422284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1261c945a62f7ef559c06042f3d5986b4b33e2103952c70e3095e9b6ef8ee282`  
		Last Modified: Tue, 02 Jul 2024 05:13:51 GMT  
		Size: 70.4 MB (70359868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3e9456d2b5c0df8a82df46022b442e86f5a6a98cf112e083fb3e8684a6e1d35`  
		Last Modified: Tue, 02 Jul 2024 05:13:44 GMT  
		Size: 902.0 B  
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
$ docker pull emqx@sha256:4b0e1ab55d4b9809b009591ec83993d8e4bdf2ac3c169250d0891452759a907f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5.4` - linux; amd64

```console
$ docker pull emqx@sha256:42955a6741f75b63882948d817ae857cee22a431298abae0936c55cd6a210d74
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.7 MB (118697894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ffce97cef3d26392e187a4ec614bc3853fc016e1afd6954915043e6b1e681fe`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 02 Jul 2024 01:25:24 GMT
ADD file:49759b7a74bac875e3619e20ed5a9521101c7729f601d90976d0755d30e97499 in / 
# Tue, 02 Jul 2024 01:25:24 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 05:11:44 GMT
ENV EMQX_VERSION=5.4.1
# Tue, 02 Jul 2024 05:11:45 GMT
ENV AMD64_SHA256=c2087651d72f17999f52d73ff22cd8f23dc5fa5db8b5a90a8bc4a1410b03affb
# Tue, 02 Jul 2024 05:11:45 GMT
ENV ARM64_SHA256=6c53a68ae907f7b4a3cdcd4dbee4f839b07853695ac1c039b51fd97d993073bc
# Tue, 02 Jul 2024 05:11:45 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 02 Jul 2024 05:11:59 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 05:12:00 GMT
WORKDIR /opt/emqx
# Tue, 02 Jul 2024 05:12:00 GMT
USER emqx
# Tue, 02 Jul 2024 05:12:00 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 02 Jul 2024 05:12:00 GMT
EXPOSE 18083 1883 4370 5369 8083 8084 8883
# Tue, 02 Jul 2024 05:12:00 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Tue, 02 Jul 2024 05:12:00 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 02 Jul 2024 05:12:00 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:76956b537f14770ffd78afbe4f17016b2794c4b9b568325e8079089ea5c4e8cd`  
		Last Modified: Tue, 02 Jul 2024 01:29:27 GMT  
		Size: 31.4 MB (31422284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c500b6dd8d8ca0cbc623c6af89a7079c1cc7578e38f1d0c3672e480981e81b76`  
		Last Modified: Tue, 02 Jul 2024 05:14:07 GMT  
		Size: 87.3 MB (87274711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eade092beaf0415793194de00c07f80f8409a411920f36478cbf1ed04a48b56e`  
		Last Modified: Tue, 02 Jul 2024 05:13:58 GMT  
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
$ docker pull emqx@sha256:4b0e1ab55d4b9809b009591ec83993d8e4bdf2ac3c169250d0891452759a907f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5.4.1` - linux; amd64

```console
$ docker pull emqx@sha256:42955a6741f75b63882948d817ae857cee22a431298abae0936c55cd6a210d74
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.7 MB (118697894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ffce97cef3d26392e187a4ec614bc3853fc016e1afd6954915043e6b1e681fe`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 02 Jul 2024 01:25:24 GMT
ADD file:49759b7a74bac875e3619e20ed5a9521101c7729f601d90976d0755d30e97499 in / 
# Tue, 02 Jul 2024 01:25:24 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 05:11:44 GMT
ENV EMQX_VERSION=5.4.1
# Tue, 02 Jul 2024 05:11:45 GMT
ENV AMD64_SHA256=c2087651d72f17999f52d73ff22cd8f23dc5fa5db8b5a90a8bc4a1410b03affb
# Tue, 02 Jul 2024 05:11:45 GMT
ENV ARM64_SHA256=6c53a68ae907f7b4a3cdcd4dbee4f839b07853695ac1c039b51fd97d993073bc
# Tue, 02 Jul 2024 05:11:45 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 02 Jul 2024 05:11:59 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 05:12:00 GMT
WORKDIR /opt/emqx
# Tue, 02 Jul 2024 05:12:00 GMT
USER emqx
# Tue, 02 Jul 2024 05:12:00 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 02 Jul 2024 05:12:00 GMT
EXPOSE 18083 1883 4370 5369 8083 8084 8883
# Tue, 02 Jul 2024 05:12:00 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Tue, 02 Jul 2024 05:12:00 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 02 Jul 2024 05:12:00 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:76956b537f14770ffd78afbe4f17016b2794c4b9b568325e8079089ea5c4e8cd`  
		Last Modified: Tue, 02 Jul 2024 01:29:27 GMT  
		Size: 31.4 MB (31422284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c500b6dd8d8ca0cbc623c6af89a7079c1cc7578e38f1d0c3672e480981e81b76`  
		Last Modified: Tue, 02 Jul 2024 05:14:07 GMT  
		Size: 87.3 MB (87274711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eade092beaf0415793194de00c07f80f8409a411920f36478cbf1ed04a48b56e`  
		Last Modified: Tue, 02 Jul 2024 05:13:58 GMT  
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
$ docker pull emqx@sha256:5fcf8a55a20568edad2d5227b2e53df349a7248dd78fc34dc59317122c154ba3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5.5` - linux; amd64

```console
$ docker pull emqx@sha256:999e0b2ecaebac7714b26e0c5caac6256cd51d099543d50d03a69fd15f8b88fb
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.3 MB (121262952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37388df384f5b48e1c32ca9350ef171d971af74e307a24745ad7f5db892c01f7`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 02 Jul 2024 01:25:24 GMT
ADD file:49759b7a74bac875e3619e20ed5a9521101c7729f601d90976d0755d30e97499 in / 
# Tue, 02 Jul 2024 01:25:24 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 05:12:05 GMT
ENV EMQX_VERSION=5.5.1
# Tue, 02 Jul 2024 05:12:05 GMT
ENV AMD64_SHA256=8bac2886987a632aab1c738aa3de28684b415d3b1e1f9489b458c819254673a6
# Tue, 02 Jul 2024 05:12:05 GMT
ENV ARM64_SHA256=8b962ad8beea50fb92dc0b93d2ab8a5064752147b70bbf46fd221bc4cc29c32d
# Tue, 02 Jul 2024 05:12:05 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 02 Jul 2024 05:12:20 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     mkdir -p /opt/emqx/log /opt/emqx/data /opt/emqx/plugins;     chown -R emqx:emqx /opt/emqx/log /opt/emqx/data /opt/emqx/plugins;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Tue, 02 Jul 2024 05:12:21 GMT
WORKDIR /opt/emqx
# Tue, 02 Jul 2024 05:12:21 GMT
USER emqx
# Tue, 02 Jul 2024 05:12:21 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 02 Jul 2024 05:12:21 GMT
EXPOSE 18083 1883 4370 5369 8083 8084 8883
# Tue, 02 Jul 2024 05:12:21 GMT
COPY file:f0e3faa715cc7e845bbdf3b121a4a8bad40d65e5cef1fac9f1285fec250cedf2 in /usr/bin/ 
# Tue, 02 Jul 2024 05:12:21 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 02 Jul 2024 05:12:22 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:76956b537f14770ffd78afbe4f17016b2794c4b9b568325e8079089ea5c4e8cd`  
		Last Modified: Tue, 02 Jul 2024 01:29:27 GMT  
		Size: 31.4 MB (31422284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2e6043e2163de61203ae65be71d96b57a4a6c820cf1fcbe617f2c166653d3e1`  
		Last Modified: Tue, 02 Jul 2024 05:14:23 GMT  
		Size: 89.8 MB (89839639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a45b7094f4d380d350586ce15dcaa9d7d99de769afd539dcc93fd7a30cda9fa3`  
		Last Modified: Tue, 02 Jul 2024 05:14:14 GMT  
		Size: 1.0 KB (1029 bytes)  
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
$ docker pull emqx@sha256:5fcf8a55a20568edad2d5227b2e53df349a7248dd78fc34dc59317122c154ba3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5.5.1` - linux; amd64

```console
$ docker pull emqx@sha256:999e0b2ecaebac7714b26e0c5caac6256cd51d099543d50d03a69fd15f8b88fb
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.3 MB (121262952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37388df384f5b48e1c32ca9350ef171d971af74e307a24745ad7f5db892c01f7`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 02 Jul 2024 01:25:24 GMT
ADD file:49759b7a74bac875e3619e20ed5a9521101c7729f601d90976d0755d30e97499 in / 
# Tue, 02 Jul 2024 01:25:24 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 05:12:05 GMT
ENV EMQX_VERSION=5.5.1
# Tue, 02 Jul 2024 05:12:05 GMT
ENV AMD64_SHA256=8bac2886987a632aab1c738aa3de28684b415d3b1e1f9489b458c819254673a6
# Tue, 02 Jul 2024 05:12:05 GMT
ENV ARM64_SHA256=8b962ad8beea50fb92dc0b93d2ab8a5064752147b70bbf46fd221bc4cc29c32d
# Tue, 02 Jul 2024 05:12:05 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 02 Jul 2024 05:12:20 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     mkdir -p /opt/emqx/log /opt/emqx/data /opt/emqx/plugins;     chown -R emqx:emqx /opt/emqx/log /opt/emqx/data /opt/emqx/plugins;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Tue, 02 Jul 2024 05:12:21 GMT
WORKDIR /opt/emqx
# Tue, 02 Jul 2024 05:12:21 GMT
USER emqx
# Tue, 02 Jul 2024 05:12:21 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 02 Jul 2024 05:12:21 GMT
EXPOSE 18083 1883 4370 5369 8083 8084 8883
# Tue, 02 Jul 2024 05:12:21 GMT
COPY file:f0e3faa715cc7e845bbdf3b121a4a8bad40d65e5cef1fac9f1285fec250cedf2 in /usr/bin/ 
# Tue, 02 Jul 2024 05:12:21 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 02 Jul 2024 05:12:22 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:76956b537f14770ffd78afbe4f17016b2794c4b9b568325e8079089ea5c4e8cd`  
		Last Modified: Tue, 02 Jul 2024 01:29:27 GMT  
		Size: 31.4 MB (31422284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2e6043e2163de61203ae65be71d96b57a4a6c820cf1fcbe617f2c166653d3e1`  
		Last Modified: Tue, 02 Jul 2024 05:14:23 GMT  
		Size: 89.8 MB (89839639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a45b7094f4d380d350586ce15dcaa9d7d99de769afd539dcc93fd7a30cda9fa3`  
		Last Modified: Tue, 02 Jul 2024 05:14:14 GMT  
		Size: 1.0 KB (1029 bytes)  
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
$ docker pull emqx@sha256:d752fcb30ef61b6abe977357042af51a073ec3ba072d5e89ad412012f754c27c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5.6` - linux; amd64

```console
$ docker pull emqx@sha256:2964b39d918b82b81382e908d4d79a0334e276d678f2747c7c600957fce232d9
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.2 MB (124179363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47b2d2be8a70ed439001866085d96541d84cfcee082449fd245dd04109bfd6fd`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 02 Jul 2024 01:25:02 GMT
ADD file:b24689567a7c604de93e4ef1dc87c372514f692556744da43925c575b4f80df6 in / 
# Tue, 02 Jul 2024 01:25:02 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 05:12:25 GMT
ENV EMQX_VERSION=5.6.1
# Tue, 02 Jul 2024 05:12:26 GMT
ENV AMD64_SHA256=a5be37660bfe6130bc159b934ed98ffcb9bef5519765491b4ed38d08ba304538
# Tue, 02 Jul 2024 05:12:26 GMT
ENV ARM64_SHA256=3f7f9b10d313f760af43e0a54cba2af4eb23ad3864b439196cb8b2903baf5651
# Tue, 02 Jul 2024 05:12:26 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 02 Jul 2024 05:12:38 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Tue, 02 Jul 2024 05:12:38 GMT
WORKDIR /opt/emqx
# Tue, 02 Jul 2024 05:12:39 GMT
USER emqx
# Tue, 02 Jul 2024 05:12:39 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 02 Jul 2024 05:12:39 GMT
EXPOSE 18083 1883 4370 5369 8083 8084 8883
# Tue, 02 Jul 2024 05:12:39 GMT
COPY file:f0e3faa715cc7e845bbdf3b121a4a8bad40d65e5cef1fac9f1285fec250cedf2 in /usr/bin/ 
# Tue, 02 Jul 2024 05:12:39 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 02 Jul 2024 05:12:39 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:f11c1adaa26e078479ccdd45312ea3b88476441b91be0ec898a7e07bfd05badc`  
		Last Modified: Tue, 02 Jul 2024 01:28:49 GMT  
		Size: 29.1 MB (29126278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79f30e1b7e495b6c08d67ad65bccb890c6bfa71a32a707d821df9edc08e1eefe`  
		Last Modified: Tue, 02 Jul 2024 05:14:40 GMT  
		Size: 95.1 MB (95052051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8516a646972d45a8a2be20eb1e83bbcdde3a9f841eec08358548a198f0259f87`  
		Last Modified: Tue, 02 Jul 2024 05:14:31 GMT  
		Size: 1.0 KB (1034 bytes)  
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
$ docker pull emqx@sha256:d752fcb30ef61b6abe977357042af51a073ec3ba072d5e89ad412012f754c27c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5.6.1` - linux; amd64

```console
$ docker pull emqx@sha256:2964b39d918b82b81382e908d4d79a0334e276d678f2747c7c600957fce232d9
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.2 MB (124179363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47b2d2be8a70ed439001866085d96541d84cfcee082449fd245dd04109bfd6fd`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 02 Jul 2024 01:25:02 GMT
ADD file:b24689567a7c604de93e4ef1dc87c372514f692556744da43925c575b4f80df6 in / 
# Tue, 02 Jul 2024 01:25:02 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 05:12:25 GMT
ENV EMQX_VERSION=5.6.1
# Tue, 02 Jul 2024 05:12:26 GMT
ENV AMD64_SHA256=a5be37660bfe6130bc159b934ed98ffcb9bef5519765491b4ed38d08ba304538
# Tue, 02 Jul 2024 05:12:26 GMT
ENV ARM64_SHA256=3f7f9b10d313f760af43e0a54cba2af4eb23ad3864b439196cb8b2903baf5651
# Tue, 02 Jul 2024 05:12:26 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 02 Jul 2024 05:12:38 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Tue, 02 Jul 2024 05:12:38 GMT
WORKDIR /opt/emqx
# Tue, 02 Jul 2024 05:12:39 GMT
USER emqx
# Tue, 02 Jul 2024 05:12:39 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 02 Jul 2024 05:12:39 GMT
EXPOSE 18083 1883 4370 5369 8083 8084 8883
# Tue, 02 Jul 2024 05:12:39 GMT
COPY file:f0e3faa715cc7e845bbdf3b121a4a8bad40d65e5cef1fac9f1285fec250cedf2 in /usr/bin/ 
# Tue, 02 Jul 2024 05:12:39 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 02 Jul 2024 05:12:39 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:f11c1adaa26e078479ccdd45312ea3b88476441b91be0ec898a7e07bfd05badc`  
		Last Modified: Tue, 02 Jul 2024 01:28:49 GMT  
		Size: 29.1 MB (29126278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79f30e1b7e495b6c08d67ad65bccb890c6bfa71a32a707d821df9edc08e1eefe`  
		Last Modified: Tue, 02 Jul 2024 05:14:40 GMT  
		Size: 95.1 MB (95052051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8516a646972d45a8a2be20eb1e83bbcdde3a9f841eec08358548a198f0259f87`  
		Last Modified: Tue, 02 Jul 2024 05:14:31 GMT  
		Size: 1.0 KB (1034 bytes)  
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
$ docker pull emqx@sha256:9b3f31a262ccb09ca2286f6458672cc42f006bd1a97a97315c6e08111074ae78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5.7` - linux; amd64

```console
$ docker pull emqx@sha256:15456b72c9d1cb61b56a7a1ce0857909ee9fc9ebad8419378a81add3adb6ed15
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.2 MB (126241662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00e77fc8b626c1b9f206306128246eb5dfacc19cbdbf5fc1d9f63e8e87bd1d06`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 02 Jul 2024 01:25:02 GMT
ADD file:b24689567a7c604de93e4ef1dc87c372514f692556744da43925c575b4f80df6 in / 
# Tue, 02 Jul 2024 01:25:02 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 05:12:43 GMT
ENV EMQX_VERSION=5.7.1
# Tue, 02 Jul 2024 05:12:43 GMT
ENV AMD64_SHA256=6896263e24c1211fea0e15464afb39931e9b4c7139804e0a6fb5f143826efaf8
# Tue, 02 Jul 2024 05:12:43 GMT
ENV ARM64_SHA256=c321477bab28e381a472761c2d62f9e5acf6290f298f5aaf9404ab70feb6d587
# Tue, 02 Jul 2024 05:12:43 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 02 Jul 2024 05:12:58 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Tue, 02 Jul 2024 05:12:59 GMT
WORKDIR /opt/emqx
# Tue, 02 Jul 2024 05:12:59 GMT
USER emqx
# Tue, 02 Jul 2024 05:12:59 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 02 Jul 2024 05:12:59 GMT
EXPOSE 18083 1883 4370 5369 8083 8084 8883
# Tue, 02 Jul 2024 05:13:00 GMT
COPY file:f0e3faa715cc7e845bbdf3b121a4a8bad40d65e5cef1fac9f1285fec250cedf2 in /usr/bin/ 
# Tue, 02 Jul 2024 05:13:00 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 02 Jul 2024 05:13:00 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:f11c1adaa26e078479ccdd45312ea3b88476441b91be0ec898a7e07bfd05badc`  
		Last Modified: Tue, 02 Jul 2024 01:28:49 GMT  
		Size: 29.1 MB (29126278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1196d7aba6f1e9c7c461f95948e03afe739ab4078c2ace0d2d2985fc7be16227`  
		Last Modified: Tue, 02 Jul 2024 05:14:57 GMT  
		Size: 97.1 MB (97114351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66dd426bb64ae176d26b1300ae5ec1d4474edbf7f6c5938fc127b680feb3c35c`  
		Last Modified: Tue, 02 Jul 2024 05:14:48 GMT  
		Size: 1.0 KB (1033 bytes)  
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
$ docker pull emqx@sha256:9b3f31a262ccb09ca2286f6458672cc42f006bd1a97a97315c6e08111074ae78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5.7.1` - linux; amd64

```console
$ docker pull emqx@sha256:15456b72c9d1cb61b56a7a1ce0857909ee9fc9ebad8419378a81add3adb6ed15
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.2 MB (126241662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00e77fc8b626c1b9f206306128246eb5dfacc19cbdbf5fc1d9f63e8e87bd1d06`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 02 Jul 2024 01:25:02 GMT
ADD file:b24689567a7c604de93e4ef1dc87c372514f692556744da43925c575b4f80df6 in / 
# Tue, 02 Jul 2024 01:25:02 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 05:12:43 GMT
ENV EMQX_VERSION=5.7.1
# Tue, 02 Jul 2024 05:12:43 GMT
ENV AMD64_SHA256=6896263e24c1211fea0e15464afb39931e9b4c7139804e0a6fb5f143826efaf8
# Tue, 02 Jul 2024 05:12:43 GMT
ENV ARM64_SHA256=c321477bab28e381a472761c2d62f9e5acf6290f298f5aaf9404ab70feb6d587
# Tue, 02 Jul 2024 05:12:43 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 02 Jul 2024 05:12:58 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Tue, 02 Jul 2024 05:12:59 GMT
WORKDIR /opt/emqx
# Tue, 02 Jul 2024 05:12:59 GMT
USER emqx
# Tue, 02 Jul 2024 05:12:59 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 02 Jul 2024 05:12:59 GMT
EXPOSE 18083 1883 4370 5369 8083 8084 8883
# Tue, 02 Jul 2024 05:13:00 GMT
COPY file:f0e3faa715cc7e845bbdf3b121a4a8bad40d65e5cef1fac9f1285fec250cedf2 in /usr/bin/ 
# Tue, 02 Jul 2024 05:13:00 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 02 Jul 2024 05:13:00 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:f11c1adaa26e078479ccdd45312ea3b88476441b91be0ec898a7e07bfd05badc`  
		Last Modified: Tue, 02 Jul 2024 01:28:49 GMT  
		Size: 29.1 MB (29126278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1196d7aba6f1e9c7c461f95948e03afe739ab4078c2ace0d2d2985fc7be16227`  
		Last Modified: Tue, 02 Jul 2024 05:14:57 GMT  
		Size: 97.1 MB (97114351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66dd426bb64ae176d26b1300ae5ec1d4474edbf7f6c5938fc127b680feb3c35c`  
		Last Modified: Tue, 02 Jul 2024 05:14:48 GMT  
		Size: 1.0 KB (1033 bytes)  
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
$ docker pull emqx@sha256:9b3f31a262ccb09ca2286f6458672cc42f006bd1a97a97315c6e08111074ae78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:latest` - linux; amd64

```console
$ docker pull emqx@sha256:15456b72c9d1cb61b56a7a1ce0857909ee9fc9ebad8419378a81add3adb6ed15
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.2 MB (126241662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00e77fc8b626c1b9f206306128246eb5dfacc19cbdbf5fc1d9f63e8e87bd1d06`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 02 Jul 2024 01:25:02 GMT
ADD file:b24689567a7c604de93e4ef1dc87c372514f692556744da43925c575b4f80df6 in / 
# Tue, 02 Jul 2024 01:25:02 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 05:12:43 GMT
ENV EMQX_VERSION=5.7.1
# Tue, 02 Jul 2024 05:12:43 GMT
ENV AMD64_SHA256=6896263e24c1211fea0e15464afb39931e9b4c7139804e0a6fb5f143826efaf8
# Tue, 02 Jul 2024 05:12:43 GMT
ENV ARM64_SHA256=c321477bab28e381a472761c2d62f9e5acf6290f298f5aaf9404ab70feb6d587
# Tue, 02 Jul 2024 05:12:43 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 02 Jul 2024 05:12:58 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Tue, 02 Jul 2024 05:12:59 GMT
WORKDIR /opt/emqx
# Tue, 02 Jul 2024 05:12:59 GMT
USER emqx
# Tue, 02 Jul 2024 05:12:59 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 02 Jul 2024 05:12:59 GMT
EXPOSE 18083 1883 4370 5369 8083 8084 8883
# Tue, 02 Jul 2024 05:13:00 GMT
COPY file:f0e3faa715cc7e845bbdf3b121a4a8bad40d65e5cef1fac9f1285fec250cedf2 in /usr/bin/ 
# Tue, 02 Jul 2024 05:13:00 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 02 Jul 2024 05:13:00 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:f11c1adaa26e078479ccdd45312ea3b88476441b91be0ec898a7e07bfd05badc`  
		Last Modified: Tue, 02 Jul 2024 01:28:49 GMT  
		Size: 29.1 MB (29126278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1196d7aba6f1e9c7c461f95948e03afe739ab4078c2ace0d2d2985fc7be16227`  
		Last Modified: Tue, 02 Jul 2024 05:14:57 GMT  
		Size: 97.1 MB (97114351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66dd426bb64ae176d26b1300ae5ec1d4474edbf7f6c5938fc127b680feb3c35c`  
		Last Modified: Tue, 02 Jul 2024 05:14:48 GMT  
		Size: 1.0 KB (1033 bytes)  
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
