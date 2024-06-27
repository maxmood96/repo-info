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
$ docker pull emqx@sha256:47b29b52b625a4da3508f53afd532074ef560b9b6afabd67ce688d18a6171490
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5` - linux; amd64

```console
$ docker pull emqx@sha256:722144392b1f5ef1298f51b2819f47638f1bbef86dd3432ab08441eba90d6a34
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.9 MB (125874540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd4abaec15ba22847f6bafcabef9baad0298e9848b4fe42fbaf83388b5297560`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Thu, 13 Jun 2024 01:20:56 GMT
ADD file:5f9954090af042b377ea0d1d184faa64d2e9d4c946b6c3898d52aff47e764056 in / 
# Thu, 13 Jun 2024 01:20:56 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 03:56:54 GMT
ENV EMQX_VERSION=5.7.0
# Thu, 13 Jun 2024 03:56:54 GMT
ENV AMD64_SHA256=910d6ff5af8c36df9d15ae99a9ffe03a9690849fd952b7666b5809d9f9c42180
# Thu, 13 Jun 2024 03:56:54 GMT
ENV ARM64_SHA256=4e7c4e3f321f6ce8de5d9da93e96769a49174f62ffecc61451b2292e6f3e415f
# Thu, 13 Jun 2024 03:56:54 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Thu, 13 Jun 2024 03:57:09 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 13 Jun 2024 03:57:09 GMT
WORKDIR /opt/emqx
# Thu, 13 Jun 2024 03:57:09 GMT
USER emqx
# Thu, 13 Jun 2024 03:57:10 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Thu, 13 Jun 2024 03:57:10 GMT
EXPOSE 18083 1883 4370 5369 8083 8084 8883
# Thu, 13 Jun 2024 03:57:10 GMT
COPY file:f0e3faa715cc7e845bbdf3b121a4a8bad40d65e5cef1fac9f1285fec250cedf2 in /usr/bin/ 
# Thu, 13 Jun 2024 03:57:10 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Thu, 13 Jun 2024 03:57:10 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:2cc3ae149d28a36d28d4eefbae70aaa14a0c9eab588c3790f7979f310b893c44`  
		Last Modified: Thu, 13 Jun 2024 01:25:30 GMT  
		Size: 29.2 MB (29150430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59e1e8d8153defc8ad008583f7e666aedc4ad4ea415c563c3e8ddc71572a52ff`  
		Last Modified: Thu, 13 Jun 2024 03:59:17 GMT  
		Size: 96.7 MB (96723077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34bdc935b2ea217ab47e87cd78f93f2a87c79e989276f72c3fc93133ac1d84ff`  
		Last Modified: Thu, 13 Jun 2024 03:59:07 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:5` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:1fc5d43018076be2ecc2ae71068c669653ffe516eb37acb85fcc853507ed0430
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.5 MB (122455516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f378277c2b8a5a2f3966d49bc49b40cadb367a581b68d56ef4926ed130501342`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Thu, 13 Jun 2024 00:39:50 GMT
ADD file:5f17f77072bcd27aa8c4d09ef5117423b789c42445b6e6c13af711dfb2abd544 in / 
# Thu, 13 Jun 2024 00:39:51 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 07:26:07 GMT
ENV EMQX_VERSION=5.7.0
# Thu, 13 Jun 2024 07:26:07 GMT
ENV AMD64_SHA256=910d6ff5af8c36df9d15ae99a9ffe03a9690849fd952b7666b5809d9f9c42180
# Thu, 13 Jun 2024 07:26:08 GMT
ENV ARM64_SHA256=4e7c4e3f321f6ce8de5d9da93e96769a49174f62ffecc61451b2292e6f3e415f
# Thu, 13 Jun 2024 07:26:08 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Thu, 13 Jun 2024 07:26:20 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 13 Jun 2024 07:26:21 GMT
WORKDIR /opt/emqx
# Thu, 13 Jun 2024 07:26:21 GMT
USER emqx
# Thu, 13 Jun 2024 07:26:21 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Thu, 13 Jun 2024 07:26:21 GMT
EXPOSE 18083 1883 4370 5369 8083 8084 8883
# Thu, 13 Jun 2024 07:26:21 GMT
COPY file:f0e3faa715cc7e845bbdf3b121a4a8bad40d65e5cef1fac9f1285fec250cedf2 in /usr/bin/ 
# Thu, 13 Jun 2024 07:26:22 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Thu, 13 Jun 2024 07:26:22 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:559a764445207341cf1207d83ceb89f1e59e2b57e860b7a80a6df6447641832b`  
		Last Modified: Thu, 13 Jun 2024 00:43:13 GMT  
		Size: 29.2 MB (29179666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e367470c1980076f657cd7f5436ef848086e592a06e509987b05c21870843c80`  
		Last Modified: Thu, 13 Jun 2024 07:28:10 GMT  
		Size: 93.3 MB (93274815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6b447fda4b95d70109b3417028bdcd0cf5cea71fa7635954581d7894f4d9088`  
		Last Modified: Thu, 13 Jun 2024 07:28:02 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:5.1`

```console
$ docker pull emqx@sha256:1ee592dbdfe92eb59d60977c86d73202bec533aa1ef023f9c7675aef98ec9a4b
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
$ docker pull emqx@sha256:9ce015509b76ee86faaf0eaffee9f9b5cebe4fa3ba2c0a1cf74cee9f6d9de282
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.7 MB (92722656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e805a0ef8496bb8cd1cf34f13d082c4eea14cb23807a21c5a43f8fdb68e941e3`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Thu, 13 Jun 2024 00:40:06 GMT
ADD file:55edb70d595bba9782144ef15994a2ae5c40adeb65f6c3acd6570a0c148ffa96 in / 
# Thu, 13 Jun 2024 00:40:06 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 07:24:33 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 07:24:34 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Thu, 13 Jun 2024 07:24:34 GMT
ENV EMQX_VERSION=5.1.6
# Thu, 13 Jun 2024 07:24:34 GMT
ENV AMD64_SHA256=5c65f7538141e93d71d1dd7d088589339ef6a091b90f901604a2e0e004f5f4aa
# Thu, 13 Jun 2024 07:24:34 GMT
ENV ARM64_SHA256=ae832d29d6b4e7fa43f3bf04c8c9fad4c9047f079d1587d3ed2a3564d5ea8147
# Thu, 13 Jun 2024 07:24:34 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Thu, 13 Jun 2024 07:24:40 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg
# Thu, 13 Jun 2024 07:24:41 GMT
WORKDIR /opt/emqx
# Thu, 13 Jun 2024 07:24:41 GMT
USER emqx
# Thu, 13 Jun 2024 07:24:41 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Thu, 13 Jun 2024 07:24:41 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Thu, 13 Jun 2024 07:24:41 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Thu, 13 Jun 2024 07:24:41 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Thu, 13 Jun 2024 07:24:41 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:ca4da1869379178993d4f7abc946f75e7515789ff7e15c7ccfedfc8e2bfeaf6d`  
		Last Modified: Thu, 13 Jun 2024 00:43:54 GMT  
		Size: 30.1 MB (30086973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:183cb54505e3874cbfbfc1884479f71ebd1cc1af629ccd554fdfe3ba11cc3890`  
		Last Modified: Thu, 13 Jun 2024 07:26:38 GMT  
		Size: 3.0 MB (3005963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83d9448e01fd22f9ce31c89496f73492264b4318e8672cf62c14c2a6c00eb7f2`  
		Last Modified: Thu, 13 Jun 2024 07:26:37 GMT  
		Size: 4.1 KB (4088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73c57df79c7b8dffa967681bc80b4519159ff71bc63cd12a4a0c96f26e19f591`  
		Last Modified: Thu, 13 Jun 2024 07:26:43 GMT  
		Size: 59.6 MB (59624729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a57b37dfa93c86059ecd2b5e1478034e8e909103f68ffcab0e2b5f9dede0a42`  
		Last Modified: Thu, 13 Jun 2024 07:26:38 GMT  
		Size: 903.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:5.1.6`

```console
$ docker pull emqx@sha256:1ee592dbdfe92eb59d60977c86d73202bec533aa1ef023f9c7675aef98ec9a4b
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
$ docker pull emqx@sha256:9ce015509b76ee86faaf0eaffee9f9b5cebe4fa3ba2c0a1cf74cee9f6d9de282
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.7 MB (92722656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e805a0ef8496bb8cd1cf34f13d082c4eea14cb23807a21c5a43f8fdb68e941e3`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Thu, 13 Jun 2024 00:40:06 GMT
ADD file:55edb70d595bba9782144ef15994a2ae5c40adeb65f6c3acd6570a0c148ffa96 in / 
# Thu, 13 Jun 2024 00:40:06 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 07:24:33 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 07:24:34 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Thu, 13 Jun 2024 07:24:34 GMT
ENV EMQX_VERSION=5.1.6
# Thu, 13 Jun 2024 07:24:34 GMT
ENV AMD64_SHA256=5c65f7538141e93d71d1dd7d088589339ef6a091b90f901604a2e0e004f5f4aa
# Thu, 13 Jun 2024 07:24:34 GMT
ENV ARM64_SHA256=ae832d29d6b4e7fa43f3bf04c8c9fad4c9047f079d1587d3ed2a3564d5ea8147
# Thu, 13 Jun 2024 07:24:34 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Thu, 13 Jun 2024 07:24:40 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg
# Thu, 13 Jun 2024 07:24:41 GMT
WORKDIR /opt/emqx
# Thu, 13 Jun 2024 07:24:41 GMT
USER emqx
# Thu, 13 Jun 2024 07:24:41 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Thu, 13 Jun 2024 07:24:41 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Thu, 13 Jun 2024 07:24:41 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Thu, 13 Jun 2024 07:24:41 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Thu, 13 Jun 2024 07:24:41 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:ca4da1869379178993d4f7abc946f75e7515789ff7e15c7ccfedfc8e2bfeaf6d`  
		Last Modified: Thu, 13 Jun 2024 00:43:54 GMT  
		Size: 30.1 MB (30086973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:183cb54505e3874cbfbfc1884479f71ebd1cc1af629ccd554fdfe3ba11cc3890`  
		Last Modified: Thu, 13 Jun 2024 07:26:38 GMT  
		Size: 3.0 MB (3005963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83d9448e01fd22f9ce31c89496f73492264b4318e8672cf62c14c2a6c00eb7f2`  
		Last Modified: Thu, 13 Jun 2024 07:26:37 GMT  
		Size: 4.1 KB (4088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73c57df79c7b8dffa967681bc80b4519159ff71bc63cd12a4a0c96f26e19f591`  
		Last Modified: Thu, 13 Jun 2024 07:26:43 GMT  
		Size: 59.6 MB (59624729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a57b37dfa93c86059ecd2b5e1478034e8e909103f68ffcab0e2b5f9dede0a42`  
		Last Modified: Thu, 13 Jun 2024 07:26:38 GMT  
		Size: 903.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:5.2`

```console
$ docker pull emqx@sha256:620b98205e7a9f75a8193111e090e1e1bbc8931bd34aabf5b6872d56290500da
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
$ docker pull emqx@sha256:760ddabba3b3fac4bd23aa3913a6e97d7a06bede68bc755c8ffdd8842b50b154
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.5 MB (91489263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e53779f3001e55ab028c01237e5e235f2f2bd3407ff0a9903357a86d06f8f9db`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Thu, 13 Jun 2024 00:40:06 GMT
ADD file:55edb70d595bba9782144ef15994a2ae5c40adeb65f6c3acd6570a0c148ffa96 in / 
# Thu, 13 Jun 2024 00:40:06 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 07:24:49 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 07:24:49 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Thu, 13 Jun 2024 07:24:49 GMT
ENV EMQX_VERSION=5.2.1
# Thu, 13 Jun 2024 07:24:49 GMT
ENV AMD64_SHA256=359a12811e5e6725e4269d9484abd348effdde35c0f2af1f5b63cae790c73020
# Thu, 13 Jun 2024 07:24:50 GMT
ENV ARM64_SHA256=2e0a3e0b33669c9b6da488970a2f92d08d7bd0824295822b205b83461ba4728d
# Thu, 13 Jun 2024 07:24:50 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Thu, 13 Jun 2024 07:24:58 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl;     rm -rf /var/lib/apt/lists/*;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl
# Thu, 13 Jun 2024 07:24:59 GMT
WORKDIR /opt/emqx
# Thu, 13 Jun 2024 07:24:59 GMT
USER emqx
# Thu, 13 Jun 2024 07:24:59 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Thu, 13 Jun 2024 07:24:59 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Thu, 13 Jun 2024 07:24:59 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Thu, 13 Jun 2024 07:24:59 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Thu, 13 Jun 2024 07:24:59 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:ca4da1869379178993d4f7abc946f75e7515789ff7e15c7ccfedfc8e2bfeaf6d`  
		Last Modified: Thu, 13 Jun 2024 00:43:54 GMT  
		Size: 30.1 MB (30086973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:325a547eeeaf45250e7b95fa8de664160b22ef0821b3cd5c30c762e30f575396`  
		Last Modified: Thu, 13 Jun 2024 07:26:51 GMT  
		Size: 1.6 MB (1645689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a64ab85eaefb6ed9b7ee536bdcb3b40bc178a075717d36b5cccb76574d73587`  
		Last Modified: Thu, 13 Jun 2024 07:26:51 GMT  
		Size: 4.1 KB (4088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d7f5a78e140b8add2760f222ba1f7cc784e8cf94dc9e6d482a6eb3c7c061d8a`  
		Last Modified: Thu, 13 Jun 2024 07:26:56 GMT  
		Size: 59.8 MB (59751612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92c9749ca4eb494ea876ff5ca187de35b7ecd31ca3d20b89d7500e5e61ce3301`  
		Last Modified: Thu, 13 Jun 2024 07:26:51 GMT  
		Size: 901.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:5.2.1`

```console
$ docker pull emqx@sha256:620b98205e7a9f75a8193111e090e1e1bbc8931bd34aabf5b6872d56290500da
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
$ docker pull emqx@sha256:760ddabba3b3fac4bd23aa3913a6e97d7a06bede68bc755c8ffdd8842b50b154
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.5 MB (91489263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e53779f3001e55ab028c01237e5e235f2f2bd3407ff0a9903357a86d06f8f9db`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Thu, 13 Jun 2024 00:40:06 GMT
ADD file:55edb70d595bba9782144ef15994a2ae5c40adeb65f6c3acd6570a0c148ffa96 in / 
# Thu, 13 Jun 2024 00:40:06 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 07:24:49 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 07:24:49 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Thu, 13 Jun 2024 07:24:49 GMT
ENV EMQX_VERSION=5.2.1
# Thu, 13 Jun 2024 07:24:49 GMT
ENV AMD64_SHA256=359a12811e5e6725e4269d9484abd348effdde35c0f2af1f5b63cae790c73020
# Thu, 13 Jun 2024 07:24:50 GMT
ENV ARM64_SHA256=2e0a3e0b33669c9b6da488970a2f92d08d7bd0824295822b205b83461ba4728d
# Thu, 13 Jun 2024 07:24:50 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Thu, 13 Jun 2024 07:24:58 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl;     rm -rf /var/lib/apt/lists/*;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl
# Thu, 13 Jun 2024 07:24:59 GMT
WORKDIR /opt/emqx
# Thu, 13 Jun 2024 07:24:59 GMT
USER emqx
# Thu, 13 Jun 2024 07:24:59 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Thu, 13 Jun 2024 07:24:59 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Thu, 13 Jun 2024 07:24:59 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Thu, 13 Jun 2024 07:24:59 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Thu, 13 Jun 2024 07:24:59 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:ca4da1869379178993d4f7abc946f75e7515789ff7e15c7ccfedfc8e2bfeaf6d`  
		Last Modified: Thu, 13 Jun 2024 00:43:54 GMT  
		Size: 30.1 MB (30086973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:325a547eeeaf45250e7b95fa8de664160b22ef0821b3cd5c30c762e30f575396`  
		Last Modified: Thu, 13 Jun 2024 07:26:51 GMT  
		Size: 1.6 MB (1645689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a64ab85eaefb6ed9b7ee536bdcb3b40bc178a075717d36b5cccb76574d73587`  
		Last Modified: Thu, 13 Jun 2024 07:26:51 GMT  
		Size: 4.1 KB (4088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d7f5a78e140b8add2760f222ba1f7cc784e8cf94dc9e6d482a6eb3c7c061d8a`  
		Last Modified: Thu, 13 Jun 2024 07:26:56 GMT  
		Size: 59.8 MB (59751612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92c9749ca4eb494ea876ff5ca187de35b7ecd31ca3d20b89d7500e5e61ce3301`  
		Last Modified: Thu, 13 Jun 2024 07:26:51 GMT  
		Size: 901.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:5.3`

```console
$ docker pull emqx@sha256:2ffa699b2cd082d6fb6ddf48733f3675246b69764d5869333c561a8777e144ea
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
$ docker pull emqx@sha256:6ef3df8639696cb4d16f692a508891a740e9200260b619057f5f40ad4d165062
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.1 MB (92102819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0301bb15348381a6f65480c2433084044ebcaab67992202d74516f96d93fa54c`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Thu, 13 Jun 2024 00:40:06 GMT
ADD file:55edb70d595bba9782144ef15994a2ae5c40adeb65f6c3acd6570a0c148ffa96 in / 
# Thu, 13 Jun 2024 00:40:06 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 07:25:01 GMT
ENV EMQX_VERSION=5.3.2
# Thu, 13 Jun 2024 07:25:01 GMT
ENV AMD64_SHA256=d5948d4171f57e77756dd6c9eeb745c39e391e75aad3798fce445f44f5690be0
# Thu, 13 Jun 2024 07:25:01 GMT
ENV ARM64_SHA256=82b056bb1c1cd1f16e9d0719150fa8ac19c499d29563738bcd6984b3c395c6ac
# Thu, 13 Jun 2024 07:25:02 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Thu, 13 Jun 2024 07:25:13 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 07:25:13 GMT
WORKDIR /opt/emqx
# Thu, 13 Jun 2024 07:25:13 GMT
USER emqx
# Thu, 13 Jun 2024 07:25:14 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Thu, 13 Jun 2024 07:25:14 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Thu, 13 Jun 2024 07:25:14 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Thu, 13 Jun 2024 07:25:14 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Thu, 13 Jun 2024 07:25:14 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:ca4da1869379178993d4f7abc946f75e7515789ff7e15c7ccfedfc8e2bfeaf6d`  
		Last Modified: Thu, 13 Jun 2024 00:43:54 GMT  
		Size: 30.1 MB (30086973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9daabaf0c01a31731994be700ba760e550374950ec5e850580e512b39a6dc330`  
		Last Modified: Thu, 13 Jun 2024 07:27:08 GMT  
		Size: 62.0 MB (62014944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b7b44abe9bf3481a3f74b8584b3d5c5856922cf67e83d0bb47b78b5f5758fa0`  
		Last Modified: Thu, 13 Jun 2024 07:27:03 GMT  
		Size: 902.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:5.3.2`

```console
$ docker pull emqx@sha256:2ffa699b2cd082d6fb6ddf48733f3675246b69764d5869333c561a8777e144ea
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
$ docker pull emqx@sha256:6ef3df8639696cb4d16f692a508891a740e9200260b619057f5f40ad4d165062
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.1 MB (92102819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0301bb15348381a6f65480c2433084044ebcaab67992202d74516f96d93fa54c`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Thu, 13 Jun 2024 00:40:06 GMT
ADD file:55edb70d595bba9782144ef15994a2ae5c40adeb65f6c3acd6570a0c148ffa96 in / 
# Thu, 13 Jun 2024 00:40:06 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 07:25:01 GMT
ENV EMQX_VERSION=5.3.2
# Thu, 13 Jun 2024 07:25:01 GMT
ENV AMD64_SHA256=d5948d4171f57e77756dd6c9eeb745c39e391e75aad3798fce445f44f5690be0
# Thu, 13 Jun 2024 07:25:01 GMT
ENV ARM64_SHA256=82b056bb1c1cd1f16e9d0719150fa8ac19c499d29563738bcd6984b3c395c6ac
# Thu, 13 Jun 2024 07:25:02 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Thu, 13 Jun 2024 07:25:13 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 07:25:13 GMT
WORKDIR /opt/emqx
# Thu, 13 Jun 2024 07:25:13 GMT
USER emqx
# Thu, 13 Jun 2024 07:25:14 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Thu, 13 Jun 2024 07:25:14 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Thu, 13 Jun 2024 07:25:14 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Thu, 13 Jun 2024 07:25:14 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Thu, 13 Jun 2024 07:25:14 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:ca4da1869379178993d4f7abc946f75e7515789ff7e15c7ccfedfc8e2bfeaf6d`  
		Last Modified: Thu, 13 Jun 2024 00:43:54 GMT  
		Size: 30.1 MB (30086973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9daabaf0c01a31731994be700ba760e550374950ec5e850580e512b39a6dc330`  
		Last Modified: Thu, 13 Jun 2024 07:27:08 GMT  
		Size: 62.0 MB (62014944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b7b44abe9bf3481a3f74b8584b3d5c5856922cf67e83d0bb47b78b5f5758fa0`  
		Last Modified: Thu, 13 Jun 2024 07:27:03 GMT  
		Size: 902.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:5.4`

```console
$ docker pull emqx@sha256:8fcd370fb3547894a719daacca01bbb3a4786444da59c8dd8c3e91381fa951c7
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
$ docker pull emqx@sha256:1b8b8ce8382e633420a468698545e98e186477277236bfc8879bcadbf352b3d1
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.5 MB (108498951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71c1d03dab1726b59e3511319e6a4030aa691f7cf7048dd27c49ede05bd56f85`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Thu, 13 Jun 2024 00:40:06 GMT
ADD file:55edb70d595bba9782144ef15994a2ae5c40adeb65f6c3acd6570a0c148ffa96 in / 
# Thu, 13 Jun 2024 00:40:06 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 07:25:18 GMT
ENV EMQX_VERSION=5.4.1
# Thu, 13 Jun 2024 07:25:18 GMT
ENV AMD64_SHA256=c2087651d72f17999f52d73ff22cd8f23dc5fa5db8b5a90a8bc4a1410b03affb
# Thu, 13 Jun 2024 07:25:18 GMT
ENV ARM64_SHA256=6c53a68ae907f7b4a3cdcd4dbee4f839b07853695ac1c039b51fd97d993073bc
# Thu, 13 Jun 2024 07:25:18 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Thu, 13 Jun 2024 07:25:30 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 07:25:31 GMT
WORKDIR /opt/emqx
# Thu, 13 Jun 2024 07:25:31 GMT
USER emqx
# Thu, 13 Jun 2024 07:25:31 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Thu, 13 Jun 2024 07:25:31 GMT
EXPOSE 18083 1883 4370 5369 8083 8084 8883
# Thu, 13 Jun 2024 07:25:31 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Thu, 13 Jun 2024 07:25:31 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Thu, 13 Jun 2024 07:25:31 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:ca4da1869379178993d4f7abc946f75e7515789ff7e15c7ccfedfc8e2bfeaf6d`  
		Last Modified: Thu, 13 Jun 2024 00:43:54 GMT  
		Size: 30.1 MB (30086973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74d4d6d7f963ce0f48653eae5452439dc7b089751f5e4601a51721d1fab35b65`  
		Last Modified: Thu, 13 Jun 2024 07:27:22 GMT  
		Size: 78.4 MB (78411076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e63bb493c2c99be6537db40193f4f944904ed1140eb48847e1269d5fa26703bc`  
		Last Modified: Thu, 13 Jun 2024 07:27:16 GMT  
		Size: 902.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:5.4.1`

```console
$ docker pull emqx@sha256:8fcd370fb3547894a719daacca01bbb3a4786444da59c8dd8c3e91381fa951c7
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
$ docker pull emqx@sha256:1b8b8ce8382e633420a468698545e98e186477277236bfc8879bcadbf352b3d1
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.5 MB (108498951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71c1d03dab1726b59e3511319e6a4030aa691f7cf7048dd27c49ede05bd56f85`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Thu, 13 Jun 2024 00:40:06 GMT
ADD file:55edb70d595bba9782144ef15994a2ae5c40adeb65f6c3acd6570a0c148ffa96 in / 
# Thu, 13 Jun 2024 00:40:06 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 07:25:18 GMT
ENV EMQX_VERSION=5.4.1
# Thu, 13 Jun 2024 07:25:18 GMT
ENV AMD64_SHA256=c2087651d72f17999f52d73ff22cd8f23dc5fa5db8b5a90a8bc4a1410b03affb
# Thu, 13 Jun 2024 07:25:18 GMT
ENV ARM64_SHA256=6c53a68ae907f7b4a3cdcd4dbee4f839b07853695ac1c039b51fd97d993073bc
# Thu, 13 Jun 2024 07:25:18 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Thu, 13 Jun 2024 07:25:30 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 07:25:31 GMT
WORKDIR /opt/emqx
# Thu, 13 Jun 2024 07:25:31 GMT
USER emqx
# Thu, 13 Jun 2024 07:25:31 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Thu, 13 Jun 2024 07:25:31 GMT
EXPOSE 18083 1883 4370 5369 8083 8084 8883
# Thu, 13 Jun 2024 07:25:31 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Thu, 13 Jun 2024 07:25:31 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Thu, 13 Jun 2024 07:25:31 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:ca4da1869379178993d4f7abc946f75e7515789ff7e15c7ccfedfc8e2bfeaf6d`  
		Last Modified: Thu, 13 Jun 2024 00:43:54 GMT  
		Size: 30.1 MB (30086973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74d4d6d7f963ce0f48653eae5452439dc7b089751f5e4601a51721d1fab35b65`  
		Last Modified: Thu, 13 Jun 2024 07:27:22 GMT  
		Size: 78.4 MB (78411076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e63bb493c2c99be6537db40193f4f944904ed1140eb48847e1269d5fa26703bc`  
		Last Modified: Thu, 13 Jun 2024 07:27:16 GMT  
		Size: 902.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:5.5`

```console
$ docker pull emqx@sha256:de791394b020912b98fa6f11c518766b9087099f3292784bcbf092c97f5cec4e
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
$ docker pull emqx@sha256:7ac876afc74b9b2743f8a49ee091f515d45466a6eac44d27782d126c0cc95fc2
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.8 MB (116796968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7837c744c9709ab149a7d8e53f63835dd4b95bce2516d9017a45e579c4bbf7e4`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Thu, 13 Jun 2024 00:40:06 GMT
ADD file:55edb70d595bba9782144ef15994a2ae5c40adeb65f6c3acd6570a0c148ffa96 in / 
# Thu, 13 Jun 2024 00:40:06 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 07:25:34 GMT
ENV EMQX_VERSION=5.5.1
# Thu, 13 Jun 2024 07:25:35 GMT
ENV AMD64_SHA256=8bac2886987a632aab1c738aa3de28684b415d3b1e1f9489b458c819254673a6
# Thu, 13 Jun 2024 07:25:35 GMT
ENV ARM64_SHA256=8b962ad8beea50fb92dc0b93d2ab8a5064752147b70bbf46fd221bc4cc29c32d
# Thu, 13 Jun 2024 07:25:35 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Thu, 13 Jun 2024 07:25:47 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     mkdir -p /opt/emqx/log /opt/emqx/data /opt/emqx/plugins;     chown -R emqx:emqx /opt/emqx/log /opt/emqx/data /opt/emqx/plugins;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 13 Jun 2024 07:25:48 GMT
WORKDIR /opt/emqx
# Thu, 13 Jun 2024 07:25:48 GMT
USER emqx
# Thu, 13 Jun 2024 07:25:48 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Thu, 13 Jun 2024 07:25:48 GMT
EXPOSE 18083 1883 4370 5369 8083 8084 8883
# Thu, 13 Jun 2024 07:25:48 GMT
COPY file:f0e3faa715cc7e845bbdf3b121a4a8bad40d65e5cef1fac9f1285fec250cedf2 in /usr/bin/ 
# Thu, 13 Jun 2024 07:25:48 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Thu, 13 Jun 2024 07:25:48 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:ca4da1869379178993d4f7abc946f75e7515789ff7e15c7ccfedfc8e2bfeaf6d`  
		Last Modified: Thu, 13 Jun 2024 00:43:54 GMT  
		Size: 30.1 MB (30086973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fbbd8d4c3d4f76c7c5ee82032ed34ad427148237bdc85ad375e663b73a315cb`  
		Last Modified: Thu, 13 Jun 2024 07:27:38 GMT  
		Size: 86.7 MB (86708960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b88b17ec00c2c4f8d88b646093535f67e2d6067428500b5cad5374f7fc842a57`  
		Last Modified: Thu, 13 Jun 2024 07:27:30 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:5.5.1`

```console
$ docker pull emqx@sha256:de791394b020912b98fa6f11c518766b9087099f3292784bcbf092c97f5cec4e
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
$ docker pull emqx@sha256:7ac876afc74b9b2743f8a49ee091f515d45466a6eac44d27782d126c0cc95fc2
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.8 MB (116796968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7837c744c9709ab149a7d8e53f63835dd4b95bce2516d9017a45e579c4bbf7e4`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Thu, 13 Jun 2024 00:40:06 GMT
ADD file:55edb70d595bba9782144ef15994a2ae5c40adeb65f6c3acd6570a0c148ffa96 in / 
# Thu, 13 Jun 2024 00:40:06 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 07:25:34 GMT
ENV EMQX_VERSION=5.5.1
# Thu, 13 Jun 2024 07:25:35 GMT
ENV AMD64_SHA256=8bac2886987a632aab1c738aa3de28684b415d3b1e1f9489b458c819254673a6
# Thu, 13 Jun 2024 07:25:35 GMT
ENV ARM64_SHA256=8b962ad8beea50fb92dc0b93d2ab8a5064752147b70bbf46fd221bc4cc29c32d
# Thu, 13 Jun 2024 07:25:35 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Thu, 13 Jun 2024 07:25:47 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     mkdir -p /opt/emqx/log /opt/emqx/data /opt/emqx/plugins;     chown -R emqx:emqx /opt/emqx/log /opt/emqx/data /opt/emqx/plugins;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 13 Jun 2024 07:25:48 GMT
WORKDIR /opt/emqx
# Thu, 13 Jun 2024 07:25:48 GMT
USER emqx
# Thu, 13 Jun 2024 07:25:48 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Thu, 13 Jun 2024 07:25:48 GMT
EXPOSE 18083 1883 4370 5369 8083 8084 8883
# Thu, 13 Jun 2024 07:25:48 GMT
COPY file:f0e3faa715cc7e845bbdf3b121a4a8bad40d65e5cef1fac9f1285fec250cedf2 in /usr/bin/ 
# Thu, 13 Jun 2024 07:25:48 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Thu, 13 Jun 2024 07:25:48 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:ca4da1869379178993d4f7abc946f75e7515789ff7e15c7ccfedfc8e2bfeaf6d`  
		Last Modified: Thu, 13 Jun 2024 00:43:54 GMT  
		Size: 30.1 MB (30086973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fbbd8d4c3d4f76c7c5ee82032ed34ad427148237bdc85ad375e663b73a315cb`  
		Last Modified: Thu, 13 Jun 2024 07:27:38 GMT  
		Size: 86.7 MB (86708960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b88b17ec00c2c4f8d88b646093535f67e2d6067428500b5cad5374f7fc842a57`  
		Last Modified: Thu, 13 Jun 2024 07:27:30 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:5.6`

```console
$ docker pull emqx@sha256:c72ac3527a23c9c8fc147b3311b2002635500b400bd1d5053a0c74b9247b8f2e
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
$ docker pull emqx@sha256:ff81231af9af42f63c6e6a8031c9e3bd48d4c9274de82dac76956c9792975847
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.8 MB (120796171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb6d56b01f338cf0e9b6308a2fea43e01584d9535cca5bc2c5a8e4f7b168d2ad`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Thu, 13 Jun 2024 00:39:50 GMT
ADD file:5f17f77072bcd27aa8c4d09ef5117423b789c42445b6e6c13af711dfb2abd544 in / 
# Thu, 13 Jun 2024 00:39:51 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 07:25:51 GMT
ENV EMQX_VERSION=5.6.1
# Thu, 13 Jun 2024 07:25:51 GMT
ENV AMD64_SHA256=a5be37660bfe6130bc159b934ed98ffcb9bef5519765491b4ed38d08ba304538
# Thu, 13 Jun 2024 07:25:51 GMT
ENV ARM64_SHA256=3f7f9b10d313f760af43e0a54cba2af4eb23ad3864b439196cb8b2903baf5651
# Thu, 13 Jun 2024 07:25:51 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Thu, 13 Jun 2024 07:26:04 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 13 Jun 2024 07:26:05 GMT
WORKDIR /opt/emqx
# Thu, 13 Jun 2024 07:26:05 GMT
USER emqx
# Thu, 13 Jun 2024 07:26:05 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Thu, 13 Jun 2024 07:26:05 GMT
EXPOSE 18083 1883 4370 5369 8083 8084 8883
# Thu, 13 Jun 2024 07:26:05 GMT
COPY file:f0e3faa715cc7e845bbdf3b121a4a8bad40d65e5cef1fac9f1285fec250cedf2 in /usr/bin/ 
# Thu, 13 Jun 2024 07:26:05 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Thu, 13 Jun 2024 07:26:05 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:559a764445207341cf1207d83ceb89f1e59e2b57e860b7a80a6df6447641832b`  
		Last Modified: Thu, 13 Jun 2024 00:43:13 GMT  
		Size: 29.2 MB (29179666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01ef6c331b6ab06e8075eea6ab8ada2dddbe9f37ce961368ffb96cb58b5801ed`  
		Last Modified: Thu, 13 Jun 2024 07:27:55 GMT  
		Size: 91.6 MB (91615470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36f76f2b0197f0155d27bfbaecf782343fd47a3b357dbf28831f0a8f2d4f195c`  
		Last Modified: Thu, 13 Jun 2024 07:27:47 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:5.6.1`

```console
$ docker pull emqx@sha256:c72ac3527a23c9c8fc147b3311b2002635500b400bd1d5053a0c74b9247b8f2e
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
$ docker pull emqx@sha256:ff81231af9af42f63c6e6a8031c9e3bd48d4c9274de82dac76956c9792975847
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.8 MB (120796171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb6d56b01f338cf0e9b6308a2fea43e01584d9535cca5bc2c5a8e4f7b168d2ad`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Thu, 13 Jun 2024 00:39:50 GMT
ADD file:5f17f77072bcd27aa8c4d09ef5117423b789c42445b6e6c13af711dfb2abd544 in / 
# Thu, 13 Jun 2024 00:39:51 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 07:25:51 GMT
ENV EMQX_VERSION=5.6.1
# Thu, 13 Jun 2024 07:25:51 GMT
ENV AMD64_SHA256=a5be37660bfe6130bc159b934ed98ffcb9bef5519765491b4ed38d08ba304538
# Thu, 13 Jun 2024 07:25:51 GMT
ENV ARM64_SHA256=3f7f9b10d313f760af43e0a54cba2af4eb23ad3864b439196cb8b2903baf5651
# Thu, 13 Jun 2024 07:25:51 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Thu, 13 Jun 2024 07:26:04 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 13 Jun 2024 07:26:05 GMT
WORKDIR /opt/emqx
# Thu, 13 Jun 2024 07:26:05 GMT
USER emqx
# Thu, 13 Jun 2024 07:26:05 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Thu, 13 Jun 2024 07:26:05 GMT
EXPOSE 18083 1883 4370 5369 8083 8084 8883
# Thu, 13 Jun 2024 07:26:05 GMT
COPY file:f0e3faa715cc7e845bbdf3b121a4a8bad40d65e5cef1fac9f1285fec250cedf2 in /usr/bin/ 
# Thu, 13 Jun 2024 07:26:05 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Thu, 13 Jun 2024 07:26:05 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:559a764445207341cf1207d83ceb89f1e59e2b57e860b7a80a6df6447641832b`  
		Last Modified: Thu, 13 Jun 2024 00:43:13 GMT  
		Size: 29.2 MB (29179666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01ef6c331b6ab06e8075eea6ab8ada2dddbe9f37ce961368ffb96cb58b5801ed`  
		Last Modified: Thu, 13 Jun 2024 07:27:55 GMT  
		Size: 91.6 MB (91615470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36f76f2b0197f0155d27bfbaecf782343fd47a3b357dbf28831f0a8f2d4f195c`  
		Last Modified: Thu, 13 Jun 2024 07:27:47 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:5.7`

```console
$ docker pull emqx@sha256:47b29b52b625a4da3508f53afd532074ef560b9b6afabd67ce688d18a6171490
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5.7` - linux; amd64

```console
$ docker pull emqx@sha256:722144392b1f5ef1298f51b2819f47638f1bbef86dd3432ab08441eba90d6a34
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.9 MB (125874540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd4abaec15ba22847f6bafcabef9baad0298e9848b4fe42fbaf83388b5297560`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Thu, 13 Jun 2024 01:20:56 GMT
ADD file:5f9954090af042b377ea0d1d184faa64d2e9d4c946b6c3898d52aff47e764056 in / 
# Thu, 13 Jun 2024 01:20:56 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 03:56:54 GMT
ENV EMQX_VERSION=5.7.0
# Thu, 13 Jun 2024 03:56:54 GMT
ENV AMD64_SHA256=910d6ff5af8c36df9d15ae99a9ffe03a9690849fd952b7666b5809d9f9c42180
# Thu, 13 Jun 2024 03:56:54 GMT
ENV ARM64_SHA256=4e7c4e3f321f6ce8de5d9da93e96769a49174f62ffecc61451b2292e6f3e415f
# Thu, 13 Jun 2024 03:56:54 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Thu, 13 Jun 2024 03:57:09 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 13 Jun 2024 03:57:09 GMT
WORKDIR /opt/emqx
# Thu, 13 Jun 2024 03:57:09 GMT
USER emqx
# Thu, 13 Jun 2024 03:57:10 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Thu, 13 Jun 2024 03:57:10 GMT
EXPOSE 18083 1883 4370 5369 8083 8084 8883
# Thu, 13 Jun 2024 03:57:10 GMT
COPY file:f0e3faa715cc7e845bbdf3b121a4a8bad40d65e5cef1fac9f1285fec250cedf2 in /usr/bin/ 
# Thu, 13 Jun 2024 03:57:10 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Thu, 13 Jun 2024 03:57:10 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:2cc3ae149d28a36d28d4eefbae70aaa14a0c9eab588c3790f7979f310b893c44`  
		Last Modified: Thu, 13 Jun 2024 01:25:30 GMT  
		Size: 29.2 MB (29150430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59e1e8d8153defc8ad008583f7e666aedc4ad4ea415c563c3e8ddc71572a52ff`  
		Last Modified: Thu, 13 Jun 2024 03:59:17 GMT  
		Size: 96.7 MB (96723077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34bdc935b2ea217ab47e87cd78f93f2a87c79e989276f72c3fc93133ac1d84ff`  
		Last Modified: Thu, 13 Jun 2024 03:59:07 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:5.7` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:1fc5d43018076be2ecc2ae71068c669653ffe516eb37acb85fcc853507ed0430
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.5 MB (122455516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f378277c2b8a5a2f3966d49bc49b40cadb367a581b68d56ef4926ed130501342`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Thu, 13 Jun 2024 00:39:50 GMT
ADD file:5f17f77072bcd27aa8c4d09ef5117423b789c42445b6e6c13af711dfb2abd544 in / 
# Thu, 13 Jun 2024 00:39:51 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 07:26:07 GMT
ENV EMQX_VERSION=5.7.0
# Thu, 13 Jun 2024 07:26:07 GMT
ENV AMD64_SHA256=910d6ff5af8c36df9d15ae99a9ffe03a9690849fd952b7666b5809d9f9c42180
# Thu, 13 Jun 2024 07:26:08 GMT
ENV ARM64_SHA256=4e7c4e3f321f6ce8de5d9da93e96769a49174f62ffecc61451b2292e6f3e415f
# Thu, 13 Jun 2024 07:26:08 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Thu, 13 Jun 2024 07:26:20 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 13 Jun 2024 07:26:21 GMT
WORKDIR /opt/emqx
# Thu, 13 Jun 2024 07:26:21 GMT
USER emqx
# Thu, 13 Jun 2024 07:26:21 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Thu, 13 Jun 2024 07:26:21 GMT
EXPOSE 18083 1883 4370 5369 8083 8084 8883
# Thu, 13 Jun 2024 07:26:21 GMT
COPY file:f0e3faa715cc7e845bbdf3b121a4a8bad40d65e5cef1fac9f1285fec250cedf2 in /usr/bin/ 
# Thu, 13 Jun 2024 07:26:22 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Thu, 13 Jun 2024 07:26:22 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:559a764445207341cf1207d83ceb89f1e59e2b57e860b7a80a6df6447641832b`  
		Last Modified: Thu, 13 Jun 2024 00:43:13 GMT  
		Size: 29.2 MB (29179666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e367470c1980076f657cd7f5436ef848086e592a06e509987b05c21870843c80`  
		Last Modified: Thu, 13 Jun 2024 07:28:10 GMT  
		Size: 93.3 MB (93274815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6b447fda4b95d70109b3417028bdcd0cf5cea71fa7635954581d7894f4d9088`  
		Last Modified: Thu, 13 Jun 2024 07:28:02 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:5.7.1`

```console
$ docker pull emqx@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `emqx:latest`

```console
$ docker pull emqx@sha256:47b29b52b625a4da3508f53afd532074ef560b9b6afabd67ce688d18a6171490
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:latest` - linux; amd64

```console
$ docker pull emqx@sha256:722144392b1f5ef1298f51b2819f47638f1bbef86dd3432ab08441eba90d6a34
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.9 MB (125874540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd4abaec15ba22847f6bafcabef9baad0298e9848b4fe42fbaf83388b5297560`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Thu, 13 Jun 2024 01:20:56 GMT
ADD file:5f9954090af042b377ea0d1d184faa64d2e9d4c946b6c3898d52aff47e764056 in / 
# Thu, 13 Jun 2024 01:20:56 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 03:56:54 GMT
ENV EMQX_VERSION=5.7.0
# Thu, 13 Jun 2024 03:56:54 GMT
ENV AMD64_SHA256=910d6ff5af8c36df9d15ae99a9ffe03a9690849fd952b7666b5809d9f9c42180
# Thu, 13 Jun 2024 03:56:54 GMT
ENV ARM64_SHA256=4e7c4e3f321f6ce8de5d9da93e96769a49174f62ffecc61451b2292e6f3e415f
# Thu, 13 Jun 2024 03:56:54 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Thu, 13 Jun 2024 03:57:09 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 13 Jun 2024 03:57:09 GMT
WORKDIR /opt/emqx
# Thu, 13 Jun 2024 03:57:09 GMT
USER emqx
# Thu, 13 Jun 2024 03:57:10 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Thu, 13 Jun 2024 03:57:10 GMT
EXPOSE 18083 1883 4370 5369 8083 8084 8883
# Thu, 13 Jun 2024 03:57:10 GMT
COPY file:f0e3faa715cc7e845bbdf3b121a4a8bad40d65e5cef1fac9f1285fec250cedf2 in /usr/bin/ 
# Thu, 13 Jun 2024 03:57:10 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Thu, 13 Jun 2024 03:57:10 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:2cc3ae149d28a36d28d4eefbae70aaa14a0c9eab588c3790f7979f310b893c44`  
		Last Modified: Thu, 13 Jun 2024 01:25:30 GMT  
		Size: 29.2 MB (29150430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59e1e8d8153defc8ad008583f7e666aedc4ad4ea415c563c3e8ddc71572a52ff`  
		Last Modified: Thu, 13 Jun 2024 03:59:17 GMT  
		Size: 96.7 MB (96723077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34bdc935b2ea217ab47e87cd78f93f2a87c79e989276f72c3fc93133ac1d84ff`  
		Last Modified: Thu, 13 Jun 2024 03:59:07 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:latest` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:1fc5d43018076be2ecc2ae71068c669653ffe516eb37acb85fcc853507ed0430
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.5 MB (122455516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f378277c2b8a5a2f3966d49bc49b40cadb367a581b68d56ef4926ed130501342`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Thu, 13 Jun 2024 00:39:50 GMT
ADD file:5f17f77072bcd27aa8c4d09ef5117423b789c42445b6e6c13af711dfb2abd544 in / 
# Thu, 13 Jun 2024 00:39:51 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 07:26:07 GMT
ENV EMQX_VERSION=5.7.0
# Thu, 13 Jun 2024 07:26:07 GMT
ENV AMD64_SHA256=910d6ff5af8c36df9d15ae99a9ffe03a9690849fd952b7666b5809d9f9c42180
# Thu, 13 Jun 2024 07:26:08 GMT
ENV ARM64_SHA256=4e7c4e3f321f6ce8de5d9da93e96769a49174f62ffecc61451b2292e6f3e415f
# Thu, 13 Jun 2024 07:26:08 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Thu, 13 Jun 2024 07:26:20 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 13 Jun 2024 07:26:21 GMT
WORKDIR /opt/emqx
# Thu, 13 Jun 2024 07:26:21 GMT
USER emqx
# Thu, 13 Jun 2024 07:26:21 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Thu, 13 Jun 2024 07:26:21 GMT
EXPOSE 18083 1883 4370 5369 8083 8084 8883
# Thu, 13 Jun 2024 07:26:21 GMT
COPY file:f0e3faa715cc7e845bbdf3b121a4a8bad40d65e5cef1fac9f1285fec250cedf2 in /usr/bin/ 
# Thu, 13 Jun 2024 07:26:22 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Thu, 13 Jun 2024 07:26:22 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:559a764445207341cf1207d83ceb89f1e59e2b57e860b7a80a6df6447641832b`  
		Last Modified: Thu, 13 Jun 2024 00:43:13 GMT  
		Size: 29.2 MB (29179666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e367470c1980076f657cd7f5436ef848086e592a06e509987b05c21870843c80`  
		Last Modified: Thu, 13 Jun 2024 07:28:10 GMT  
		Size: 93.3 MB (93274815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6b447fda4b95d70109b3417028bdcd0cf5cea71fa7635954581d7894f4d9088`  
		Last Modified: Thu, 13 Jun 2024 07:28:02 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
