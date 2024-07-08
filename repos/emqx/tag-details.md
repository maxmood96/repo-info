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
$ docker pull emqx@sha256:34d1e4eb60a8388c0e81cb51437f49cfdc82173bfa19bb6657bb3b71278f1a29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	unknown; unknown

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
$ docker pull emqx@sha256:074ff8d864916263abc6e8c42120a7efa67fea641cb6a3a070a3614a2c5b66d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.8 MB (122815523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:573da311dffd01ef129754dc5a68bc6494d88d070bb031800b6881927091e973`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Thu, 27 Jun 2024 06:50:32 GMT
ADD file:cbda549b25cd4337cd3ce345e3b66c0d3b43c247d7315906a028f98a56c41f1d in / 
# Thu, 27 Jun 2024 06:50:32 GMT
CMD ["bash"]
# Thu, 27 Jun 2024 06:50:32 GMT
ENV EMQX_VERSION=5.7.1
# Thu, 27 Jun 2024 06:50:32 GMT
ENV AMD64_SHA256=6896263e24c1211fea0e15464afb39931e9b4c7139804e0a6fb5f143826efaf8
# Thu, 27 Jun 2024 06:50:32 GMT
ENV ARM64_SHA256=c321477bab28e381a472761c2d62f9e5acf6290f298f5aaf9404ab70feb6d587
# Thu, 27 Jun 2024 06:50:32 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Thu, 27 Jun 2024 06:50:32 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Thu, 27 Jun 2024 06:50:32 GMT
WORKDIR /opt/emqx
# Thu, 27 Jun 2024 06:50:32 GMT
USER emqx
# Thu, 27 Jun 2024 06:50:32 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Thu, 27 Jun 2024 06:50:32 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Thu, 27 Jun 2024 06:50:32 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Thu, 27 Jun 2024 06:50:32 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Thu, 27 Jun 2024 06:50:32 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:ea235d1ccf77ca07a545b448996766dc3eca4b971b04ba39d50af69660b25751`  
		Last Modified: Tue, 02 Jul 2024 00:42:25 GMT  
		Size: 29.2 MB (29156563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b31646db1381832e88900fde1500ba647e8458191411a4d10dcc4c8becfe406`  
		Last Modified: Mon, 08 Jul 2024 19:14:23 GMT  
		Size: 93.7 MB (93657896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:762d975f3920ce02bd4da5ca7a8fdc83b4f8f921649f9451c80a10c3edccf678`  
		Last Modified: Mon, 08 Jul 2024 19:14:20 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5` - unknown; unknown

```console
$ docker pull emqx@sha256:dd3bbbb96dcc4b68baf65342c6a21b9823d447ab4b1885e31b16f99167788509
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2572375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb517a98e5b34cd172b0be13bd95c2cf36068984db6969a8c563accb9a671403`

```dockerfile
```

-	Layers:
	-	`sha256:5dd0ef27adb8bfba84a8a3bbd60855144597953b9ee86a6b30793bdc44cdb30c`  
		Last Modified: Mon, 08 Jul 2024 19:14:21 GMT  
		Size: 2.6 MB (2559768 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b57ba143a92dd352085be44c5cc683e7846827132d92ab0aa6c287b80b3d3ac`  
		Last Modified: Mon, 08 Jul 2024 19:14:20 GMT  
		Size: 12.6 KB (12607 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.1`

```console
$ docker pull emqx@sha256:565682578cd04ae459ed9e1388feff2fe6903ce0bf35bf70425164f90601f71d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	unknown; unknown

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
$ docker pull emqx@sha256:cada4e0bebc80733ea8b2deaaa4c17b8b89b7ecae41eb72037d86975677b7b93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.7 MB (92698712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb76131bb270212955ab13689d623955acc25a8bad1f4b6ff667d46ee4c122c2`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 05 Sep 2023 13:05:03 GMT
ADD file:17d80cdc7d7b37786a32ac4e261c7d17cd4d80248ae39f9574ab5a6bf6a2707c in / 
# Tue, 05 Sep 2023 13:05:03 GMT
CMD ["bash"]
# Tue, 05 Sep 2023 13:05:03 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Sep 2023 13:05:03 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx; # buildkit
# Tue, 05 Sep 2023 13:05:03 GMT
ENV EMQX_VERSION=5.1.6
# Tue, 05 Sep 2023 13:05:03 GMT
ENV AMD64_SHA256=5c65f7538141e93d71d1dd7d088589339ef6a091b90f901604a2e0e004f5f4aa
# Tue, 05 Sep 2023 13:05:03 GMT
ENV ARM64_SHA256=ae832d29d6b4e7fa43f3bf04c8c9fad4c9047f079d1587d3ed2a3564d5ea8147
# Tue, 05 Sep 2023 13:05:03 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 05 Sep 2023 13:05:03 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg # buildkit
# Tue, 05 Sep 2023 13:05:03 GMT
WORKDIR /opt/emqx
# Tue, 05 Sep 2023 13:05:03 GMT
USER emqx
# Tue, 05 Sep 2023 13:05:03 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 05 Sep 2023 13:05:03 GMT
EXPOSE map[11883/tcp:{} 18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Tue, 05 Sep 2023 13:05:03 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Tue, 05 Sep 2023 13:05:03 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 05 Sep 2023 13:05:03 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:d13ad33c16eef01d20d5563bfb2ec4f25c0d12699b40cdab418e47b88d2f02e2`  
		Last Modified: Tue, 02 Jul 2024 00:43:04 GMT  
		Size: 30.1 MB (30069615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a47fc32e1771420c513826f66af1965425d7fde637f9df85e79c88abcf9df8f4`  
		Last Modified: Mon, 08 Jul 2024 19:10:27 GMT  
		Size: 3.0 MB (3003825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30abb6da25a89b034369ea57a7b6f06a4b59035a842b59538e0b0c9b70412159`  
		Last Modified: Mon, 08 Jul 2024 19:10:27 GMT  
		Size: 4.0 KB (3998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bcbc9c4ef2388a1d129a01b42394a636072b082259312c8de48ca08ec4341e4`  
		Last Modified: Mon, 08 Jul 2024 19:10:28 GMT  
		Size: 59.6 MB (59620341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:442fe0e0448c7bbd97e338110a8b195ab0aa51764677f1519f6e668b821d7d97`  
		Last Modified: Mon, 08 Jul 2024 19:10:27 GMT  
		Size: 901.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.1` - unknown; unknown

```console
$ docker pull emqx@sha256:a7758fa95ff78651af4b5807080d88ecb614e10124348dc840d3627821a3ab03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2837769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8eb74e25ec6582b18ce5c04a69587822c751bd640c95ac9ff32b440b4b16d3c3`

```dockerfile
```

-	Layers:
	-	`sha256:39de6641d6a29c6221c008ff83be6625a111c57ee1f3a985bf449f2ad286e61c`  
		Last Modified: Mon, 08 Jul 2024 19:10:27 GMT  
		Size: 2.8 MB (2822362 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04f67d2af5dcf43b040dba313ee19eab8ac3fb660a57d74e6a50c72efc1580e2`  
		Last Modified: Mon, 08 Jul 2024 19:10:26 GMT  
		Size: 15.4 KB (15407 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.1.6`

```console
$ docker pull emqx@sha256:565682578cd04ae459ed9e1388feff2fe6903ce0bf35bf70425164f90601f71d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	unknown; unknown

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
$ docker pull emqx@sha256:cada4e0bebc80733ea8b2deaaa4c17b8b89b7ecae41eb72037d86975677b7b93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.7 MB (92698712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb76131bb270212955ab13689d623955acc25a8bad1f4b6ff667d46ee4c122c2`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 05 Sep 2023 13:05:03 GMT
ADD file:17d80cdc7d7b37786a32ac4e261c7d17cd4d80248ae39f9574ab5a6bf6a2707c in / 
# Tue, 05 Sep 2023 13:05:03 GMT
CMD ["bash"]
# Tue, 05 Sep 2023 13:05:03 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Sep 2023 13:05:03 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx; # buildkit
# Tue, 05 Sep 2023 13:05:03 GMT
ENV EMQX_VERSION=5.1.6
# Tue, 05 Sep 2023 13:05:03 GMT
ENV AMD64_SHA256=5c65f7538141e93d71d1dd7d088589339ef6a091b90f901604a2e0e004f5f4aa
# Tue, 05 Sep 2023 13:05:03 GMT
ENV ARM64_SHA256=ae832d29d6b4e7fa43f3bf04c8c9fad4c9047f079d1587d3ed2a3564d5ea8147
# Tue, 05 Sep 2023 13:05:03 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 05 Sep 2023 13:05:03 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg # buildkit
# Tue, 05 Sep 2023 13:05:03 GMT
WORKDIR /opt/emqx
# Tue, 05 Sep 2023 13:05:03 GMT
USER emqx
# Tue, 05 Sep 2023 13:05:03 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 05 Sep 2023 13:05:03 GMT
EXPOSE map[11883/tcp:{} 18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Tue, 05 Sep 2023 13:05:03 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Tue, 05 Sep 2023 13:05:03 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 05 Sep 2023 13:05:03 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:d13ad33c16eef01d20d5563bfb2ec4f25c0d12699b40cdab418e47b88d2f02e2`  
		Last Modified: Tue, 02 Jul 2024 00:43:04 GMT  
		Size: 30.1 MB (30069615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a47fc32e1771420c513826f66af1965425d7fde637f9df85e79c88abcf9df8f4`  
		Last Modified: Mon, 08 Jul 2024 19:10:27 GMT  
		Size: 3.0 MB (3003825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30abb6da25a89b034369ea57a7b6f06a4b59035a842b59538e0b0c9b70412159`  
		Last Modified: Mon, 08 Jul 2024 19:10:27 GMT  
		Size: 4.0 KB (3998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bcbc9c4ef2388a1d129a01b42394a636072b082259312c8de48ca08ec4341e4`  
		Last Modified: Mon, 08 Jul 2024 19:10:28 GMT  
		Size: 59.6 MB (59620341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:442fe0e0448c7bbd97e338110a8b195ab0aa51764677f1519f6e668b821d7d97`  
		Last Modified: Mon, 08 Jul 2024 19:10:27 GMT  
		Size: 901.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.1.6` - unknown; unknown

```console
$ docker pull emqx@sha256:a7758fa95ff78651af4b5807080d88ecb614e10124348dc840d3627821a3ab03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2837769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8eb74e25ec6582b18ce5c04a69587822c751bd640c95ac9ff32b440b4b16d3c3`

```dockerfile
```

-	Layers:
	-	`sha256:39de6641d6a29c6221c008ff83be6625a111c57ee1f3a985bf449f2ad286e61c`  
		Last Modified: Mon, 08 Jul 2024 19:10:27 GMT  
		Size: 2.8 MB (2822362 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04f67d2af5dcf43b040dba313ee19eab8ac3fb660a57d74e6a50c72efc1580e2`  
		Last Modified: Mon, 08 Jul 2024 19:10:26 GMT  
		Size: 15.4 KB (15407 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.2`

```console
$ docker pull emqx@sha256:ecc8a441c720a011f6dd6c14905d142d321d3f83a092c24f14202b6545d0f173
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	unknown; unknown

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
$ docker pull emqx@sha256:2262eef51d4a9f61be2b7407b21706a2465c050cc30110b0d9e7d6dc7cb380f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.3 MB (91255514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5d4f0cc3734ca61ac76aa974e1346421d7668cdf39ee0b57c0f37f847f96d93`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 25 Sep 2023 09:53:58 GMT
ADD file:17d80cdc7d7b37786a32ac4e261c7d17cd4d80248ae39f9574ab5a6bf6a2707c in / 
# Mon, 25 Sep 2023 09:53:58 GMT
CMD ["bash"]
# Mon, 25 Sep 2023 09:53:58 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 25 Sep 2023 09:53:58 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx; # buildkit
# Mon, 25 Sep 2023 09:53:58 GMT
ENV EMQX_VERSION=5.2.1
# Mon, 25 Sep 2023 09:53:58 GMT
ENV AMD64_SHA256=359a12811e5e6725e4269d9484abd348effdde35c0f2af1f5b63cae790c73020
# Mon, 25 Sep 2023 09:53:58 GMT
ENV ARM64_SHA256=2e0a3e0b33669c9b6da488970a2f92d08d7bd0824295822b205b83461ba4728d
# Mon, 25 Sep 2023 09:53:58 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Mon, 25 Sep 2023 09:53:58 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl;     rm -rf /var/lib/apt/lists/*;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl # buildkit
# Mon, 25 Sep 2023 09:53:58 GMT
WORKDIR /opt/emqx
# Mon, 25 Sep 2023 09:53:58 GMT
USER emqx
# Mon, 25 Sep 2023 09:53:58 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Mon, 25 Sep 2023 09:53:58 GMT
EXPOSE map[11883/tcp:{} 18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Mon, 25 Sep 2023 09:53:58 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Mon, 25 Sep 2023 09:53:58 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Mon, 25 Sep 2023 09:53:58 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:d13ad33c16eef01d20d5563bfb2ec4f25c0d12699b40cdab418e47b88d2f02e2`  
		Last Modified: Tue, 02 Jul 2024 00:43:04 GMT  
		Size: 30.1 MB (30069615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d47f685676a84b42ad28e83cc2288b58817812479b9f78a84df26fc6d2ba6d58`  
		Last Modified: Mon, 08 Jul 2024 19:11:05 GMT  
		Size: 1.6 MB (1643742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9667ea51efb76fc783c11b275ac32c60c19eba9d80c6d79a52c63654793225e6`  
		Last Modified: Mon, 08 Jul 2024 19:11:04 GMT  
		Size: 4.0 KB (3998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e1143fda4d658df0d453ccde0405de6a0cec03673cc964e9ce07dd4fe12b187`  
		Last Modified: Mon, 08 Jul 2024 19:11:07 GMT  
		Size: 59.5 MB (59537226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:797b4d2cd4c0f7c62b169286fa88cdc4b702f8cf2dae5e2c08a8d2d8e06563a2`  
		Last Modified: Mon, 08 Jul 2024 19:11:05 GMT  
		Size: 901.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.2` - unknown; unknown

```console
$ docker pull emqx@sha256:0bca6dd2d4e8601122ae7e30393d3ec62b9d1911176784ec1e078b2bab02ac10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2784870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ad7b4e33e396474881ae0eade18c058b76ad76d2a125d8d95f9f7d4871297ee`

```dockerfile
```

-	Layers:
	-	`sha256:778f56810c422ec9c701dfede4ad8c5fc809fcf52caf1b3bd455a5e87526f293`  
		Last Modified: Mon, 08 Jul 2024 19:11:05 GMT  
		Size: 2.8 MB (2768961 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:030b4d71e411dc20c6c2a709f33103035822397592f6a8cc4bdb3444ea9e5e46`  
		Last Modified: Mon, 08 Jul 2024 19:11:06 GMT  
		Size: 15.9 KB (15909 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.2.1`

```console
$ docker pull emqx@sha256:ecc8a441c720a011f6dd6c14905d142d321d3f83a092c24f14202b6545d0f173
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	unknown; unknown

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
$ docker pull emqx@sha256:2262eef51d4a9f61be2b7407b21706a2465c050cc30110b0d9e7d6dc7cb380f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.3 MB (91255514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5d4f0cc3734ca61ac76aa974e1346421d7668cdf39ee0b57c0f37f847f96d93`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 25 Sep 2023 09:53:58 GMT
ADD file:17d80cdc7d7b37786a32ac4e261c7d17cd4d80248ae39f9574ab5a6bf6a2707c in / 
# Mon, 25 Sep 2023 09:53:58 GMT
CMD ["bash"]
# Mon, 25 Sep 2023 09:53:58 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 25 Sep 2023 09:53:58 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx; # buildkit
# Mon, 25 Sep 2023 09:53:58 GMT
ENV EMQX_VERSION=5.2.1
# Mon, 25 Sep 2023 09:53:58 GMT
ENV AMD64_SHA256=359a12811e5e6725e4269d9484abd348effdde35c0f2af1f5b63cae790c73020
# Mon, 25 Sep 2023 09:53:58 GMT
ENV ARM64_SHA256=2e0a3e0b33669c9b6da488970a2f92d08d7bd0824295822b205b83461ba4728d
# Mon, 25 Sep 2023 09:53:58 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Mon, 25 Sep 2023 09:53:58 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl;     rm -rf /var/lib/apt/lists/*;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl # buildkit
# Mon, 25 Sep 2023 09:53:58 GMT
WORKDIR /opt/emqx
# Mon, 25 Sep 2023 09:53:58 GMT
USER emqx
# Mon, 25 Sep 2023 09:53:58 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Mon, 25 Sep 2023 09:53:58 GMT
EXPOSE map[11883/tcp:{} 18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Mon, 25 Sep 2023 09:53:58 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Mon, 25 Sep 2023 09:53:58 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Mon, 25 Sep 2023 09:53:58 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:d13ad33c16eef01d20d5563bfb2ec4f25c0d12699b40cdab418e47b88d2f02e2`  
		Last Modified: Tue, 02 Jul 2024 00:43:04 GMT  
		Size: 30.1 MB (30069615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d47f685676a84b42ad28e83cc2288b58817812479b9f78a84df26fc6d2ba6d58`  
		Last Modified: Mon, 08 Jul 2024 19:11:05 GMT  
		Size: 1.6 MB (1643742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9667ea51efb76fc783c11b275ac32c60c19eba9d80c6d79a52c63654793225e6`  
		Last Modified: Mon, 08 Jul 2024 19:11:04 GMT  
		Size: 4.0 KB (3998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e1143fda4d658df0d453ccde0405de6a0cec03673cc964e9ce07dd4fe12b187`  
		Last Modified: Mon, 08 Jul 2024 19:11:07 GMT  
		Size: 59.5 MB (59537226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:797b4d2cd4c0f7c62b169286fa88cdc4b702f8cf2dae5e2c08a8d2d8e06563a2`  
		Last Modified: Mon, 08 Jul 2024 19:11:05 GMT  
		Size: 901.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.2.1` - unknown; unknown

```console
$ docker pull emqx@sha256:0bca6dd2d4e8601122ae7e30393d3ec62b9d1911176784ec1e078b2bab02ac10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2784870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ad7b4e33e396474881ae0eade18c058b76ad76d2a125d8d95f9f7d4871297ee`

```dockerfile
```

-	Layers:
	-	`sha256:778f56810c422ec9c701dfede4ad8c5fc809fcf52caf1b3bd455a5e87526f293`  
		Last Modified: Mon, 08 Jul 2024 19:11:05 GMT  
		Size: 2.8 MB (2768961 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:030b4d71e411dc20c6c2a709f33103035822397592f6a8cc4bdb3444ea9e5e46`  
		Last Modified: Mon, 08 Jul 2024 19:11:06 GMT  
		Size: 15.9 KB (15909 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.3`

```console
$ docker pull emqx@sha256:3fb689254835da4250600c8555d010e7b6a26248cbc3444916f648072c1ef4b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	unknown; unknown

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
$ docker pull emqx@sha256:988f5d343469d557bdea7c43791cbe2d3c80a4c5d338c2e978da1020e9429592
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.1 MB (92081158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56b75fe113027384d5d77071c49148c048ce843069161fcf8e37bb77e3b2e683`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Fri, 01 Dec 2023 10:27:11 GMT
ADD file:17d80cdc7d7b37786a32ac4e261c7d17cd4d80248ae39f9574ab5a6bf6a2707c in / 
# Fri, 01 Dec 2023 10:27:11 GMT
CMD ["bash"]
# Fri, 01 Dec 2023 10:27:11 GMT
ENV EMQX_VERSION=5.3.2
# Fri, 01 Dec 2023 10:27:11 GMT
ENV AMD64_SHA256=d5948d4171f57e77756dd6c9eeb745c39e391e75aad3798fce445f44f5690be0
# Fri, 01 Dec 2023 10:27:11 GMT
ENV ARM64_SHA256=82b056bb1c1cd1f16e9d0719150fa8ac19c499d29563738bcd6984b3c395c6ac
# Fri, 01 Dec 2023 10:27:11 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Fri, 01 Dec 2023 10:27:11 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Dec 2023 10:27:11 GMT
WORKDIR /opt/emqx
# Fri, 01 Dec 2023 10:27:11 GMT
USER emqx
# Fri, 01 Dec 2023 10:27:11 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Fri, 01 Dec 2023 10:27:11 GMT
EXPOSE map[11883/tcp:{} 18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Fri, 01 Dec 2023 10:27:11 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Fri, 01 Dec 2023 10:27:11 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Fri, 01 Dec 2023 10:27:11 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:d13ad33c16eef01d20d5563bfb2ec4f25c0d12699b40cdab418e47b88d2f02e2`  
		Last Modified: Tue, 02 Jul 2024 00:43:04 GMT  
		Size: 30.1 MB (30069615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52cab82329c1e3ef265821322daff0415d83d5f27f461c80fdad1e800cf38ba3`  
		Last Modified: Mon, 08 Jul 2024 19:11:42 GMT  
		Size: 62.0 MB (62010610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0566a31872da74abd788a5bc34c298683d3f97d9d6037f09f5640668abb81838`  
		Last Modified: Mon, 08 Jul 2024 19:11:38 GMT  
		Size: 901.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.3` - unknown; unknown

```console
$ docker pull emqx@sha256:810b9f82ca5926ef2b4127348ca0085a3fe6ceab1ba7122e29d28d622e2e885f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2791712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2411b2201c7bff828cf1ebcf64108f9c56db164e3448bc2f321e5aaec038fcdc`

```dockerfile
```

-	Layers:
	-	`sha256:0f99375ac7482efa306d1d270621d0c5ae5038208124da1d66f0a0b7830dcbb3`  
		Last Modified: Mon, 08 Jul 2024 19:11:38 GMT  
		Size: 2.8 MB (2778874 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63a3a98bbe060291962b24b8d2ee9eee82015834014427d2ec016a04a023e566`  
		Last Modified: Mon, 08 Jul 2024 19:11:38 GMT  
		Size: 12.8 KB (12838 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.3.2`

```console
$ docker pull emqx@sha256:3fb689254835da4250600c8555d010e7b6a26248cbc3444916f648072c1ef4b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	unknown; unknown

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
$ docker pull emqx@sha256:988f5d343469d557bdea7c43791cbe2d3c80a4c5d338c2e978da1020e9429592
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.1 MB (92081158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56b75fe113027384d5d77071c49148c048ce843069161fcf8e37bb77e3b2e683`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Fri, 01 Dec 2023 10:27:11 GMT
ADD file:17d80cdc7d7b37786a32ac4e261c7d17cd4d80248ae39f9574ab5a6bf6a2707c in / 
# Fri, 01 Dec 2023 10:27:11 GMT
CMD ["bash"]
# Fri, 01 Dec 2023 10:27:11 GMT
ENV EMQX_VERSION=5.3.2
# Fri, 01 Dec 2023 10:27:11 GMT
ENV AMD64_SHA256=d5948d4171f57e77756dd6c9eeb745c39e391e75aad3798fce445f44f5690be0
# Fri, 01 Dec 2023 10:27:11 GMT
ENV ARM64_SHA256=82b056bb1c1cd1f16e9d0719150fa8ac19c499d29563738bcd6984b3c395c6ac
# Fri, 01 Dec 2023 10:27:11 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Fri, 01 Dec 2023 10:27:11 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Dec 2023 10:27:11 GMT
WORKDIR /opt/emqx
# Fri, 01 Dec 2023 10:27:11 GMT
USER emqx
# Fri, 01 Dec 2023 10:27:11 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Fri, 01 Dec 2023 10:27:11 GMT
EXPOSE map[11883/tcp:{} 18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Fri, 01 Dec 2023 10:27:11 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Fri, 01 Dec 2023 10:27:11 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Fri, 01 Dec 2023 10:27:11 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:d13ad33c16eef01d20d5563bfb2ec4f25c0d12699b40cdab418e47b88d2f02e2`  
		Last Modified: Tue, 02 Jul 2024 00:43:04 GMT  
		Size: 30.1 MB (30069615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52cab82329c1e3ef265821322daff0415d83d5f27f461c80fdad1e800cf38ba3`  
		Last Modified: Mon, 08 Jul 2024 19:11:42 GMT  
		Size: 62.0 MB (62010610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0566a31872da74abd788a5bc34c298683d3f97d9d6037f09f5640668abb81838`  
		Last Modified: Mon, 08 Jul 2024 19:11:38 GMT  
		Size: 901.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.3.2` - unknown; unknown

```console
$ docker pull emqx@sha256:810b9f82ca5926ef2b4127348ca0085a3fe6ceab1ba7122e29d28d622e2e885f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2791712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2411b2201c7bff828cf1ebcf64108f9c56db164e3448bc2f321e5aaec038fcdc`

```dockerfile
```

-	Layers:
	-	`sha256:0f99375ac7482efa306d1d270621d0c5ae5038208124da1d66f0a0b7830dcbb3`  
		Last Modified: Mon, 08 Jul 2024 19:11:38 GMT  
		Size: 2.8 MB (2778874 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63a3a98bbe060291962b24b8d2ee9eee82015834014427d2ec016a04a023e566`  
		Last Modified: Mon, 08 Jul 2024 19:11:38 GMT  
		Size: 12.8 KB (12838 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.4`

```console
$ docker pull emqx@sha256:e4c69878c0946661e209419c4d7a14bed2230ad461e27da7f2f64e47b74d0d88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	unknown; unknown

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
$ docker pull emqx@sha256:372129587039fb4d05a7b1f092a5cb01fd403a02ad00156e3ebd04f577dea18b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.5 MB (108479553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c629d363e9597a0fc94034631d9cc2831df884201a6bcf81644116287ea32a5`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Fri, 12 Jan 2024 14:13:45 GMT
ADD file:17d80cdc7d7b37786a32ac4e261c7d17cd4d80248ae39f9574ab5a6bf6a2707c in / 
# Fri, 12 Jan 2024 14:13:45 GMT
CMD ["bash"]
# Fri, 12 Jan 2024 14:13:45 GMT
ENV EMQX_VERSION=5.4.1
# Fri, 12 Jan 2024 14:13:45 GMT
ENV AMD64_SHA256=c2087651d72f17999f52d73ff22cd8f23dc5fa5db8b5a90a8bc4a1410b03affb
# Fri, 12 Jan 2024 14:13:45 GMT
ENV ARM64_SHA256=6c53a68ae907f7b4a3cdcd4dbee4f839b07853695ac1c039b51fd97d993073bc
# Fri, 12 Jan 2024 14:13:45 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Fri, 12 Jan 2024 14:13:45 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 12 Jan 2024 14:13:45 GMT
WORKDIR /opt/emqx
# Fri, 12 Jan 2024 14:13:45 GMT
USER emqx
# Fri, 12 Jan 2024 14:13:45 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Fri, 12 Jan 2024 14:13:45 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Fri, 12 Jan 2024 14:13:45 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Fri, 12 Jan 2024 14:13:45 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Fri, 12 Jan 2024 14:13:45 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:d13ad33c16eef01d20d5563bfb2ec4f25c0d12699b40cdab418e47b88d2f02e2`  
		Last Modified: Tue, 02 Jul 2024 00:43:04 GMT  
		Size: 30.1 MB (30069615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3602325be2f03896f21a1b18ec916d00c20d1d0d4ff357ea418b351ddfc993b7`  
		Last Modified: Mon, 08 Jul 2024 19:12:18 GMT  
		Size: 78.4 MB (78409005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a443efe216cff55e388643f0246e1746bde91e197528a31e4a5f5109c29ff585`  
		Last Modified: Mon, 08 Jul 2024 19:12:15 GMT  
		Size: 901.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.4` - unknown; unknown

```console
$ docker pull emqx@sha256:a23fd6dc2af4f850b35bdd7e407b53bf1c0a51186b5b1664d910a5ec74580def
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2785839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c88ab692e308275b2fdcef7f96f5e805f0af93a0b98992f7a6d0c05ea084ae6a`

```dockerfile
```

-	Layers:
	-	`sha256:7ebad33375cb3eb1724f405536bce35e2b65b667071a82abcb0ddb31ac31b7cd`  
		Last Modified: Mon, 08 Jul 2024 19:12:16 GMT  
		Size: 2.8 MB (2773057 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c54a86be65a75bb9a55e0e2ecedb678e8fa8801603ed8ee8e5b262bcc3d6617`  
		Last Modified: Mon, 08 Jul 2024 19:12:15 GMT  
		Size: 12.8 KB (12782 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.4.1`

```console
$ docker pull emqx@sha256:e4c69878c0946661e209419c4d7a14bed2230ad461e27da7f2f64e47b74d0d88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	unknown; unknown

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
$ docker pull emqx@sha256:372129587039fb4d05a7b1f092a5cb01fd403a02ad00156e3ebd04f577dea18b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.5 MB (108479553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c629d363e9597a0fc94034631d9cc2831df884201a6bcf81644116287ea32a5`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Fri, 12 Jan 2024 14:13:45 GMT
ADD file:17d80cdc7d7b37786a32ac4e261c7d17cd4d80248ae39f9574ab5a6bf6a2707c in / 
# Fri, 12 Jan 2024 14:13:45 GMT
CMD ["bash"]
# Fri, 12 Jan 2024 14:13:45 GMT
ENV EMQX_VERSION=5.4.1
# Fri, 12 Jan 2024 14:13:45 GMT
ENV AMD64_SHA256=c2087651d72f17999f52d73ff22cd8f23dc5fa5db8b5a90a8bc4a1410b03affb
# Fri, 12 Jan 2024 14:13:45 GMT
ENV ARM64_SHA256=6c53a68ae907f7b4a3cdcd4dbee4f839b07853695ac1c039b51fd97d993073bc
# Fri, 12 Jan 2024 14:13:45 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Fri, 12 Jan 2024 14:13:45 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 12 Jan 2024 14:13:45 GMT
WORKDIR /opt/emqx
# Fri, 12 Jan 2024 14:13:45 GMT
USER emqx
# Fri, 12 Jan 2024 14:13:45 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Fri, 12 Jan 2024 14:13:45 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Fri, 12 Jan 2024 14:13:45 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Fri, 12 Jan 2024 14:13:45 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Fri, 12 Jan 2024 14:13:45 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:d13ad33c16eef01d20d5563bfb2ec4f25c0d12699b40cdab418e47b88d2f02e2`  
		Last Modified: Tue, 02 Jul 2024 00:43:04 GMT  
		Size: 30.1 MB (30069615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3602325be2f03896f21a1b18ec916d00c20d1d0d4ff357ea418b351ddfc993b7`  
		Last Modified: Mon, 08 Jul 2024 19:12:18 GMT  
		Size: 78.4 MB (78409005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a443efe216cff55e388643f0246e1746bde91e197528a31e4a5f5109c29ff585`  
		Last Modified: Mon, 08 Jul 2024 19:12:15 GMT  
		Size: 901.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.4.1` - unknown; unknown

```console
$ docker pull emqx@sha256:a23fd6dc2af4f850b35bdd7e407b53bf1c0a51186b5b1664d910a5ec74580def
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2785839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c88ab692e308275b2fdcef7f96f5e805f0af93a0b98992f7a6d0c05ea084ae6a`

```dockerfile
```

-	Layers:
	-	`sha256:7ebad33375cb3eb1724f405536bce35e2b65b667071a82abcb0ddb31ac31b7cd`  
		Last Modified: Mon, 08 Jul 2024 19:12:16 GMT  
		Size: 2.8 MB (2773057 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c54a86be65a75bb9a55e0e2ecedb678e8fa8801603ed8ee8e5b262bcc3d6617`  
		Last Modified: Mon, 08 Jul 2024 19:12:15 GMT  
		Size: 12.8 KB (12782 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.5`

```console
$ docker pull emqx@sha256:34ee54823eebcb603e818fbf6e686027dbb24d059ac843d69145d9c844697852
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	unknown; unknown

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
$ docker pull emqx@sha256:ac7bf171d1a3642d64769d50db4aaa1da31af3078465c6336c600485d37daf23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.8 MB (116777814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5258c409483366dae6b03bb495f5ca837095616adc4eb76abc9648884ddb83e`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 03 Apr 2024 12:49:39 GMT
ADD file:17d80cdc7d7b37786a32ac4e261c7d17cd4d80248ae39f9574ab5a6bf6a2707c in / 
# Wed, 03 Apr 2024 12:49:39 GMT
CMD ["bash"]
# Wed, 03 Apr 2024 12:49:39 GMT
ENV EMQX_VERSION=5.5.1
# Wed, 03 Apr 2024 12:49:39 GMT
ENV AMD64_SHA256=8bac2886987a632aab1c738aa3de28684b415d3b1e1f9489b458c819254673a6
# Wed, 03 Apr 2024 12:49:39 GMT
ENV ARM64_SHA256=8b962ad8beea50fb92dc0b93d2ab8a5064752147b70bbf46fd221bc4cc29c32d
# Wed, 03 Apr 2024 12:49:39 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 03 Apr 2024 12:49:39 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     mkdir -p /opt/emqx/log /opt/emqx/data /opt/emqx/plugins;     chown -R emqx:emqx /opt/emqx/log /opt/emqx/data /opt/emqx/plugins;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Wed, 03 Apr 2024 12:49:39 GMT
WORKDIR /opt/emqx
# Wed, 03 Apr 2024 12:49:39 GMT
USER emqx
# Wed, 03 Apr 2024 12:49:39 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 03 Apr 2024 12:49:39 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Wed, 03 Apr 2024 12:49:39 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Wed, 03 Apr 2024 12:49:39 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 03 Apr 2024 12:49:39 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:d13ad33c16eef01d20d5563bfb2ec4f25c0d12699b40cdab418e47b88d2f02e2`  
		Last Modified: Tue, 02 Jul 2024 00:43:04 GMT  
		Size: 30.1 MB (30069615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:683d31784681b627bf9d7a783bdd8234bd2e23eb72007310cfbd93ccb01ca839`  
		Last Modified: Mon, 08 Jul 2024 19:12:54 GMT  
		Size: 86.7 MB (86707135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d443b25a39e53134295d1fbc3ffaecb74826d01b2d2bbc0e630c27ade7c64057`  
		Last Modified: Mon, 08 Jul 2024 19:12:52 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.5` - unknown; unknown

```console
$ docker pull emqx@sha256:46e79cb810438a94f5c4465c05e12ecf07d3b5f87d0cc037d53ff4980d54e0e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2785901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b9787d744429f183b66f26754b4a33a6169c2b5ed796bea91655b2e86e78648`

```dockerfile
```

-	Layers:
	-	`sha256:aef6b69a7208c02e2b911d26c930fd16fc7074b491330289101ec477407b3a19`  
		Last Modified: Mon, 08 Jul 2024 19:12:52 GMT  
		Size: 2.8 MB (2773018 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e816758d0759f99074fb60904d9e203c2b52b50cea7267960c27cde890b1fe7`  
		Last Modified: Mon, 08 Jul 2024 19:12:51 GMT  
		Size: 12.9 KB (12883 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.5.1`

```console
$ docker pull emqx@sha256:34ee54823eebcb603e818fbf6e686027dbb24d059ac843d69145d9c844697852
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	unknown; unknown

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
$ docker pull emqx@sha256:ac7bf171d1a3642d64769d50db4aaa1da31af3078465c6336c600485d37daf23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.8 MB (116777814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5258c409483366dae6b03bb495f5ca837095616adc4eb76abc9648884ddb83e`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 03 Apr 2024 12:49:39 GMT
ADD file:17d80cdc7d7b37786a32ac4e261c7d17cd4d80248ae39f9574ab5a6bf6a2707c in / 
# Wed, 03 Apr 2024 12:49:39 GMT
CMD ["bash"]
# Wed, 03 Apr 2024 12:49:39 GMT
ENV EMQX_VERSION=5.5.1
# Wed, 03 Apr 2024 12:49:39 GMT
ENV AMD64_SHA256=8bac2886987a632aab1c738aa3de28684b415d3b1e1f9489b458c819254673a6
# Wed, 03 Apr 2024 12:49:39 GMT
ENV ARM64_SHA256=8b962ad8beea50fb92dc0b93d2ab8a5064752147b70bbf46fd221bc4cc29c32d
# Wed, 03 Apr 2024 12:49:39 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 03 Apr 2024 12:49:39 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     mkdir -p /opt/emqx/log /opt/emqx/data /opt/emqx/plugins;     chown -R emqx:emqx /opt/emqx/log /opt/emqx/data /opt/emqx/plugins;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Wed, 03 Apr 2024 12:49:39 GMT
WORKDIR /opt/emqx
# Wed, 03 Apr 2024 12:49:39 GMT
USER emqx
# Wed, 03 Apr 2024 12:49:39 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 03 Apr 2024 12:49:39 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Wed, 03 Apr 2024 12:49:39 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Wed, 03 Apr 2024 12:49:39 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 03 Apr 2024 12:49:39 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:d13ad33c16eef01d20d5563bfb2ec4f25c0d12699b40cdab418e47b88d2f02e2`  
		Last Modified: Tue, 02 Jul 2024 00:43:04 GMT  
		Size: 30.1 MB (30069615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:683d31784681b627bf9d7a783bdd8234bd2e23eb72007310cfbd93ccb01ca839`  
		Last Modified: Mon, 08 Jul 2024 19:12:54 GMT  
		Size: 86.7 MB (86707135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d443b25a39e53134295d1fbc3ffaecb74826d01b2d2bbc0e630c27ade7c64057`  
		Last Modified: Mon, 08 Jul 2024 19:12:52 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.5.1` - unknown; unknown

```console
$ docker pull emqx@sha256:46e79cb810438a94f5c4465c05e12ecf07d3b5f87d0cc037d53ff4980d54e0e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2785901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b9787d744429f183b66f26754b4a33a6169c2b5ed796bea91655b2e86e78648`

```dockerfile
```

-	Layers:
	-	`sha256:aef6b69a7208c02e2b911d26c930fd16fc7074b491330289101ec477407b3a19`  
		Last Modified: Mon, 08 Jul 2024 19:12:52 GMT  
		Size: 2.8 MB (2773018 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e816758d0759f99074fb60904d9e203c2b52b50cea7267960c27cde890b1fe7`  
		Last Modified: Mon, 08 Jul 2024 19:12:51 GMT  
		Size: 12.9 KB (12883 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.6`

```console
$ docker pull emqx@sha256:cf2378830a18e963d303051dfd69895f182f3facb7d71beb8f0de7af5d872cb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	unknown; unknown

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
$ docker pull emqx@sha256:3672b7c05cce1e4925fd46a8bda3a5c1584f222d42e408a35048264d743d71f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.8 MB (120775029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86e6d072aa51b5aaf239a941c72b3ec197802b764183f48127a6321c99fdc7dd`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 22 Apr 2024 06:31:42 GMT
ADD file:cbda549b25cd4337cd3ce345e3b66c0d3b43c247d7315906a028f98a56c41f1d in / 
# Mon, 22 Apr 2024 06:31:42 GMT
CMD ["bash"]
# Mon, 22 Apr 2024 06:31:42 GMT
ENV EMQX_VERSION=5.6.1
# Mon, 22 Apr 2024 06:31:42 GMT
ENV AMD64_SHA256=a5be37660bfe6130bc159b934ed98ffcb9bef5519765491b4ed38d08ba304538
# Mon, 22 Apr 2024 06:31:42 GMT
ENV ARM64_SHA256=3f7f9b10d313f760af43e0a54cba2af4eb23ad3864b439196cb8b2903baf5651
# Mon, 22 Apr 2024 06:31:42 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Mon, 22 Apr 2024 06:31:42 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Mon, 22 Apr 2024 06:31:42 GMT
WORKDIR /opt/emqx
# Mon, 22 Apr 2024 06:31:42 GMT
USER emqx
# Mon, 22 Apr 2024 06:31:42 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Mon, 22 Apr 2024 06:31:42 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Mon, 22 Apr 2024 06:31:42 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Mon, 22 Apr 2024 06:31:42 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Mon, 22 Apr 2024 06:31:42 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:ea235d1ccf77ca07a545b448996766dc3eca4b971b04ba39d50af69660b25751`  
		Last Modified: Tue, 02 Jul 2024 00:42:25 GMT  
		Size: 29.2 MB (29156563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43835f8cf5b229f55d9c7b439ff9d127fe655be4b2bd9e4d9e5ed35271314631`  
		Last Modified: Mon, 08 Jul 2024 19:13:41 GMT  
		Size: 91.6 MB (91617405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5679dd221f9633c40dc1c6987afed73d67588bd6649bee99983230043238e7e0`  
		Last Modified: Mon, 08 Jul 2024 19:13:39 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.6` - unknown; unknown

```console
$ docker pull emqx@sha256:9345065322dae3f338d4ac8a509937978b4580c83359bbd369328036e524684a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2564419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71c2ade3b0c32f55629eca99573bc25cc300b71421082cd5f9184fc49148d718`

```dockerfile
```

-	Layers:
	-	`sha256:e3cb7cb3dcf0adccbe9d4689b327b5b1e893d797d115eeacfa3cbf85c54f944c`  
		Last Modified: Mon, 08 Jul 2024 19:13:39 GMT  
		Size: 2.6 MB (2552413 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eb734b3bd3151a422e104ddf51890260a2f9be4dcbede4614c180993038d1d40`  
		Last Modified: Mon, 08 Jul 2024 19:13:38 GMT  
		Size: 12.0 KB (12006 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.6.1`

```console
$ docker pull emqx@sha256:cf2378830a18e963d303051dfd69895f182f3facb7d71beb8f0de7af5d872cb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	unknown; unknown

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
$ docker pull emqx@sha256:3672b7c05cce1e4925fd46a8bda3a5c1584f222d42e408a35048264d743d71f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.8 MB (120775029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86e6d072aa51b5aaf239a941c72b3ec197802b764183f48127a6321c99fdc7dd`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 22 Apr 2024 06:31:42 GMT
ADD file:cbda549b25cd4337cd3ce345e3b66c0d3b43c247d7315906a028f98a56c41f1d in / 
# Mon, 22 Apr 2024 06:31:42 GMT
CMD ["bash"]
# Mon, 22 Apr 2024 06:31:42 GMT
ENV EMQX_VERSION=5.6.1
# Mon, 22 Apr 2024 06:31:42 GMT
ENV AMD64_SHA256=a5be37660bfe6130bc159b934ed98ffcb9bef5519765491b4ed38d08ba304538
# Mon, 22 Apr 2024 06:31:42 GMT
ENV ARM64_SHA256=3f7f9b10d313f760af43e0a54cba2af4eb23ad3864b439196cb8b2903baf5651
# Mon, 22 Apr 2024 06:31:42 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Mon, 22 Apr 2024 06:31:42 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Mon, 22 Apr 2024 06:31:42 GMT
WORKDIR /opt/emqx
# Mon, 22 Apr 2024 06:31:42 GMT
USER emqx
# Mon, 22 Apr 2024 06:31:42 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Mon, 22 Apr 2024 06:31:42 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Mon, 22 Apr 2024 06:31:42 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Mon, 22 Apr 2024 06:31:42 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Mon, 22 Apr 2024 06:31:42 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:ea235d1ccf77ca07a545b448996766dc3eca4b971b04ba39d50af69660b25751`  
		Last Modified: Tue, 02 Jul 2024 00:42:25 GMT  
		Size: 29.2 MB (29156563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43835f8cf5b229f55d9c7b439ff9d127fe655be4b2bd9e4d9e5ed35271314631`  
		Last Modified: Mon, 08 Jul 2024 19:13:41 GMT  
		Size: 91.6 MB (91617405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5679dd221f9633c40dc1c6987afed73d67588bd6649bee99983230043238e7e0`  
		Last Modified: Mon, 08 Jul 2024 19:13:39 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.6.1` - unknown; unknown

```console
$ docker pull emqx@sha256:9345065322dae3f338d4ac8a509937978b4580c83359bbd369328036e524684a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2564419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71c2ade3b0c32f55629eca99573bc25cc300b71421082cd5f9184fc49148d718`

```dockerfile
```

-	Layers:
	-	`sha256:e3cb7cb3dcf0adccbe9d4689b327b5b1e893d797d115eeacfa3cbf85c54f944c`  
		Last Modified: Mon, 08 Jul 2024 19:13:39 GMT  
		Size: 2.6 MB (2552413 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eb734b3bd3151a422e104ddf51890260a2f9be4dcbede4614c180993038d1d40`  
		Last Modified: Mon, 08 Jul 2024 19:13:38 GMT  
		Size: 12.0 KB (12006 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.7`

```console
$ docker pull emqx@sha256:34d1e4eb60a8388c0e81cb51437f49cfdc82173bfa19bb6657bb3b71278f1a29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	unknown; unknown

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
$ docker pull emqx@sha256:074ff8d864916263abc6e8c42120a7efa67fea641cb6a3a070a3614a2c5b66d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.8 MB (122815523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:573da311dffd01ef129754dc5a68bc6494d88d070bb031800b6881927091e973`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Thu, 27 Jun 2024 06:50:32 GMT
ADD file:cbda549b25cd4337cd3ce345e3b66c0d3b43c247d7315906a028f98a56c41f1d in / 
# Thu, 27 Jun 2024 06:50:32 GMT
CMD ["bash"]
# Thu, 27 Jun 2024 06:50:32 GMT
ENV EMQX_VERSION=5.7.1
# Thu, 27 Jun 2024 06:50:32 GMT
ENV AMD64_SHA256=6896263e24c1211fea0e15464afb39931e9b4c7139804e0a6fb5f143826efaf8
# Thu, 27 Jun 2024 06:50:32 GMT
ENV ARM64_SHA256=c321477bab28e381a472761c2d62f9e5acf6290f298f5aaf9404ab70feb6d587
# Thu, 27 Jun 2024 06:50:32 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Thu, 27 Jun 2024 06:50:32 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Thu, 27 Jun 2024 06:50:32 GMT
WORKDIR /opt/emqx
# Thu, 27 Jun 2024 06:50:32 GMT
USER emqx
# Thu, 27 Jun 2024 06:50:32 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Thu, 27 Jun 2024 06:50:32 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Thu, 27 Jun 2024 06:50:32 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Thu, 27 Jun 2024 06:50:32 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Thu, 27 Jun 2024 06:50:32 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:ea235d1ccf77ca07a545b448996766dc3eca4b971b04ba39d50af69660b25751`  
		Last Modified: Tue, 02 Jul 2024 00:42:25 GMT  
		Size: 29.2 MB (29156563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b31646db1381832e88900fde1500ba647e8458191411a4d10dcc4c8becfe406`  
		Last Modified: Mon, 08 Jul 2024 19:14:23 GMT  
		Size: 93.7 MB (93657896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:762d975f3920ce02bd4da5ca7a8fdc83b4f8f921649f9451c80a10c3edccf678`  
		Last Modified: Mon, 08 Jul 2024 19:14:20 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.7` - unknown; unknown

```console
$ docker pull emqx@sha256:dd3bbbb96dcc4b68baf65342c6a21b9823d447ab4b1885e31b16f99167788509
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2572375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb517a98e5b34cd172b0be13bd95c2cf36068984db6969a8c563accb9a671403`

```dockerfile
```

-	Layers:
	-	`sha256:5dd0ef27adb8bfba84a8a3bbd60855144597953b9ee86a6b30793bdc44cdb30c`  
		Last Modified: Mon, 08 Jul 2024 19:14:21 GMT  
		Size: 2.6 MB (2559768 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b57ba143a92dd352085be44c5cc683e7846827132d92ab0aa6c287b80b3d3ac`  
		Last Modified: Mon, 08 Jul 2024 19:14:20 GMT  
		Size: 12.6 KB (12607 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.7.1`

```console
$ docker pull emqx@sha256:34d1e4eb60a8388c0e81cb51437f49cfdc82173bfa19bb6657bb3b71278f1a29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	unknown; unknown

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
$ docker pull emqx@sha256:074ff8d864916263abc6e8c42120a7efa67fea641cb6a3a070a3614a2c5b66d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.8 MB (122815523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:573da311dffd01ef129754dc5a68bc6494d88d070bb031800b6881927091e973`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Thu, 27 Jun 2024 06:50:32 GMT
ADD file:cbda549b25cd4337cd3ce345e3b66c0d3b43c247d7315906a028f98a56c41f1d in / 
# Thu, 27 Jun 2024 06:50:32 GMT
CMD ["bash"]
# Thu, 27 Jun 2024 06:50:32 GMT
ENV EMQX_VERSION=5.7.1
# Thu, 27 Jun 2024 06:50:32 GMT
ENV AMD64_SHA256=6896263e24c1211fea0e15464afb39931e9b4c7139804e0a6fb5f143826efaf8
# Thu, 27 Jun 2024 06:50:32 GMT
ENV ARM64_SHA256=c321477bab28e381a472761c2d62f9e5acf6290f298f5aaf9404ab70feb6d587
# Thu, 27 Jun 2024 06:50:32 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Thu, 27 Jun 2024 06:50:32 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Thu, 27 Jun 2024 06:50:32 GMT
WORKDIR /opt/emqx
# Thu, 27 Jun 2024 06:50:32 GMT
USER emqx
# Thu, 27 Jun 2024 06:50:32 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Thu, 27 Jun 2024 06:50:32 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Thu, 27 Jun 2024 06:50:32 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Thu, 27 Jun 2024 06:50:32 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Thu, 27 Jun 2024 06:50:32 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:ea235d1ccf77ca07a545b448996766dc3eca4b971b04ba39d50af69660b25751`  
		Last Modified: Tue, 02 Jul 2024 00:42:25 GMT  
		Size: 29.2 MB (29156563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b31646db1381832e88900fde1500ba647e8458191411a4d10dcc4c8becfe406`  
		Last Modified: Mon, 08 Jul 2024 19:14:23 GMT  
		Size: 93.7 MB (93657896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:762d975f3920ce02bd4da5ca7a8fdc83b4f8f921649f9451c80a10c3edccf678`  
		Last Modified: Mon, 08 Jul 2024 19:14:20 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.7.1` - unknown; unknown

```console
$ docker pull emqx@sha256:dd3bbbb96dcc4b68baf65342c6a21b9823d447ab4b1885e31b16f99167788509
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2572375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb517a98e5b34cd172b0be13bd95c2cf36068984db6969a8c563accb9a671403`

```dockerfile
```

-	Layers:
	-	`sha256:5dd0ef27adb8bfba84a8a3bbd60855144597953b9ee86a6b30793bdc44cdb30c`  
		Last Modified: Mon, 08 Jul 2024 19:14:21 GMT  
		Size: 2.6 MB (2559768 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b57ba143a92dd352085be44c5cc683e7846827132d92ab0aa6c287b80b3d3ac`  
		Last Modified: Mon, 08 Jul 2024 19:14:20 GMT  
		Size: 12.6 KB (12607 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:latest`

```console
$ docker pull emqx@sha256:34d1e4eb60a8388c0e81cb51437f49cfdc82173bfa19bb6657bb3b71278f1a29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	unknown; unknown

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
$ docker pull emqx@sha256:074ff8d864916263abc6e8c42120a7efa67fea641cb6a3a070a3614a2c5b66d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.8 MB (122815523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:573da311dffd01ef129754dc5a68bc6494d88d070bb031800b6881927091e973`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Thu, 27 Jun 2024 06:50:32 GMT
ADD file:cbda549b25cd4337cd3ce345e3b66c0d3b43c247d7315906a028f98a56c41f1d in / 
# Thu, 27 Jun 2024 06:50:32 GMT
CMD ["bash"]
# Thu, 27 Jun 2024 06:50:32 GMT
ENV EMQX_VERSION=5.7.1
# Thu, 27 Jun 2024 06:50:32 GMT
ENV AMD64_SHA256=6896263e24c1211fea0e15464afb39931e9b4c7139804e0a6fb5f143826efaf8
# Thu, 27 Jun 2024 06:50:32 GMT
ENV ARM64_SHA256=c321477bab28e381a472761c2d62f9e5acf6290f298f5aaf9404ab70feb6d587
# Thu, 27 Jun 2024 06:50:32 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Thu, 27 Jun 2024 06:50:32 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Thu, 27 Jun 2024 06:50:32 GMT
WORKDIR /opt/emqx
# Thu, 27 Jun 2024 06:50:32 GMT
USER emqx
# Thu, 27 Jun 2024 06:50:32 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Thu, 27 Jun 2024 06:50:32 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Thu, 27 Jun 2024 06:50:32 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Thu, 27 Jun 2024 06:50:32 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Thu, 27 Jun 2024 06:50:32 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:ea235d1ccf77ca07a545b448996766dc3eca4b971b04ba39d50af69660b25751`  
		Last Modified: Tue, 02 Jul 2024 00:42:25 GMT  
		Size: 29.2 MB (29156563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b31646db1381832e88900fde1500ba647e8458191411a4d10dcc4c8becfe406`  
		Last Modified: Mon, 08 Jul 2024 19:14:23 GMT  
		Size: 93.7 MB (93657896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:762d975f3920ce02bd4da5ca7a8fdc83b4f8f921649f9451c80a10c3edccf678`  
		Last Modified: Mon, 08 Jul 2024 19:14:20 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:latest` - unknown; unknown

```console
$ docker pull emqx@sha256:dd3bbbb96dcc4b68baf65342c6a21b9823d447ab4b1885e31b16f99167788509
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2572375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb517a98e5b34cd172b0be13bd95c2cf36068984db6969a8c563accb9a671403`

```dockerfile
```

-	Layers:
	-	`sha256:5dd0ef27adb8bfba84a8a3bbd60855144597953b9ee86a6b30793bdc44cdb30c`  
		Last Modified: Mon, 08 Jul 2024 19:14:21 GMT  
		Size: 2.6 MB (2559768 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b57ba143a92dd352085be44c5cc683e7846827132d92ab0aa6c287b80b3d3ac`  
		Last Modified: Mon, 08 Jul 2024 19:14:20 GMT  
		Size: 12.6 KB (12607 bytes)  
		MIME: application/vnd.in-toto+json
